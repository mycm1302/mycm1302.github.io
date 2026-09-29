[![Gmail](https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:mycm1302@gmail.com)[![LinkedIn](https://img.shields.io/badge/linkedin-%230077B5.svg?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/ycmoon)[![Google Scholar](https://img.shields.io/badge/Google%20Scholar-4285F4?style=for-the-badge&logo=google-scholar&logoColor=white)](https://scholar.google.co.kr/citations?user=XA4uoGAAAAAJ&hl=ko&oi=ao)

[한국어](CV_kr.md)

---

# Research Focus
> "Robotic System Development and Trajectory Optimization for Quadruped Robots"

- **Current Research Areas**: Robotic System Integration, Dynamic Analysis, Optimal Trajectory Generation
- **Affiliation**: RoDEL (Robot Design Engineering Laboratory), Hanyang University
- **Research Interests**: 
  - Robotic Overall Systems
  - Trajectory Optimization
  - System Architectures
  - Dynamics

---

# Education

- **Ph.D. in Robotics & Control Systems** (2021 - Present)
  - Department of Convergence Mechanical Engineering, Hanyang University
  - Professor: TaeWon Seo
  - Dissertation: "Quadruped Robot System Development with Rope-based Ascender Module and Trajectory Optimization"

- **M.S. in Mechanical Engineering** (2018 - 2020)
  - Department of Convergence Mechanical Engineering, Hanyang University
  - Professor: TaeWon Seo
  - Thesis: "Torque Distribution Based on Real-time Weighting Matrix Optimization Between AUV and Underwater Manipulator"

- **B.S. in Mechanical Engineering** (2014 - 2018)
  - Department of Mechanical Engineering, Hanyang University
  - Thesis: "Delta Robot for Circuit Manufacturing"

---

# Technical Skills

**Robotics & Control**
- Robot Operating System 2 (ROS2) - Advanced
- Electric System and PCB Design - Advanced
- Motion Planning - Intermediate
- Dynamics & Kinematics - Advanced

**Programming & Tools**
- C++ / Python - Advanced
- MATLAB / Simulink - Intermediate
- LabVIEW - Intermediate
- CAD Tools (SolidWorks, CATIA) - Intermediate

**Hardware & Sensors**
- Robotic Manipulators - Advanced
- IMU Sensors - Intermediate
- Force/Torque Sensors - Intermediate
- Vision Systems (Lidar, Depth Camera) - Intermediate

---

# Research Projects

## Control System Research for Ascending Quadruped Wheel-Legged Robot [2023 - Present]
> Dynamics analysis and control system development for a wheel-legged quadruped robot moving on building facades using a pair of ropes

- **Role**: Group leader of a large-scale project involving 4 institutions (CSCAM, Hanyang University, Kyonggi University, Seoul National University of Science and Technology)
- **Key Responsibilities**:
  - Design and development of the overall robot control system architecture
  - Led transition from legacy LabVIEW-based system to ROS2
  - Designed robot electrical systems and CAN communication network
- **Technical Contributions**:
  - Implemented ROS2 node-based distributed control system integrating complex mechanisms (ascender, legs, wheels)
  - Designed system architecture for efficient control of a 20-DOF robot
  - Currently advancing research from open-loop control to autonomous optimization algorithms

<div style="display: flex; flex-wrap: nowrap; justify-content: center; gap: 2%; max-width: 100%; overflow-x: auto; align-items: center;">
  <div style="flex: 0 0 48%; height: 250px; background-color: #f0f0f0;">
    <img src="/Media/Edelstro/Experiment.jpg" style="width: 100%; height: 100%; object-fit: contain;" alt="Robot Experiment">
  </div>
  <div style="flex: 0 0 48%; height: 250px; background-color: #f0f0f0;">
    <img src="/Media/Edelstro/robot structure.png" style="width: 100%; height: 100%; object-fit: contain;" alt="Robot Structure">
  </div>
</div>

![image](/Media/Edelstro/control_framework2.png)
![image](/Media/Edelstro/system_diagram.png)

[![GitHub](https://img.shields.io/badge/github-%23121011.svg?style=for-the-badge&logo=github&logoColor=white)](https://github.com/mycm1302/edelstro-control-packages) (under public review)

---

## Utility Tunnel Inspection Robot Based on ASW System [2022 - 2023]
> Development of a small Lidar SLAM robot system based on ASW for utility tunnel inspection

- **Role**: Team leader of a 2-person team, overall system design and development
- **Key Responsibilities**:
  - Robot electrical system design and implementation
  - ROS2-based integrated control system development
  - Sensor integration and data processing system development
- **Technical Contributions**:
  - Implemented Velodyne Lidar-based SLAM and localization system
  - Applied SLAM Toolbox (2D SLAM) and LeGO-LOAM (3D SLAM) algorithms
  - Implemented Nav2 framework-based DWB (Dynamic Window B) path planning algorithm
  - Developed integrated sensor module for gas, temperature, oxygen, and CO2 measurement
  - Enhanced position estimation accuracy in narrow spaces through costmap range adjustment and position update algorithms
- **Achievements**:
  - Implemented a spoke wheel-based obstacle-overcoming robot platform
  - Developed an integrated utility tunnel environment monitoring system
  - Successfully conducted validation tests at Hyundai Engineering internal facilities
  - Implemented system supporting both remote and autonomous navigation modes

<div style="display: flex; flex-wrap: nowrap; justify-content: center; gap: 2%; max-width: 100%; overflow-x: auto; align-items: center;">
  <div style="flex: 0 0 48%; height: 250px; background-color: #f0f0f0;">
    <img src="/Media/UTIR/UTIR_사진.png" style="width: 100%; height: 100%; object-fit: contain;" alt="Utility Tunnel Inspection Robot">
  </div>
  <div style="flex: 0 0 48%; height: 250px; background-color: #f0f0f0;">
    <img src="/Media/UTIR/현장사진.jpg" style="width: 100%; height: 100%; object-fit: contain;" alt="Field Test">
  </div>
</div>

![image](/Media/UTIR/UTIR_전체_그림.png)

<div style="display: flex; flex-wrap: nowrap; justify-content: center; gap: 2%; max-width: 100%; overflow-x: auto; align-items: center;">
  <div style="flex: 0 0 48%; height: 250px; background-color: #f0f0f0;">
    <img src="/Media/UTIR/SLAM.png" style="width: 100%; height: 100%; object-fit: contain;" alt="SLAM">
  </div>
  <div style="flex: 0 0 48%; height: 250px; background-color: #f0f0f0;">
    <img src="/Media/UTIR/3dslam.png" style="width: 100%; height: 100%; object-fit: contain;" alt="3D SLAM">
  </div>
</div>

---

## U.S. Delegation Project - VTT Path Planning [2022]
> Path generation for Spiral Zipper-based VTT (Variable Truss Topology) robots

- **Role**: Doctoral research assistant, system development lead, assistant researcher
- **Key Responsibilities**:
  - Support and participation in VTT (Variable Topology Truss) research team
  - System development and manual creation for subsequent visiting students
  - Research on motion primitive-based optimal movement path
- **Technical Contributions**:
  - Learned and applied embedded systems (ESP, STM32-based) for modular robot control
  - Designed and implemented ROS2 integrated control system structure
  - Researched basic behavioral principles and motion primitives of the robot
- **Achievements**:
  - Presented paper at 2022 International Conference on Ubiquitous Robots (UR)
  - Participated in research on gripping mechanisms and magnetic bearings for modular robots
  - Gained experience collaborating with international research community

![image](/Media/VTT/프로토타입.JPG)
<div style="display: flex; flex-wrap: nowrap; justify-content: center; gap: 2%; max-width: 100%; overflow-x: auto; align-items: center;">
  <div style="flex: 0 0 48%; height: 250px; background-color: #f0f0f0;">
    <img src="/Media/VTT/motion_primitive.JPG" style="width: 100%; height: 100%; object-fit: contain;" alt="Motion Primitive">
  </div>
  <div style="flex: 0 0 48%; height: 250px; background-color: #f0f0f0;">
    <img src="/Media/VTT/TrajectoryNode.JPG" style="width: 100%; height: 100%; object-fit: contain;" alt="Trajectory Node">
  </div>
</div>

---

## Wall Cleaning Robot Type Development [2021 - 2022]

<div style="display: flex; flex-wrap: nowrap; justify-content: center; gap: 2%; max-width: 100%; overflow-x: auto; align-items: center;">
  <div style="flex: 0 0 48%; height: 250px; background-color: #f0f0f0;">
    <img src="/Media/operation.png" style="width: 100%; height: 100%; object-fit: contain;" alt="Operation">
  </div>
  <div style="flex: 0 0 48%; height: 250px; background-color: #f0f0f0;">
    <img src="/Media/로프어센딩.png" style="width: 100%; height: 100%; object-fit: contain;" alt="Rope Ascending">
  </div>
</div>
<div style="display: flex; flex-wrap: nowrap; justify-content: center; gap: 2%; max-width: 100%; overflow-x: auto; align-items: center;">
  <div style="flex: 0 0 48%; height: 250px; background-color: #f0f0f0;">
    <img src="/Media/청소로봇실물구조.png" style="width: 100%; height: 100%; object-fit: contain;" alt="Cleaning Robot Structure">
  </div>
  <div style="flex: 0 0 48%; height: 250px; background-color: #f0f0f0;">
    <img src="/Media/청소로봇실물케이스.jpg" style="width: 100%; height: 100%; object-fit: contain;" alt="Cleaning Robot Case">
  </div>
</div>

---

## Underwater Robot Project [2018 - 2020]

- **Role**: Promoted from initial research assistant to senior researcher, team leader
- **Key Responsibilities**:
  - Led integration of various subsystems
  - Designed and fabricated buoyancy systems
  - Configured motor control driver system circuits
  - Organized existing code and integrated systems
- **Technical Contributions**:
  - Implemented integrated control system for underwater robot (AUV) and bilateral manipulators
  - Developed optimal torque distribution algorithm for multi-DOF cooperative system
  - Applied real-time weighting matrix optimization techniques
- **Achievements**:
  - Published journal paper in PLOS ONE ("Real-time UVMS torque distribution algorithm based on weighting matrix")
  - Completed Master's thesis
  - Successfully implemented and tested complete underwater robot system

![image](/Media/수중로봇_전체_구조.png)
<div style="display: flex; flex-wrap: nowrap; justify-content: center; gap: 2%; max-width: 100%; overflow-x: auto; align-items: center;">
  <div style="flex: 0 0 48%; height: 250px; background-color: #f0f0f0;">
    <img src="/Media/수중로봇2.jpg" style="width: 100%; height: 100%; object-fit: contain;" alt="Underwater Robot 2">
  </div>
  <div style="flex: 0 0 48%; height: 250px; background-color: #f0f0f0;">
    <img src="/Media/수중로봇.jpg" style="width: 100%; height: 100%; object-fit: contain;" alt="Underwater Robot">
  </div>
</div>

---

# Research Experience
## Participated Research Projects
1. **Development of a Robot Platform Capable of Moving Freely on Various Types of Facades**
   * Contracting Organization: National Research Foundation of Korea
   * Principal Investigator: TaeWon Seo
   * Participation Period: 2023.01.01 ~ 2025.02.28 (approx. 2 years)
   * Role: Project group leader, electrical system development, ROS2 system integration, optimal control system development
2. **Utility Tunnel Inspection Robot Technology**
   * Contracting Organization: Hyundai Engineering Co., Ltd.
   * Principal Investigator: TaeWon Seo
   * Participation Period: 2022.05.01~2022.12.31 (approx. 8 months)
   * Role: Team leader, software system development, electrical system integration
3. **Global Talent Development for Robot-Engineering Innovation Design**
   * Contracting Organization: Korea Institute for Advancement of Technology
   * Principal Investigators: TaeWon Seo/Simon Song
   * Participation Period: 2021.09.01~2022.02.28 (approx. 6 months)
   * Role: Visiting scholar, assistant researcher
4. **Development of AI-Based Adaptive Control Algorithm for Various Types of Facade Cleaning Robots**
   * Contracting Organization: National Research Foundation of Korea
   * Principal Investigator: TaeWon Seo
   * Participation Period: 2021.03.01~2021.08.31 (approx. 6 months)
   * Role: Researcher, software development
5. **Robust Position Control of Underwater Robot with Tilt Thrusters**
   * Contracting Organization: National Research Foundation of Korea
   * Principal Investigator: TaeWon Seo
   * Participation Period: 2018.09.01~2020.08.31 (approx. 2 years)
   * Role: Researcher, team leader, integrated system development
6. **Research on Multi-Scale Underwater Structure Exploration Robot Team System**
   * Contracting Organization: National Research Foundation of Korea
   * Principal Investigator: TaeWon Seo
   * Participation Period: 2018.09.01~2020.02.29 (approx. 1 year and 6 months)
   * Role: Researcher, team leader, integrated system development

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
- [공동구 점검 로봇을 이용한 공동구 내부의 실시간 점검 시스템 및 그 방법(A real-time inspection system and method for the interior of a cavity using a cavity inspection robot)](https://doi.org/10.8080/1020230122928)
- [멀티 시브 장치 및 이를 포함하는 무한 로프 윈치 시스템(Multi sheave apparatus and infinite rope winch system including the same)](https://doi.org/10.8080/1020220002870)
- [변형바퀴를 갖는 주행장치(Driving deivce with the deformed wheels)](https://doi.org/10.8080/1020190085132)

- [밧줄 보호 모듈 및 이를 포함하는 밧줄 보호 장치(Rope protection module and rope protection apparatus comprising the same)](https://doi.org/10.8080/1020220059195)
- [건물 외벽 청소 로봇(Robot for cleaning building outer wall)](https://doi.org/10.8080/1020210065790)

---

# Contact
- Academic Email: mycm1302@hanyang.ac.kr
- Lab: Robot Design Engineering Lab, Room 217, Engineering Center Main Building, Hanyang University
- Lab Website: [Robot Design Engineering Lab](http://rodel.hanyang.ac.kr/)

---

# Reference for this page
- [markdown-badges](https://github.com/Ileriayo/markdown-badges)
