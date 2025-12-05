# Real-Time_Simulator_for_Multi-Axis_Robot
다관절 로봇 실시간 시뮬레이터(Real Time Simulator  for Multi Axis Robot)

<img width="200" height="300" alt="Digitla_Twin_Robot_Simulator" src="https://github.com/user-attachments/assets/ebc5995b-5646-4fb0-a9cb-499f32e42fca" />


# 목차 (Table of Contents)

- [Chapter 1. 본서의 구성](#chapter-1-본서의-구성)
- [Chapter 2. 소프트웨어 개요](#chapter-2-소프트웨어-개요)
  - [2.1 Indy7 - CoppeliaSim 연동 소프트웨어 개요](#21-indy7---coppeliasim-연동-소프트웨어-개요)
  - [2.2 Indy7 / STEP / CONTY 개요](#22-indy7--step--conty-개요)
  - [2.3 CoppeliaSim Edu 개요](#23-coppeliasim-edu-개요)
- [Chapter 3. Indy7 - CoppeliaSim 연동 소프트웨어](#chapter-3-indy7---coppeliasim-연동-소프트웨어)
  - [3.1 Indy7 - CoppeliaSim 연동 소프트웨어 개요](#31-indy7---coppeliasim-연동-소프트웨어-개요-1)
    - [3.1.1 NRMK Indy7 - CoppeliaSim 시뮬레이션 방법 및 구성](#311-nrmk-indy7---coppeliasim-시뮬레이션-방법-및-구성)
    - [3.1.2 Indy7 Conty - STEP - CoppeliaSim 연동 방법](#312-indy7-conty---step---coppeliasim-연동-방법)
    - [3.1.3 Indy7Conty-Copp-Middleware 사용 방법](#313-indy7conty-copp-middleware-사용-방법)
  - [3.2 Indy7 STEP - CoppeliaSim 연동 Simulator 사용방법](#32-indy7-step---coppeliasim-연동-simulator-사용방법)
    - [3.2.1 Indy7 STEP - CoppeliaSim 연동 시뮬레이터](#321-indy7-step---coppeliasim-연동-시뮬레이터)
    - [3.2.2 Indy7 STEP - CoppeliaSim 연동 시뮬레이터 사용 방법](#322-indy7-step---coppeliasim-연동-시뮬레이터-사용-방법)
  - [3.3 단독 구동 CoppeliaSim Interface Software 사용방법](#33-단독-구동-coppeliasim-interface-software-사용방법)
    - [3.3.1 CoppeliaSim 단독 구동 방법](#331-coppeliasim-단독-구동-방법)
    - [3.3.2 Indy7-Copp-Standalone 사용 방법](#332-indy7-copp-standalone-사용-방법)
- [Chapter 4. Indy7 - CoppeliaSim 연동 소프트웨어 적용 예제](#chapter-4-indy7---coppeliasim-연동-소프트웨어-적용-예제)
  - [4.1 ROBOTIQ-85 그리퍼를 적용한 Pick-and-Place 적용 예제](#41-robotiq-85-그리퍼를-적용한-pick-and-place-적용-예제)
    - [4.1.1 예제 구성](#411-예제-구성)
    - [4.1.2 Indy7의 Pick-and-Place 예제를 실행하기 위한 준비 항목](#412-indy7의-pick-and-place-예제를-실행하기-위한-준비-항목)
    - [4.1.3 Pick-and-Place 구현 방법](#413-pick-and-place-구현-방법)
    - [4.1.4 Pick-and-Place 실행](#414-pick-and-place-실행)
  - [4.2 ROBOTIQ-85 그리퍼를 적용한 Palletizing 적용 예제](#42-robotiq-85-그리퍼를-적용한-palletizing-적용-예제)
    - [4.2.1 예제 구성](#421-예제-구성)
    - [4.2.2 CoppeliaSim에서 Indy7의 Palletizing 예제를 실행하기 위한 준비 항목](#422-coppeliasim에서-indy7의-palletizing-예제를-실행하기-위한-준비-항목)
    - [4.2.3 Pick-and-Place 구현 방법](#423-pick-and-place-구현-방법)
  - [4.3 Indy7 로봇 카페 적용 예제](#43-indy7-로봇-카페-적용-예제)
    - [4.3.1 예제 구성](#431-예제-구성-1)
  - [4.4 Indy7 로봇 카페 예제를 실행하기 위한 준비 항목](#44-indy7-로봇-카페-예제를-실행하기-위한-준비-항목)
    - [4.4.1 Indy7 로봇 카페 구현 방법](#441-indy7-로봇-카페-구현-방법)
- [Chapter 5. Robotic manipulator model 구성 방법](#chapter-5-robotic-manipulator-model-구성-방법)
  - [5.1 Indy7의 3D 모델 파일 다운로드](#51-indy7의-3d-모델-파일-다운로드)
  - [5.2 Indy7 mesh 입력 및 시뮬레이션 모델 작성](#52-indy7-mesh-입력-및-시뮬레이션-모델-작성)
- [Chapter 6. CoppeliaSim Edu 프로그래밍](#chapter-6-coppeliasim-edu-프로그래밍)
  - [6.1 CoppeliaSim Edu의 Script 사용방법](#61-coppeliasim-edu의-script-사용방법)
    - [6.1.1 CoppeliaSim Edu의 Script 개요](#611-coppeliasim-edu의-script-개요)
    - [6.1.2 Python API 개요](#612-python-api-개요)
    - [6.1.3 BlueZero remote API를 활용한 CoppeliaSim Edu 코드 작성 방법](#613-bluezero-remote-api를-활용한-coppeliasim-edu-코드-작성-방법)



      
