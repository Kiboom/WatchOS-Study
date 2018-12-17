# Chapter 3: Architecture

- watchOS 앱을 잘 만들려면 Watch와 WatchKit 프레임워크의 기초에 대해 잘 알아야 함.

## Exploring Watch
- ### Operating System
  - watchOS는 iOS 위에서 만들어진 OS

- ### Interaction
  - 탭과 스와이프 제스처, 포스터치만 지원함. 멀티제스처는 아직 지원 안함.
  
- ### The Watch Display
  - 워치 디스플레이는 4:5 비율을 가짐. (하지만 4세대 워치는 비율이 달라짐)
  
## Introducing WatchKit
- watchKit은 Apple Watch 앱을 구성하는 클래스와 인터페이스 빌더의 그룹임. 
- watch 앱은 일종의 extension으로서, 아이폰 페어링 없이는 설치될 수 없음.

## WatchKit Apps
- Watch 앱은 세 파트로 구성됨.
- iOS App: 호스트 역할을 하는 iOS 앱. 
- Watch App: 워치 앱에 필요한 번들 파일 및 리소스.
- Watch Extension: 워치에 전송되는 소스 파일.

## WatchKit classes
- ### WKInterfaceController
  - UIViewController와 매우 흡사한 역할과 라이프사이클을 가짐.
- ### Interface objects
  - UIView와 비슷한 역할을 하는 WKInterfaceObject를 상속받은 클래스들.
  - Watch의 뷰에 대한 프록시 객체임. write-only.
  - WKInterfaceObject를 상속받는 19개의 서브클래스가 있음.
      - iOS에 비하면 인터랙션이 제한적임. 
  - 오토레이아웃이나 프레임 개념이 없음. HTML과 CSS처럼 자체 사이즈와 인접 뷰를 바탕으로 자동 레이아웃 됨.
  - 유저 인터페이스는 코드가 아닌 스토리보드를 통해 생성됨.

## The dock
- 최근 사용한 앱을 백그라운드에서 suspended 상태로 보관하는 것.

## Notifications
- short look과 long look으로 구분됨.

## Complications
- 워치 페이스에 추가 가능한 써드 파티 커스터마이징

  
