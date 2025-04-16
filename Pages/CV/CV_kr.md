[![Gmail](https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:mycm1302@gmail.com)[![LinkedIn](https://img.shields.io/badge/linkedin-%230077B5.svg?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/ycmoon)[![Google Scholar](https://img.shields.io/badge/Google%20Scholar-4285F4?style=for-the-badge&logo=google-scholar&logoColor=white)](https://scholar.google.co.kr/citations?user=XA4uoGAAAAAJ&hl=ko&oi=ao)

[English](README_en.md)

---

# Research Focus
> "로봇 시스템 구축 및 4족 로봇의 Trajectory optimization"

- **현재 연구 분야**: 로봇 시스템 구축, 역학 해석, 최적 경로 생성
- **소속**: 한양대학교 로봇 설계 연구실 RoDEL (Robot Design engineering laboratory)
- **관심 분야**: 
  - Robotic overall Systems
  - Trajectory optimization
  - System Architectures
  - Dynamics

---

# Education

- **Ph.D. in Robotics & Control Systems** (2021 - Present)
  - 한양대학교 융합기계공학과
  - Professor: TaeWon Seo
  - 논문주제: "로프 기반 어센더 모듈을 이용한 4족 로봇 시스템 구축과 Trajectory optimization"

- **M.S. in Mechanical Engineering** (2018 - 2020)
  - 한양대학교 융합기계공학과
  - Professor: TaeWon Seo
  - 논문: "Torque distribution based on real-time weighting matrix optimization between AUV and underwater manipulator"

- **B.S. in Mechanical Engineering** (2014 - 2018)
  - 한양대학교 기계공학과
  - 논문: "Delta robot for circuit manufacturing"

---

# Technical Skills

**Robotics & Control**
- Robot Operating System 2 (ROS2) - 고급
- Electric system and PCB desgin - 고급
- Motion Planning - 중급
- Dynamics & Kinematics - 고급

**Programming & Tools**
- C++ / Python - 고급
- MATLAB / Simulink - 중급
- LabVIEW - 중급
- CAD Tools (SolidWorks, CATIA) - 중급

**Hardware & Sensors**
- Robotic Manipulators - 고급
- IMU Sensors - 중급
- Force/Torque Sensors - 중급
- Vision Systems (Lidar, despth camera) - 중급

---

# Research Projects

## 어센딩 4족 휠레그 로봇의 제어 시스템 연구 [2023 - Present]
> 1쌍의 로프로 건물 외벽을 이동하는 휠레그 4족 로봇의 역학 해석 및 제어 시스템 제시

- **역할**: 4개 기관(CSCAM, 한양대학교, 경기대학교, 서울과학기술대학교) 참여 대형 과제의 그룹장
- **주요 책임**:
  - 전체 로봇 제어 시스템 아키텍처 설계 및 개발 책임
  - 레거시 LabVIEW 기반 시스템에서 ROS2로의 전환 주도
  - 로봇 전장부 설계 및 CAN 통신 시스템 구축
- **기술적 기여**:
  - 복합 메커니즘(어센더, 레그, 휠) 통합을 위한 ROS2 노드 기반 분산 제어 시스템 구현
  - 20자유도 로봇의 효율적 제어를 위한 시스템 아키텍처 설계
  - 오픈 루프 제어 시스템에서 자율 최적화 알고리즘으로의 발전 연구 진행 중

<div style="display: flex; flex-wrap: nowrap; justify-content: center; gap: 2%; max-width: 100%; overflow-x: auto; align-items: center;">
  <div style="flex: 0 0 48%; height: 250px; background-color: #f0f0f0;">
    <img src="/Media/Edelstro/Experiment.jpg" style="width: 100%; height: 100%; object-fit: contain;" alt="수중로봇2">
  </div>
  <div style="flex: 0 0 48%; height: 250px; background-color: #f0f0f0;">
    <img src="/Media/Edelstro/robot structure.png" style="width: 100%; height: 100%; object-fit: contain;" alt="수중로봇">
  </div>
</div>

![image](/Media/Edelstro/control_framework2.png)
![image](/Media/Edelstro/system_diagram.png)

[![GitHub](https://img.shields.io/badge/github-%23121011.svg?style=for-the-badge&logo=github&logoColor=white)](https://github.com/mycm1302/edelstro-control-packages) (공개 검토중)

---

## ASW 시스템을 기반으로 한 공동구 탐색 로봇 [2022 - 2023]
> 공동구 탐색을 위한 소형 ASW 기반의 Lidar SLAM 로봇 시스템 개발

- **역할**: 2인 팀의 팀장, 시스템 설계 및 개발 총괄
- **주요 책임**:
  - 로봇 전장 시스템 설계 및 구현
  - ROS2 기반 통합 제어 시스템 구축
  - 센서 통합 및 데이터 처리 시스템 개발
- **기술적 기여**:
  - 벨로다인 라이다 기반 SLAM 및 로컬라이제이션 시스템 구현
  - SLAM Toolbox(2D SLAM) 및 LeGO-LOAM(3D SLAM) 알고리즘 적용
  - Nav2 프레임워크 기반 DWB(Dynamic Window B) 경로 계획 알고리즘 구현
  - 가스, 온도, 산소, CO2 측정을 위한 통합 센서 모듈 개발
  - 좁은 공간에서의 위치 추정 정확도 향상을 위한 코스트맵 레인지 조정 및 위치 재갱신 알고리즘 개발
- **성과**:
  - 스포크 휠 기반 장애물 극복 로봇 플랫폼 구현
  - 공동구 환경 모니터링 통합 시스템 개발
  - 현대엔지니어링 내부 시설에서 실증 테스트 성공적 수행
  - 원격 및 자율 주행 모드 지원 시스템 구현

<div style="display: flex; flex-wrap: nowrap; justify-content: center; gap: 2%; max-width: 100%; overflow-x: auto; align-items: center;">
  <div style="flex: 0 0 48%; height: 250px; background-color: #f0f0f0;">
    <img src="/Media/UTIR/UTIR_사진.png" style="width: 100%; height: 100%; object-fit: contain;" alt="수중로봇2">
  </div>
  <div style="flex: 0 0 48%; height: 250px; background-color: #f0f0f0;">
    <img src="/Media/UTIR/현장사진.jpg" style="width: 100%; height: 100%; object-fit: contain;" alt="수중로봇">
  </div>
</div>

![image](/Media/UTIR/UTIR_전체_그림.png)

<div style="display: flex; flex-wrap: nowrap; justify-content: center; gap: 2%; max-width: 100%; overflow-x: auto; align-items: center;">
  <div style="flex: 0 0 48%; height: 250px; background-color: #f0f0f0;">
    <img src="/Media/UTIR/SLAM.png" style="width: 100%; height: 100%; object-fit: contain;" alt="수중로봇2">
  </div>
  <div style="flex: 0 0 48%; height: 250px; background-color: #f0f0f0;">
    <img src="/Media/UTIR/3dslam.png" style="width: 100%; height: 100%; object-fit: contain;" alt="수중로봇">
  </div>
</div>

---

## 미국 파견 사업 - VTT 경로 이동 패스플래닝 [2022 - 2022]
> Spiral zipper 기반 VTT(Variable Truss Topology) 로봇의 이동 경로 생성

- **역할**: 박사과정 연구원, 시스템 구축 담당, 보조 연구원
- **주요 책임**:
  - VTT(Variable Topology Truss) 연구팀 지원 및 연구 참여
  - 후속 파견 학생들을 위한 시스템 구축 및 매뉴얼 작성
  - 모션 프리미티브 기반 최적 이동 경로 연구 수행
- **기술적 기여**:
  - 모듈러 로봇 제어를 위한 임베디드 시스템(ESP, STM32 기반) 학습 및 적용
  - ROS2 통합 제어 시스템 구조 설계 및 구현
  - 로봇의 기초 행동 원리 및 모션 프리미티브 연구
- **성과**:
  - 2022 International Conference on Ubiquitous Robots(UR) 논문 발표
  - 모듈러 로봇의 그리핑 메커니즘 및 마그네틱 베어링 연구 참여
  - 해외 연구 커뮤니티와의 협업 경험 습득

![image](/Media/VTT/프로토타입.JPG)
<div style="display: flex; flex-wrap: nowrap; justify-content: center; gap: 2%; max-width: 100%; overflow-x: auto; align-items: center;">
  <div style="flex: 0 0 48%; height: 250px; background-color: #f0f0f0;">
    <img src="/Media/VTT/motion_primitive.JPG" style="width: 100%; height: 100%; object-fit: contain;" alt="수중로봇2">
  </div>
  <div style="flex: 0 0 48%; height: 250px; background-color: #f0f0f0;">
    <img src="/Media/VTT/TrajectoryNode.JPG" style="width: 100%; height: 100%; object-fit: contain;" alt="수중로봇">
  </div>
</div>

---

## 벽면 청소 로봇 타입 개발 [2021 - 2022]

<div style="display: flex; flex-wrap: nowrap; justify-content: center; gap: 2%; max-width: 100%; overflow-x: auto; align-items: center;">
  <div style="flex: 0 0 48%; height: 250px; background-color: #f0f0f0;">
    <img src="/Media/operation.png" style="width: 100%; height: 100%; object-fit: contain;" alt="수중로봇2">
  </div>
  <div style="flex: 0 0 48%; height: 250px; background-color: #f0f0f0;">
    <img src="/Media/로프어센딩.png" style="width: 100%; height: 100%; object-fit: contain;" alt="수중로봇">
  </div>
</div>
<div style="display: flex; flex-wrap: nowrap; justify-content: center; gap: 2%; max-width: 100%; overflow-x: auto; align-items: center;">
  <div style="flex: 0 0 48%; height: 250px; background-color: #f0f0f0;">
    <img src="/Media/청소로봇실물구조.png" style="width: 100%; height: 100%; object-fit: contain;" alt="수중로봇2">
  </div>
  <div style="flex: 0 0 48%; height: 250px; background-color: #f0f0f0;">
    <img src="/Media/청소로봇실물케이스.jpg" style="width: 100%; height: 100%; object-fit: contain;" alt="수중로봇">
  </div>
</div>

---

## 수중 로봇 프로젝트 [2018 - 2020]

- **역할**: 초기 연구 보조원에서 선임 연구원으로 승진, 팀장 역할 수행
- **주요 책임**:
  - 다양한 하위 시스템 통합 작업 주도
  - 부력체 설계 및 제작
  - 모터 제어 드라이버 시스템 회로 구성
  - 기존 코드 정리 및 시스템 통합
- **기술적 기여**:
  - 수중 로봇(AUV)과 양쪽 매니퓰레이터의 통합 제어 시스템 구현
  - 다자유도 협력 시스템의 최적 토크 분배 알고리즘 개발
  - 실시간 가중치 행렬 최적화 기법 적용
- **성과**:
  - PLOS ONE 저널 논문 출판 ("Real-time UVMS torque distribution algorithm based on weighting matrix")
  - 석사 학위 논문 완성
  - 완전한 수중 로봇 시스템 구현 및 테스트 완료

![image](/Media/수중로봇_전체_구조.png)
<div style="display: flex; flex-wrap: nowrap; justify-content: center; gap: 2%; max-width: 100%; overflow-x: auto; align-items: center;">
  <div style="flex: 0 0 48%; height: 250px; background-color: #f0f0f0;">
    <img src="/Media/수중로봇2.jpg" style="width: 100%; height: 100%; object-fit: contain;" alt="수중로봇2">
  </div>
  <div style="flex: 0 0 48%; height: 250px; background-color: #f0f0f0;">
    <img src="/Media/수중로봇.jpg" style="width: 100%; height: 100%; object-fit: contain;" alt="수중로봇">
  </div>
</div>

---

# Research Experience
## 참여 연구과제
1. **다양한 형태의 외벽에서 자유롭게 이동이 가능한 로봇 플랫폼 개발**
   * 협약기관: (재)한국연구재단
   * 연구책임자: 서태원
   * 참여기간: 2023.01.01 ~ 2025.02.28 (약 2년)
   * 참여역할: 프로젝트 그룹장, 전장부 구축, ROS2 시스템 구축, 최적 제어 시스템 구축
2. **공동구 점검 로봇 기술**
   * 협약기관: 현대엔지니어링 (주)
   * 연구책임자: 서태원
   * 참여기간: 2022.05.01~2022.12.31 (약 8개월)
   * 참여역할: 팀장, 소프트웨어 시스템 구축, 전장 시스템 구축
3. **로봇-엔지니어링 혁신설계 글로벌인재양성**
   * 협약기관: 한국산업기술진흥원
   * 연구책임자: 서태원/송시몬
   * 참여기간: 2021.09.01~2022.02.28 (약 6개월)
   * 참여역할: Visiting scholar, 보조연구원
4. **여러 형태의 외벽청소 로봇의 인공지능 기반 적응형 제어알고리즘 개발**
   * 협약기관: (재)한국연구재단
   * 연구책임자: 서태원
   * 참여기간: 2021.03.01~2021.08.31 (약 6개월)
   * 참여역할: 연구원, 소프트웨어 구축
5. **틸트 쓰러스터를 가지는 수중 로봇의 강건 위치 제어**
   * 협약기관: (재)한국연구재단
   * 연구책임자: 서태원
   * 참여기간: 2018.09.01~2020.08.31 (약 2년)
   * 참여역할: 연구원, 팀장, 통합시스템 구축
6. **멀티 스케일 수중 구조물 탐사 로봇 팀 시스템 연구**
   * 협약기관: (재)한국연구재단
   * 연구책임자: 서태원
   * 참여기간: 2018.09.01~2020.02.29 (약 1년 6개월)
   * 참여역할: 연구원, 팀장, 통합시스템 구축

---


---

# Publications
## Journal Papers
### As Primary Author
1. Chae, H., Moon, Y., Lee, K., Park, S., Kim, H. S., & Seo, T. (2022). A tethered façade cleaning robot based on a dual rope windlass climbing mechanism: Design and experiments. IEEE/ASME Transactions on Mechatronics, 27(4), 1982-1989.
2. Moon, Y., Hong, J., Jin, S., Bae, J., & Seo, T. (2021). Real-time UVMS torque distribution algorithm based on weighting matrix. Plos one, 16(7), e0253771.

### As Contributing Author
1. Bak, J., Moon, Y., Kim, J., Mohan, S., Seo, T., & Jin, S. (2022). Hovering control of an underwater robot with tilting thrusters using the decomposition and compensation method based on a redundant actuation model. Robotics and Autonomous Systems, 150, 103995.
2. Bae, J., Moon, Y., Park, E., Kim, J., Jin, S., & Seo, T. (2022). Cooperative underwater vehicle-manipulator operation using redundant resolution method. International Journal of Precision Engineering and Manufacturing, 23(9), 1003-1017.
3. Lee, J., Park, G., Moon, Y., Lee, S., & Seo, T. (2019). Robust design of detecting contaminants in façade cleaning applications. IEEE Access, 8, 2869-2884.
4. Kyong, H., Choi, M., Moon, Y., Lee, K., Kim, J., Kim, T., & Seo, T. (2021). Position error compensation of Façade-cleaning robot by optimal rope winch design. IEEE Access, 9, 143392-143405.
5. Ahn, S., Hyun, D., Moon, Y., Lee, J., Kim, H., & Seo, T. (2025). Two-DoF turret mechanism for a rope-driven wheel-legged climbing robot on a 3D façade. Measurement, 242, 116073.

---

## Conference Presentations
### As Primary Author
1. Moon, Y., Hyun, D., Ahn, S., Lee, J., Joo, H., Kim, J., Kim, H., & Seo, T. Experimental study of a mobile robot that can move the dome shape façade. 대한기계학회 춘추학술대회, 2024, 206-207.
2. Moon, Y., Bae, J., Yim, M., & Seo, T. Simulation Study on the Locomotion Algorithm of Variable Topology Truss Robot based on Motion Primitives. In: 2022 19th International Conference on Ubiquitous Robots (UR). IEEE, 2022. p. 219-224.
3. Yecheol Moon, Jangho Bae, Sangrok Jin, Jongwon Kim, TaeWon Seo. Redundant Resolution Method of an Underwater Manipulation for Disturbance Rejection. IEEE/RSJ International Conference on Intelligent Robots and Systems, 2019.
4. 문예철, 안사훈, 현동근, 김채원, 도현구, 주형찬, 이종명, 이강엽, 권준혁, 김지홍, 김화수, 서태원. 비정형 형상 외벽 이동을 위한 로봇 시스템의 설계. 한국로봇종합학술대회, 2024.

### As Contributing Author
1. 안사훈, 현동근, 문예철, 이종명, 김화수, 서태원. 비정형 외벽 건물 환경에서 로프 구동 기반 휠레그 등반 로봇의 적응 제어 전략. 대한기계학회 춘추학술대회, 2024, 40-41.
2. 이종명; 문예철; 서태원. 기울어진 스포크 휠을 가지는 로봇의 현장 적용 연구. 대한기계학회 춘추학술대회, 2023, 69-70.
3. 도현구, 김지홍, 안사훈, 문예철, 현동근, 양정모, 주형찬, 김화수, 서태원. 비정형 외벽 장애물 극복을 위한 휠-레그 로봇의 궤적 최적화. 대한기계학회 춘추학술대회, 2023, 1375-1375.
4. 서태원, 권준혁, 이경욱, 최명진, 문예철, 이종명. 3 차원 공간을 이동할 수 있는 등강기 기반 모바일 로봇의 해석. 한국정밀공학회 학술발표대회 논문집, 2023, 45-45.
5. Chae, H., Moon, Y., Lee, K. O., Park, S. J., Kim, H. S., & Seo, T. Design and development of wall cleaning robot with dual rope climbing mechanism. 대한기계학회 춘추학술대회, 2021, 1637-1640.
6. 홍종인, 문예철, 배장호, 박정애, 진상록, 김종원, 서태원. 높은 마찰의 수중 매니퓰레이터 모듈의 LuGre 모델을 이용한 마찰 모델 및 보상. 대한기계학회 춘추학술대회, 2020, 165-166.
7. 박정애, 문예철, 배장호, 서태원. 수중 로봇 매니퓰레이터의 하드웨어 설계. 한국정밀공학회 학술발표대회 논문집, 2019, 346-346.
8. 박정애, 문예철, 배장호, 진상록, 서태원. 틸팅하는 추진기를 지닌 수중로봇의 추력벡터 분해와 안티와인드업 기법으로 구성된 제어기의 제어 이득 최적화. 한국정밀공학회 학술발표대회 논문집, 2019, 73-73.
9. Jeongae Bak, Yecheol Moon, Sangrok Jin, Jongwon Kim, TaeWon Seo. Hovering Control of a TTURT with Thrust Vector Decomposition Technique. IEEE/RSJ International Conference on Intelligent Robots and Systems, 2019.
10. 김혁, 문예철. 얀센 메커니즘의 다리 보행 로봇 개발 및 최적화. EDISON SW 활용 경진대회 논문집, 2016, 417-423.


## As Contributing Author
1. 안사훈, 현동근, 문예철, 이종명, 김화수, 서태원. 비정형 외벽 건물 환경에서 로프 구동 기반 휠레그 등반 로봇의 적응 제어 전략. 대한기계학회 춘추학술대회, 2024, 40-41.
2. 이종명; 문예철; 서태원. 기울어진 스포크 휠을 가지는 로봇의 현장 적용 연구. 대한기계학회 춘추학술대회, 2023, 69-70.
3. 도현구, 김지홍, 안사훈, 문예철, 현동근, 양정모, 주형찬, 김화수, 서태원. 비정형 외벽 장애물 극복을 위한 휠-레그 로봇의 궤적 최적화. 대한기계학회 춘추학술대회, 2023, 1375-1375.
4. 서태원, 권준혁, 이경욱, 최명진, 문예철, 이종명. 3 차원 공간을 이동할 수 있는 등강기 기반 모바일 로봇의 해석. 한국정밀공학회 학술발표대회 논문집, 2023, 45-45.
5. Chae, H., Moon, Y., Lee, K. O., Park, S. J., Kim, H. S., & Seo, T. Design and development of wall cleaning robot with dual rope climbing mechanism. 대한기계학회 춘추학술대회, 2021, 1637-1640.
6. 홍종인, 문예철, 배장호, 박정애, 진상록, 김종원, 서태원. 높은 마찰의 수중 매니퓰레이터 모듈의 LuGre 모델을 이용한 마찰 모델 및 보상. 대한기계학회 춘추학술대회, 2020, 165-166.
7. 박정애, 문예철, 배장호, 서태원. 수중 로봇 매니퓰레이터의 하드웨어 설계. 한국정밀공학회 학술발표대회 논문집, 2019, 346-346.
8. 박정애, 문예철, 배장호, 진상록, 서태원. 틸팅하는 추진기를 지닌 수중로봇의 추력벡터 분해와 안티와인드업 기법으로 구성된 제어기의 제어 이득 최적화. 한국정밀공학회 학술발표대회 논문집, 2019, 73-73.
9. Jeongae Bak, Yecheol Moon, Sangrok Jin, Jongwon Kim, TaeWon Seo. Hovering Control of a TTURT with Thrust Vector Decomposition Technique. IEEE/RSJ International Conference on Intelligent Robots and Systems, 2019.
10. 김혁, 문예철. 얀센 메커니즘의 다리 보행 로봇 개발 및 최적화. EDISON SW 활용 경진대회 논문집, 2016, 417-423.

# Patent
## US patent
- [Building exterior wall cleaning robot](https://patents.google.com/patent/US20240217092A1/en)

## KR patent
- [밧줄 보호 모듈 및 이를 포함하는 밧줄 보호 장치(Rope protection module and rope protection apparatus comprising the same)](https://doi.org/10.8080/1020220059195)
- [공동구 점검 로봇을 이용한 공동구 내부의 실시간 점검 시스템 및 그 방법(A real-time inspection system and method for the interior of a cavity using a cavity inspection robot)](https://doi.org/10.8080/1020230122928)
- [멀티 시브 장치 및 이를 포함하는 무한 로프 윈치 시스템(Multi sheave apparatus and infinite rope winch system including the same)](https://doi.org/10.8080/1020220002870)
- [변형바퀴를 갖는 주행장치(Driving deivce with the deformed wheels)](https://doi.org/10.8080/1020190085132)
- [건물 외벽 청소 로봇(Robot for cleaning building outer wall)](https://doi.org/10.8080/1020210065790)

---

# Contact
- Academic Email: mycm1302@hanyang.ac.kr
- Lab: 한양대학교 공업센터본관 217호 로봇설계연구실
- Lab Website: [Robot Design Engineering Lab](http://rodel.hanyang.ac.kr/)

---

# Reference for this page
- [markdown-badges](https://github.com/Ileriayo/markdown-badges)
