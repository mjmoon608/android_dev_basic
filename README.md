# android_dev_basic
google code labs - https://codelabs.developers.google.com/android-training/

# Android 기본 사항 01.1 : Android Studio 및 Hello World
- 배울 것
  1. Android Studio IDE 설치 및 사용 방법
  2. Android 앱을 개발하기 위해 개발 프로세스를 사용하는 방법
  3. 템플리셍서 Android 프로젝트를 만드는 방법
  4. 디버깅 목적으로 앱에 로그 메시지를 추가하는 방법

## 작업2: Hello World 앱 만들기
- 회사 도메인(패키지네임?)은 그대로 사용하거나 고유한 회사 도메인을 만듦.
  - 앱을 게시하지 않으려는 경우 기본값을 그대로 사용할 수 있음. <b>나중에 앱의 패키지 이름을 변경하려면 추가 작업이 필요함</b>
  
  
- ```API 15: Android 4.0.3 IceCreamSandwich```를 최소 SDK로 설정하면 20년 2월 기준 Google Play에 활성화된 Android 기기의 97%와 호환

### 2.4 앱 및 res 폴더 탐색
- ```app - java``` 폴더 밑에는 3개의 하위 폴더에 자바 클래스 파일이 포합되어 있음
- 두, 세번째 폴더는 테스트에 사용되며 다른 단원에서 설명됨.

### 2.5 매니페스트 폴더 탐색

- ```AndroidManifest.xml```파일은 Android 앱의 모든 구성 요소를 설명함

## 작업4 : (선택 사항)물리적 장치 사용

### 4.1 USB 디버깅 켜기
- Android Studio가 기기와 통신하도록 하려면 Android 기기에서 USB 디버깅을 켜야함.
- 장치의 ```개발자 옵션``` 설정에서 활성화

- <b>Android Studio에서 기기를 인식하지 못할 시</b>
  1. 장치를 분리했다가 다시 연결
  2. Android Studio를 다시 시작
  
- 여전히 장치를 찾지 못하거나 "unauthorized"으로 선언한 경우
  1. 장치를 분리
  2. 기기에서 <b>개발자 옵션</b>열기
  3. <b>USB 디버깅</b>인증 취소 누르기
  4. 기기를 컴퓨터에 다시 연결
  5. 메세지가 표시되면 권한을 부여
  
  
## 작업 5: 앱 Gradle 구성 변경

- 다른 곳에서 프로젝트를 옮겨 와서 세탕하는 경우 자신의 SDK 버전과 맞지 않아 에러가 발생할 수 있음. 이떄 설정 하는 것

- ```build.gradle(Module:app)```파일열기
- ```defaultConfig``` 블록의 ```minSdkVersion``` 값을 ```17```로 변경(보통 ```15```로 설정한다고 하는데 강의에선 ```17``` 쓰는 듯)
- Sync Now 하기

## 작업 6 : 앱에 로그 문 추가
- 앱에 ```Log```문장을 추가하여 <b>Logcat</b>창에 메세지를 표시. ```Log```메시지는 <b>값, 실행 경로 및 예외보고</b>를 확인하는데 사용할 수 있는 강력한 디버깅 도구
