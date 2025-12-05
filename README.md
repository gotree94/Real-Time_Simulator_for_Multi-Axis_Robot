# Real-Time_Simulator_for_Multi-Axis_Robot
다관절 로봇 실시간 시뮬레이터(Real Time Simulator  for Multi Axis Robot)

<img width="400" height="600" alt="Digitla_Twin_Robot_Simulator" src="https://github.com/user-attachments/assets/ebc5995b-5646-4fb0-a9cb-499f32e42fca" />


# 목차 (Table of Contents)

- [Chapter 1. 본서의 구성](#chapter-1-본서의-구성)
- [Chapter 2. 소프트웨어 개요](#chapter-2-소프트웨어-개요)
  - [2.1 Indy7 - CoppeliaSim 연동 소프트웨어 개요](#21-indy7---coppeliasim-연동-소프트웨어-개요)
  - [2.2 Indy7 / STEP / CONTY 개요](#22-indy7--step--conty-개요)
  - [2.3 CoppeliaSim Edu 개요](#23-coppeliasim-edu-개요)
- [Chapter 3. Indy7 - CoppeliaSim 연동 소프트웨어](#chapter-3-indy7---coppeliasim-연동-소프트웨어)
  - [3.1 Indy7 - CoppeliaSim 연동 소프트웨어 개요](#31-indy7---coppeliasim-연동-소프트웨어-개요-1)
    - [3.1.1 시스템 아키텍처 및 통신 구조](#311-시스템-아키텍처-및-통신-구조)
    - [3.1.2 설치 및 개발 환경 설정](#312-설치-및-개발-환경-설정)
    - [3.1.3 주요 API 및 인터페이스 소개](#313-주요-api-및-인터페이스-소개)
  - [3.2 Indy7 / STEP / CONTY 개요](#32-indy7--step--conty-개요-1)
    - [3.2.1 STEP 제어기 환경 설정](#321-step-제어기-환경-설정)
    - [3.2.2 CONTY를 이용한 로봇 티칭 기초](#322-conty를-이용한-로봇-티칭-기초)
  - [3.3 CoppeliaSim Edu 개요](#33-coppeliasim-edu-개요-1)
    - [3.3.1 시뮬레이션 환경 및 UI 구성](#331-시뮬레이션-환경-및-ui-구성)
    - [3.3.2 씬(Scene) 객체 관리 및 속성](#332-씬scene-객체-관리-및-속성)
- [Chapter 4. Indy7 - CoppeliaSim 연동 소프트웨어 적용 예제](#chapter-4-indy7---coppeliasim-연동-소프트웨어-적용-예제)
  - [4.1 기본 모션 제어 (Basic Motion)](#41-기본-모션-제어-basic-motion)
    - [4.1.1 Joint Space 제어 (MoveJ)](#411-joint-space-제어-movej)
    - [4.1.2 Task Space 제어 (MoveL)](#412-task-space-제어-movel)
    - [4.1.3 원호 보간 제어 (MoveC)](#413-원호-보간-제어-movec)
    - [4.1.4 웨이포인트(Waypoint) 추종](#414-웨이포인트waypoint-추종)
  - [4.2 센서 데이터 연동 및 피드백](#42-센서-데이터-연동-및-피드백)
    - [4.2.1 가상 비전 센서 연동](#421-가상-비전-센서-연동)
    - [4.2.2 충돌 감지 (Collision Detection)](#422-충돌-감지-collision-detection)
    - [4.2.3 토크 센서 데이터 로깅](#423-토크-센서-데이터-로깅)
  - [4.3 응용 작업 시뮬레이션](#43-응용-작업-시뮬레이션)
    - [4.3.1 Pick and Place 구현](#431-pick-and-place-구현)
  - [4.4 디지털 트윈 동기화](#44-디지털-트윈-동기화)
    - [4.4.1 실제 로봇과 시뮬레이션 동기화 테스트](#441-실제-로봇과-시뮬레이션-동기화-테스트)
- [Chapter 5. Robotic manipulator model 구성 방법](#chapter-5-robotic-manipulator-model-구성-방법)
  - [5.1 Indy7 URDF 모델링 및 Import](#51-indy7-urdf-모델링-및-import)
  - [5.2 Joint 및 Link 파라미터 설정](#52-joint-및-link-파라미터-설정)
- [Chapter 6. CoppeliaSim Edu 프로그래밍](#chapter-6-coppeliasim-edu-프로그래밍)
  - [6.1 Lua 스크립트 프로그래밍](#61-lua-스크립트-프로그래밍)
    - [6.1.1 Child Script의 구조](#611-child-script의-구조)
    - [6.1.2 주요 Sim API 함수 활용](#612-주요-sim-api-함수-활용)
    - [6.1.3 외부 통신 (ZeroMQ/Remote API) 구현](#613-외부-통신-zeromqremote-api-구현)



