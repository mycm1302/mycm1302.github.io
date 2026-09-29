# RigidBodyDynamics 함수 문서화

## URDFReadFromFile

```cpp
RigidBodyDynamics::Addons::URDFReadFromFile(urdfFilePath, robotModel, enableVerboseOutput, addFixedBaseInertia);
```

**설명:** URDF(Unified Robot Description Format) 파일을 읽어 로봇 모델을 생성합니다.

**입력:**
- `urdfFilePath`: URDF 파일 경로 (C-스타일 문자열)
- `robotModel`: 채워질 RigidBodyDynamics 모델 객체 (포인터)
- `enableVerboseOutput`: 상세 로깅 활성화 여부 (bool)
- `addFixedBaseInertia`: 루트 링크에 고정 기준 관성 추가 여부 (bool)

**출력:**
- 성공 시 `true`, 실패 시 `false` 반환
- `robotModel`에 URDF 파일 내용 기반 모델 구성

## CalcBodyToBaseCoordinates

```cpp
RigidBodyDynamics::CalcBodyToBaseCoordinates(robotModel, jointPositions, bodyId, localPointPosition, updateKinematics);
```

**설명:** 특정 바디에 부착된 점의 베이스(월드) 좌표를 계산합니다.

**입력:**
- `robotModel`: RigidBodyDynamics 모델 (참조)
- `jointPositions`: 관절 위치 벡터
- `bodyId`: 대상 바디의 ID
- `localPointPosition`: 로컬 좌표계에서의 점 위치
- `updateKinematics`: 동적 업데이트 활성화 여부

**출력:**
- 베이스 좌표계를 기준으로 한 3차원 점 위치 벡터

## CalcBaseToBodyCoordinates

```cpp
RigidBodyDynamics::CalcBaseToBodyCoordinates(robotModel, jointPositions, bodyId, basePointPosition, updateKinematics);
```

**설명:** 베이스(월드) 좌표계의 점을 특정 바디의 로컬 좌표계로 변환합니다.

**입력:**
- `robotModel`: RigidBodyDynamics 모델 (참조)
- `jointPositions`: 관절 위치 벡터
- `bodyId`: 대상 바디의 ID
- `basePointPosition`: 베이스 좌표계에서의 점 위치
- `updateKinematics`: 동적 업데이트 활성화 여부

**출력:**
- 특정 바디 좌표계를 기준으로 한 3차원 점 위치 벡터

## CalcBodyWorldOrientation

```cpp
RigidBodyDynamics::CalcBodyWorldOrientation(robotModel, jointPositions, bodyId, updateKinematics);
```

**설명:** 특정 바디의 월드 좌표계 기준 방향(orientation)을 계산합니다.

**입력:**
- `robotModel`: RigidBodyDynamics 모델 (참조)
- `jointPositions`: 관절 위치 벡터
- `bodyId`: 대상 바디의 ID
- `updateKinematics`: 동적 업데이트 활성화 여부

**출력:**
- 바디의 월드 좌표계 기준 방향을 나타내는 3x3 회전 행렬

## CalcPointJacobian

```cpp
RigidBodyDynamics::CalcPointJacobian(robotModel, jointPositions, bodyId, localPointPosition, jacobianMatrix, updateKinematics);
```

**설명:** 특정 바디의 한 점에 대한 자코비안 행렬을 계산합니다. 자코비안은 관절 공간의 미분 변화에 따른 월드 좌표에서의 점 이동 관계를 나타냅니다.

**입력:**
- `robotModel`: RigidBodyDynamics 모델 (참조)
- `jointPositions`: 관절 위치 벡터
- `bodyId`: 대상 바디의 ID
- `localPointPosition`: 로컬 좌표계에서의 점 위치
- `jacobianMatrix`: 결과를 저장할 자코비안 행렬 (참조)
- `updateKinematics`: 동적 업데이트 활성화 여부

**출력:**
- `jacobianMatrix`에 계산된 자코비안 행렬 저장

## CalcPointVelocity

```cpp
RigidBodyDynamics::CalcPointVelocity(robotModel, jointPositions, jointVelocities, bodyId, localPointPosition, updateKinematics);
```

**설명:** 바디의 특정 점의 선속도를 계산합니다.

**입력:**
- `robotModel`: RigidBodyDynamics 모델 (참조)
- `jointPositions`: 관절 위치 벡터
- `jointVelocities`: 관절 속도 벡터
- `bodyId`: 대상 바디의 ID
- `localPointPosition`: 로컬 좌표계에서의 점 위치
- `updateKinematics`: 동적 업데이트 활성화 여부

**출력:**
- 계산된 점의 선속도를 3차원 벡터로 반환

## CompositeRigidBodyAlgorithm

```cpp
RigidBodyDynamics::CompositeRigidBodyAlgorithm(robotModel, jointPositions, massMatrix, updateKinematics);
```

**설명:** 로봇의 관성 행렬(Mass Matrix)을 계산합니다. 이는 동역학 방정식에서 중요한 요소입니다.

**입력:**
- `robotModel`: RigidBodyDynamics 모델 (참조)
- `jointPositions`: 관절 위치 벡터
- `massMatrix`: 결과를 저장할 관성 행렬 (참조)
- `updateKinematics`: 동적 업데이트 활성화 여부

**출력:**
- `massMatrix`에 계산된 관성 행렬 저장

## NonlinearEffects

```cpp
RigidBodyDynamics::NonlinearEffects(robotModel, jointPositions, jointVelocities, nonlinearTerms);
```

**설명:** 코리올리력, 원심력, 중력 등 비선형 동역학 효과를 계산합니다.

**입력:**
- `robotModel`: RigidBodyDynamics 모델 (참조)
- `jointPositions`: 관절 위치 벡터
- `jointVelocities`: 관절 속도 벡터
- `nonlinearTerms`: 결과를 저장할 비선형 효과 벡터 (참조)

**출력:**
- `nonlinearTerms`에 계산된 비선형 효과(코리올리, 원심력, 중력)를 저장

## InverseKinematics

```cpp
RigidBodyDynamics::InverseKinematics(robotModel, initialJointPositions, bodyId, targetPosition, targetOrientation, &outputJointPositions, tolerance);
```

**설명:** 특정 바디가 목표 위치와 방향에 도달하기 위한 관절 각도를 계산합니다.

**입력:**
- `robotModel`: RigidBodyDynamics 모델 (참조)
- `initialJointPositions`: 초기 관절 위치 벡터
- `bodyId`: 대상 바디의 ID
- `targetPosition`: 목표 위치 (월드 좌표계)
- `targetOrientation`: 목표 방향 (회전 행렬)
- `tolerance`: 수렴 허용 오차

**출력:**
- `outputJointPositions`: 계산된 관절 위치 벡터
- 성공 여부를 나타내는 불리언 값

## ForwardDynamics

```cpp
RigidBodyDynamics::ForwardDynamics(robotModel, jointPositions, jointVelocities, jointTorques, &jointAccelerations);
```

**설명:** 관절 위치, 속도, 토크가 주어졌을 때 시스템의 관절 가속도를 계산합니다.

**입력:**
- `robotModel`: RigidBodyDynamics 모델 (참조)
- `jointPositions`: 관절 위치 벡터
- `jointVelocities`: 관절 속도 벡터
- `jointTorques`: 관절 토크 벡터

**출력:**
- `jointAccelerations`: 계산된 관절 가속도 벡터

## InverseDynamics

```cpp
RigidBodyDynamics::InverseDynamics(robotModel, jointPositions, jointVelocities, jointAccelerations, &jointTorques);
```

**설명:** 관절 위치, 속도, 가속도가 주어졌을 때 필요한 관절 토크를 계산합니다.

**입력:**
- `robotModel`: RigidBodyDynamics 모델 (참조)
- `jointPositions`: 관절 위치 벡터
- `jointVelocities`: 관절 속도 벡터
- `jointAccelerations`: 관절 가속도 벡터

**출력:**
- `jointTorques`: 계산된 관절 토크 벡터

## UpdateKinematics

```cpp
RigidBodyDynamics::UpdateKinematics(robotModel, jointPositions, jointVelocities, jointAccelerations);
```

**설명:** 로봇 모델의 전체 운동학적 상태(위치, 속도, 가속도)를 업데이트합니다.

**입력:**
- `robotModel`: RigidBodyDynamics 모델 (참조)
- `jointPositions`: 관절 위치 벡터
- `jointVelocities`: 관절 속도 벡터 (선택적)
- `jointAccelerations`: 관절 가속도 벡터 (선택적)

**출력:**
- 없음 (모델 내부 상태 업데이트)

## Forward kinematics - 없음

**대체 기능**
- `UpdateKinematics`: 모델의 전체 운동학 상태를 업데이트합니다.
- `CalcBodyToBaseCoordinates`: 특정 바디의 위치를 계산하는 순방향 운동학 연산을 수행합니다.
- `CalcBodyWorldOrientation`: 특정 바디의 방향을 계산하는 순방향 운동학 연산을 수행합니다.