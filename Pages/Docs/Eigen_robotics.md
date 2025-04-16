# Eigen 로보틱스 관련 내용 정리

## 기본 타입 및 선언
```cpp
// 고정 크기 벡터/행렬
Vector3d v;                     // 3차원 벡터 (double)
Matrix3d m;                     // 3x3 행렬 (double)
Matrix4f m;                     // 4x4 행렬 (float)

// 가변 크기 벡터/행렬
VectorXd v(n);                  // n차원 벡터
MatrixXd m(rows, cols);         // rows x cols 행렬

// 특수 행렬 초기화
MatrixXd::Zero(rows, cols);     // 영행렬
MatrixXd::Identity(n, n);       // 단위행렬
MatrixXd::Ones(rows, cols);     // 모든 원소가 1
VectorXd::Zero(n);              // 영벡터
```

## 행렬 접근 및 조작
```cpp
// 인덱싱 (0부터 시작)
v(0);                           // 벡터의 첫 번째 요소
m(1, 2);                        // 행렬의 2행 3열 요소

// 블록 접근
v.segment(start, length);       // 벡터의 부분 접근
m.block(startRow, startCol, rows, cols); // 행렬의 부분 접근

// 행/열 접근
m.row(i);                       // i번째 행
m.col(j);                       // j번째 열

// 전치
m.transpose();                  // 행렬 전치

// 크기 정보
v.size();                       // 벡터 크기
m.rows();                       // 행 수
m.cols();                       // 열 수

// 특정 요소들 설정
v.setZero();                    // 영벡터로 설정
m.setIdentity();                // 단위행렬로 설정
```

## 로봇 운동학 및 동역학
```cpp
// 회전 행렬 (SO(3))
Matrix3d R;                     // 회전 행렬
AngleAxisd rot(angle, axis);    // 축-각 표현
R = rot.toRotationMatrix();     // 회전 행렬로 변환

// 쿼터니언 (단위 쿼터니언)
Quaterniond q(w, x, y, z);      // 쿼터니언 (w가 실수부)
Quaterniond q(R);               // 회전 행렬에서 변환
Matrix3d R = q.toRotationMatrix(); // 회전 행렬로 변환

// 오일러 각
// ZYX 컨벤션 (Roll-Pitch-Yaw)
Vector3d euler = R.eulerAngles(2, 1, 0); // Z-Y-X 순서

// 변환 행렬 (SE(3))
Matrix4d T = Matrix4d::Identity();
T.block<3,3>(0,0) = R;          // 회전 부분 설정
T.block<3,1>(0,3) = p;          // 위치 부분 설정

// 동차 변환에서 회전/위치 추출
Matrix3d R = T.block<3,3>(0,0);
Vector3d p = T.block<3,1>(0,3);
```

## 연산 및 수치 계산
```cpp
// 기본 연산
v1 + v2;                        // 벡터 덧셈
m1 * m2;                        // 행렬 곱셈
m * v;                          // 행렬-벡터 곱셈
v1.dot(v2);                     // 내적
v1.cross(v2);                   // 외적 (3D 벡터만)

// 정규화
v.norm();                       // 벡터 크기(L2 노름)
v.squaredNorm();                // 제곱 노름 (계산 효율적)
v.normalized();                 // 정규화된 벡터 (새 벡터 반환)
v.normalize();                  // 벡터 정규화 (원본 수정)

// 행렬 분해
// SVD
JacobiSVD<MatrixXd> svd(m, ComputeFullU | ComputeFullV);
MatrixXd U = svd.matrixU();
MatrixXd V = svd.matrixV();
VectorXd S = svd.singularValues();

// 역행렬
MatrixXd mInv = m.inverse();    // 완전한 역행렬
MatrixXd mPinv = svd.solve(MatrixXd::Identity(m.rows(), m.rows())); // 의사역행렬

// QR 분해
HouseholderQR<MatrixXd> qr(m);
MatrixXd Q = qr.householderQ();
MatrixXd R = qr.matrixQR().triangularView<Upper>();

// LU 분해
FullPivLU<MatrixXd> lu(m);
MatrixXd P = lu.permutationP();
MatrixXd L = lu.matrixLU().triangularView<StrictlyLower>().toDenseMatrix() + MatrixXd::Identity(m.rows(), m.cols());
MatrixXd U = lu.matrixLU().triangularView<Upper>();
```

## 로보틱스 특화 연산
```cpp
// 외적 행렬 (skew-symmetric matrix)
Matrix3d skew(const Vector3d& v) {
  Matrix3d m = Matrix3d::Zero();
  m(0, 1) = -v(2);
  m(0, 2) =  v(1);
  m(1, 0) =  v(2);
  m(1, 2) = -v(0);
  m(2, 0) = -v(1);
  m(2, 1) =  v(0);
  return m;
}

// 각속도를 이용한 쿼터니언 미분
Quaterniond qDot(const Quaterniond& q, const Vector3d& omega) {
  Quaterniond result;
  result.w() = -0.5 * (q.x()*omega(0) + q.y()*omega(1) + q.z()*omega(2));
  result.x() =  0.5 * (q.w()*omega(0) - q.z()*omega(1) + q.y()*omega(2));
  result.y() =  0.5 * (q.z()*omega(0) + q.w()*omega(1) - q.x()*omega(2));
  result.z() = -0.5 * (q.y()*omega(0) - q.x()*omega(1) - q.w()*omega(2));
  return result;
}

// 야코비안 계산 (수치미분 예시)
MatrixXd numericalJacobian(Function f, VectorXd x, double eps=1e-6) {
  VectorXd f0 = f(x);
  MatrixXd J = MatrixXd::Zero(f0.size(), x.size());
  
  for (int i = 0; i < x.size(); i++) {
    VectorXd x_perturb = x;
    x_perturb(i) += eps;
    VectorXd f_perturb = f(x_perturb);
    J.col(i) = (f_perturb - f0) / eps;
  }
  
  return J;
}
```

## 관절 공간과 작업 공간 변환
```cpp
// 순기구학 (Forward Kinematics) 함수 형태
Matrix4d forwardKinematics(const VectorXd& joint_angles) {
  // DH 파라미터나 기타 방법으로 계산
  // ...
  return T_end_effector;
}

// 역기구학 (Inverse Kinematics) - 반복적 방법
VectorXd inverseKinematics(const Matrix4d& desired_pose, const VectorXd& initial_guess) {
  VectorXd q = initial_guess;
  double error_threshold = 1e-6;
  int max_iterations = 100;
  
  for (int i = 0; i < max_iterations; i++) {
    Matrix4d current_pose = forwardKinematics(q);
    // 에러 계산 (위치와 방향)
    VectorXd error = calculatePoseError(desired_pose, current_pose);
    
    if (error.norm() < error_threshold)
      break;
      
    // 자코비안 계산
    MatrixXd J = calculateJacobian(q);
    
    // 자코비안 의사역행렬
    MatrixXd J_pinv = J.completeOrthogonalDecomposition().pseudoInverse();
    
    // 조인트 값 업데이트
    q += J_pinv * error;
  }
  
  return q;
}
```

## 경로 및 궤적 계산
```cpp
// 직선 보간 (LERP)
Vector3d lerp(const Vector3d& p0, const Vector3d& p1, double t) {
  return p0 + t * (p1 - p0);
}

// 구면 선형 보간 (SLERP)
Quaterniond slerp(const Quaterniond& q0, const Quaterniond& q1, double t) {
  return q0.slerp(t, q1);
}

// 3차 다항식 궤적 생성
VectorXd cubicPolynomial(double t, double t0, double tf,
                         const VectorXd& q0, const VectorXd& qf,
                         const VectorXd& v0, const VectorXd& vf) {
  double h = tf - t0;
  double normalized_t = (t - t0) / h;
  
  // 3차 다항식 계수
  VectorXd a0 = q0;
  VectorXd a1 = v0 * h;
  VectorXd a2 = 3.0 * (qf - q0) - 2.0 * v0 * h - vf * h;
  VectorXd a3 = -2.0 * (qf - q0) + v0 * h + vf * h;
  
  // q(t) = a0 + a1*t' + a2*t'^2 + a3*t'^3, where t' = (t-t0)/(tf-t0)
  return a0 + a1 * normalized_t + a2 * normalized_t * normalized_t + 
         a3 * normalized_t * normalized_t * normalized_t;
}
```

## 저차원 동역학 방정식
```cpp
// M(q)q̈ + C(q,q̇)q̇ + G(q) = τ

// 관성 행렬 (Inertia Matrix)
MatrixXd calculateMassMatrix(const VectorXd& q) {
  // 로봇 모델에 따라 계산
  // ...
  return M;
}

// 코리올리스 및 원심력 항
VectorXd calculateCoriolisMatrix(const VectorXd& q, const VectorXd& qdot) {
  // 로봇 모델에 따라 계산
  // ...
  return C;
}

// 중력 항
VectorXd calculateGravityVector(const VectorXd& q) {
  // 로봇 모델에 따라 계산
  // ...
  return G;
}

// 역동역학 (Inverse Dynamics)
VectorXd inverseDynamics(const VectorXd& q, const VectorXd& qdot, const VectorXd& qddot) {
  MatrixXd M = calculateMassMatrix(q);
  VectorXd C = calculateCoriolisMatrix(q, qdot);
  VectorXd G = calculateGravityVector(q);
  
  return M * qddot + C + G;
}
```

## 유용한 디버깅 팁
```cpp
// 행렬/벡터 출력
std::cout << "Matrix M:\n" << M << std::endl;

// 행렬 차원 확인
std::cout << "M dimensions: " << M.rows() << "x" << M.cols() << std::endl;

// NaN 또는 Inf 확인
bool hasNaN = m.array().isNaN().any();
bool hasInf = m.array().isInf().any();

// 값 범위 제한
v = v.array().min(upper_limit).max(lower_limit);

// 행렬 비교 (근사)
bool isApprox = m1.isApprox(m2, tolerance);  // tolerance는 epsilon 값
```

## 최적화 팁
```cpp
// 매핑없이 블록 연산 (속도 향상)
m.noalias() += a * b.transpose();

// 행렬 크기가 컴파일 타임에 알려진 경우 고정 크기 사용
Matrix<double, 6, 6> jacobian;  // 6x6 자코비안

// 메모리 정렬 및 루프 최적화
// 열 우선 순서로 접근 (Eigen의 기본 저장 방식이 열 우선)
for (int j = 0; j < m.cols(); ++j) {
  for (int i = 0; i < m.rows(); ++i) {
    // m(i, j) 접근
  }
}
```