lane_detection_project
====
- **Lane detection**

[![lane_detection](http://img.youtube.com/vi/faHEmd_3msI/0.jpg)](https://youtu.be/faHEmd_3msI)
</br>
</br>

- **Object detection (Detection Result / BEV result)**

[![Object detection](http://img.youtube.com/vi/CmKZm0-LfUw/0.jpg)](https://youtu.be/CmKZm0-LfUw)
[![Object detection](http://img.youtube.com/vi/-DNyKI_qmKc/0.jpg)](https://youtu.be/-DNyKI_qmKc)
</br>
</br>

객체 인식 및 depth 추정 프로젝트
===
> **프로그래머스 K-Digital Training 자율주행 데브코스 15주차 프로젝트**  
> 1:10 스케일 모형 차(Xycar)를 활용한 객체 인식 및 depth 추정 프로젝트 (Object Detection & Depth Estimation project using 1:10 scale model car(Xycar))  
> 개발기간 (Development period): 2024.01.16 ~ 2024.01.26
</br>

## 팀 소개
| 팀원 | 팀원 | 팀원 | 멘토 |
|:------:|:------:|:------:|:---:|
| 김윤지 | 박성준 | 허동욱 |이치현|
|[@younji524](https://github.com/younji524)|[@jagbum](https://github.com/jagbum)|[@dongwookheo](https://github.com/dongwookheo)|[@hyunny223](https://github.com/hyuny223)|
</br>

## 프로젝트 소개
![경진대회 전체맵](https://github.com/object-detection-team4/lane_detection_project/assets/76142194/bc6ea7c9-e11b-4bb4-a4da-591648dc6bc9)

- 카메라 센서로 차선을 인식하여, Xycar가 주어진 코스를 완주할 수 있도록 한다. 
- 카메라 센서로 주어진 표지판과 신호등을 인식하여, 코스를 벗어나지 않으며 해당 표지판과 일치하는 주행을 할 수 있도록 한다.
  - 신호등에 맞추어 전진 혹은 정지 주행하도록 한다. 
  - 정지 표지판, 횡단보도 앞에서는 정지선 직전 45cm 이내에서 정지하도록 한다.
  - 코스 내 정적 장애물은 피해서 주행하고, 동적 장애물 등장 시 정지하도록 한다.
</br>

## 환경 설정
### Requirements
- OpenCV 4.5.5
- ROS melodic
- Ubuntu 18.04 LTS

## 주요 기능
### modules
#### Common.hpp
- 차선의 상태를 나타내는 구조체, 유지 보수를 위한 PREC data type 선언
#### ImageProcessor.hpp, ImageProcessor.cpp
- 차선 검출을 위한 이미지 전처리 담당 클래스 정의
#### KalmanFilter.hpp, KalmanFilter.cpp
- 차선 예측을 위한 칼만 필터 클래스 정의
#### LaneDetector.hpp, LaneDetector.cpp
- 차선 검출 담당 클래스 정의
#### LaneManager.hpp, LaneManager.cpp
- 차선 검출 시스템을 총괄, yolo detection 결과에 따른 객체 인식 및 깊이 추정 시스템을 총괄하는 클래스 정의
#### PIDController.hpp, PIDController.cpp
- PID 제어기 클래스 정의
#### XycarController.hpp, XycarController.cpp
- Xycar 컨트롤러 클래스 정의
#### draw.hpp
- 디버깅을 위한 그리기 함수 정의

### Run system
- 차선 인식 주행
```
roslaunch lane_detection main_xycar.launch
```

## Stacks
### Environment
<img src="https://img.shields.io/badge/ubuntu-E95420?style=for-the-badge&logo=ubuntu&logoColor=white"> <img src="https://img.shields.io/badge/visualstudiocode-007ACC?style=for-the-badge&logo=visualstudiocode&logoColor=white"> <img src="https://img.shields.io/badge/clion-000000?style=for-the-badge&logo=clion&logoColor=white">
<img src="https://img.shields.io/badge/git-F04032?style=for-the-badge&logo=git&logoColor=white"> <img src="https://img.shields.io/badge/github-181717?style=for-the-badge&logo=github&logoColor=white"> 

### Config
<img src="https://img.shields.io/badge/yaml-CB171E?style=for-the-badge&logo=yaml&logoColor=white">

### Development
<img src="https://img.shields.io/badge/cplusplus-00599C?style=for-the-badge&logo=cplusplus&logoColor=white"> <img src="https://img.shields.io/badge/ros-22314E?style=for-the-badge&logo=ros&logoColor=white"> 
<img src="https://img.shields.io/badge/opencv-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white">
<img src="https://img.shields.io/badge/cmake-064F8C?style=for-the-badge&logo=cmake&logoColor=white">

### Communication
<img src="https://img.shields.io/badge/slack-4A154B?style=for-the-badge&logo=slack&logoColor=white"> <img src="https://img.shields.io/badge/notion-000000?style=for-the-badge&logo=notion&logoColor=white">
<img src="https://img.shields.io/badge/jira-0052CC?style=for-the-badge&logo=jira&logoColor=white">

