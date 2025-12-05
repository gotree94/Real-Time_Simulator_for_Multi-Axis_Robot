# Real-Time_Simulator_for_Multi-Axis_Robot
다관절 로봇 실시간 시뮬레이터(Real Time Simulator  for Multi Axis Robot)

<img width="200" height="300" alt="Digitla_Twin_Robot_Simulator" src="https://github.com/user-attachments/assets/ebc5995b-5646-4fb0-a9cb-499f32e42fca" />


# Indy7 - CoppeliaSim 연동 소프트웨어 교재 개요

## 목차 (Table of Contents)

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

***

## Chapter 1. 본서의 구성

본 장은 교재를 효과적으로 활용하기 위한 안내서입니다. 독자가 본서의 **학습 목표**, **대상 독자**, 그리고 **각 장의 내용 흐름과 연계성**을 명확히 이해하도록 돕습니다. 특히, **Indy7 하드웨어, STEP 제어기, CONTY 소프트웨어, CoppeliaSim 시뮬레이터, 연동 미들웨어** 등 본서에서 다루는 주요 구성 요소 간의 관계를 간략하게 소개하며 학습 경로를 제시합니다.

---

## Chapter 2. 소프트웨어 개요

본 장은 Indy7 로봇 시스템과 시뮬레이션 환경 구축에 필수적인 소프트웨어들의 **기본 개념과 역할**을 정의합니다.

### 2.1 Indy7 - CoppeliaSim 연동 소프트웨어 개요
실제 로봇 제어 환경과 가상 시뮬레이션 환경을 연결하는 **NRMK 연동 미들웨어(Middleware)**의 필요성과 기능적 개요를 다룹니다. 이 소프트웨어는 로봇의 **상태** 및 **명령**을 실시간으로 양방향 통신하는 핵심적인 역할을 수행합니다.

### 2.2 Indy7 / STEP / CONTY 개요
* **Indy7:** 뉴로메카의 7자유도 협동 로봇 모델을 소개하고 기본적인 사양을 설명합니다.
* **STEP:** Indy7의 **실시간 제어기(Controller) 펌웨어** 및 임베디드 플랫폼으로서의 역할을 정의합니다.
* **CONTY:** STEP 제어기를 PC에서 모니터링하고 **티칭(Teaching), 파라미터 설정** 등을 수행하는 사용자 인터페이스(GUI) 프로그램의 사용법을 설명합니다.

### 2.3 CoppeliaSim Edu 개요
**CoppeliaSim**의 특징과 **Edu(Education) 버전**의 주요 기능을 소개합니다. 씬(Scene) 구성, 물리 엔진(Physics Engine) 설정, 객체(Object) 속성 관리 등 시뮬레이션 환경 구축에 필요한 기초 지식을 제공합니다.


---

## Chapter 3. Indy7 - CoppeliaSim 연동 소프트웨어

본 장은 실제 Indy7 시스템을 CoppeliaSim과 연동하는 구체적인 **기술적 방법론과 소프트웨어 구조**를 깊이 있게 다룹니다.

### 3.1 Indy7 - CoppeliaSim 연동 소프트웨어 개요

* **3.1.1 NRMK Indy7 - CoppeliaSim 시뮬레이션 방법 및 구성**
    * **통신 아키텍처:** **STEP 제어기**와 **CoppeliaSim** 간의 데이터 흐름 및 통신 계층을 구조화하여 설명합니다.
* **3.1.2 Indy7 Conty - STEP - CoppeliaSim 연동 방법**
    * 실제 로봇 제어 명령이 **CONTY**를 거쳐 **STEP**으로 전달되고, 그 결과를 **CoppeliaSim**의 가상 모델에 반영하는 과정을 단계별로 설명합니다.
* **3.1.3 Indy7Conty-Copp-Middleware 사용 방법**
    * 뉴로메카에서 제공하는 **미들웨어**의 설치, 설정 파일 구성, 그리고 연동 실행 절차를 상세히 안내합니다.

### 3.2 Indy7 STEP - CoppeliaSim 연동 Simulator 사용방법

* **3.2.1 Indy7 STEP - CoppeliaSim 연동 시뮬레이터**
    * STEP 제어기 로직이 시뮬레이션 환경에서 어떻게 **디지털 트윈(Digital Twin)** 형태로 동작하는지 그 원리를 다룹니다.
* **3.2.2 Indy7 STEP - CoppeliaSim 연동 시뮬레이터 사용 방법**
    * 연동 시뮬레이터를 실행하고, **CONTY**를 통해 시뮬레이션상의 로봇을 실제로 제어하는 방법을 실습합니다.

### 3.3 단독 구동 CoppeliaSim Interface Software 사용방법

* **3.3.1 CoppeliaSim 단독 구동 방법**
    * STEP 제어기 없이 **CoppeliaSim 자체 스크립트(Lua) 또는 외부 API**만을 활용하여 로봇 모델을 구동하는 방법을 소개합니다.
* **3.3.2 Indy7-Copp-Standalone 사용 방법**
    * 제어 로직을 외부 프로그램(예: **Python**)에서 작성하여 CoppeliaSim 모델을 직접 제어하는 독립 실행형(Standalone) 연동 소프트웨어의 사용법을 설명합니다.

---

## Chapter 4. Indy7 - CoppeliaSim 연동 소프트웨어 적용 예제

본 장은 앞서 배운 연동 기술을 활용하여 실제 산업 및 서비스 분야의 로봇 작업 예제를 시뮬레이션으로 구현합니다.

### 4.1 ROBOTIQ-85 그리퍼를 적용한 Pick-and-Place 적용 예제
가장 기본적인 로봇 응용 작업인 **Pick-and-Place(집어 들고 놓기)**를 **ROBOTIQ-85 그리퍼** 모델을 사용하여 구현합니다.
* **4.1.3 Pick-and-Place 구현 방법:** **MoveJ, MoveL** 등의 로봇 모션 명령어와 그리퍼 제어 신호를 조합하여 작업 순서를 프로그래밍합니다.

### 4.2 ROBOTIQ-85 그리퍼를 적용한 Palletizing 적용 예제
규칙적으로 물체를 쌓거나 해체하는 **Palletizing(팔레타이징)** 작업을 구현합니다.
* **4.2.2 준비 항목:** 다수의 물체와 팔레트 구조를 CoppeliaSim 씬에 배치하고 **작업 좌표계(WCS) 설정** 등 시뮬레이션 준비 과정을 상세히 설명합니다.
* **4.2.3 Pick-and-Place 구현 방법:** 반복적인 **좌표 계산**과 **반복문(Loop)**을 사용하여 효율적인 Palletizing 경로를 생성하는 방법을 중점적으로 설명합니다.


### 4.3 Indy7 로봇 카페 적용 예제
더 복잡한 서비스 로봇 애플리케이션인 **로봇 카페** 시나리오를 구성하며 **다단계 순차 작업**의 예제를 다룹니다.

### 4.4 Indy7 로봇 카페 예제를 실행하기 위한 준비 항목
* **4.4.1 Indy7 로봇 카페 구현 방법:** 물체 트래킹(Tracking), 순차 이벤트 발생 등 **복합적인 시뮬레이션 제어 로직**을 구성하는 방법을 실습합니다.

---

## Chapter 5. Robotic manipulator model 구성 방법

본 장은 로봇 제조사에서 제공하는 3D 모델 파일을 CoppeliaSim 환경에 가져와서 **시뮬레이션 가능한 로봇 모델**을 만드는 과정을 설명합니다.

### 5.1 Indy7의 3D 모델 파일 다운로드
**STEP** 파일, **STL** 파일 등 **Indy7의 3D 모델 파일(Mesh)**을 확보하고 준비하는 절차를 안내합니다.

### 5.2 Indy7 mesh 입력 및 시뮬레이션 모델 작성
다운로드한 Mesh 파일을 CoppeliaSim에 불러와서 **각 관절(Joint)과 링크(Link)**를 정의하고, **기구학적 관계(Kinematic Chain)**를 설정하여 동작 가능한 시뮬레이션 모델로 완성하는 방법을 다룹니다.

---

## Chapter 6. CoppeliaSim Edu 프로그래밍

본 장은 CoppeliaSim 환경에서 로봇과 객체를 제어하기 위한 다양한 **프로그래밍 방식**을 다룹니다.

### 6.1 CoppeliaSim Edu의 Script 사용방법

* **6.1.1 CoppeliaSim Edu의 Script 개요**
    * CoppeliaSim의 기본 스크립트 언어인 **Lua Script**의 기본 문법과 스크립트 유형별 특징을 소개합니다.
* **6.1.2 Python API 개요**
    * CoppeliaSim을 **외부 프로그램(Python)**으로 제어하기 위한 **Remote API** 구조와 **Python API** 사용법의 기초를 설명합니다.
* **6.1.3 BlueZero remote API를 활용한 CoppeliaSim Edu 코드 작성 방법**
    * **BlueZero (BZ) Remote API**를 이용해 로봇의 위치, 속도 명령을 전송하고 상태 피드백을 수신하는 **실제 코드 작성 방법**과 예시를 상세히 제시합니다.
 


