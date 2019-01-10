# Chapter 2: Designing Great Watch Apps

## Glanceable, Actionable, Responsive
- 애플 워치 앱은 2초 안에 사용 가능해야 함. 즉, Glancecable하고 Actionable하고 Responsive 해야 함.
- 더 좋은 디자인을 위해 watchOS 4 에서 아래와 같은 기능이 추가되었음.

- ### Simplified Navigation
  - #### WKExtension properties
    시스템 레벨의 기능들을 앱에서 사용할 수 있도록 제공함. ex) Water Lock, Auto Rotate
  - #### The Dock
    사이드 버튼을 눌러서 앱 카드를 수직 스크롤로 볼 수 있게 함.
  - #### Vertical page-based navigation
    - 계층구조를 가진 테이블 기반의 앱을 수직 스크롤로 볼 수 있게 함.
    - 스와이프나 디지털 크라운을 통해 테이블의 디테일 인터페이스를 볼 수 있게 함.
  - #### Single page app
    - 여러 페이지 간에 이동할 필요 없이 한 페이지 내에서 스크롤 만으로 볼 수 있게 함.
  - #### Scroll position
    - 특정 위치로 스크롤 할 수 있는 API 제공
  - #### Full screen
    - SpriteKit이나 SceneKit 기반의 앱에서 상태바가 없는 풀스크린으로 보여질 수 있도록 함.
  - #### Overlap layout
    - 인터페이스 그룹의 레이아웃을 Overlap으로 설정하면 하위 뷰들이 서로 오버랩하여 배치될 수 있도록 함.
  - #### Quick-swap for clock faces
    - 엣지 스와이핑을 하면 시계 화면으로 넘어갈 수 있게함.
    - 사용자가 다양한 활동을 위한 다양한 시계 화면을 설정할 수 있도록 함.
    
- ### Discoverability
  - 애플에서는 모든 앱이 Complication을 제공하도록 권장함.

- ### Session-based use
  - 손목을 떨구면 최대 8초까지 FrontMost 앱으로 남아있을 수 있게 함.
  - 다시 손목을 들었을 때 바로 앱을 사용할 수 있게 함.

- ### Quck launch for apps
  - 앱이 Dock이나 현재 시계의 Complication으로 로드되어 있으면, 대기시간 없이 바로 앱을 런치할 수 있도록 함.

- ### Inputs
  - Scribble을 통하여 텍스트를 쉽게 입력할 수 있도록 함.

<BR>

## API Overview
- ### Background Refresh and Snapshot
  - SnapShot API와 Background Refresh API를 통하여 손목을 떨궈도 앱이 최신상태를 유지하도록 함.

- ### In-line Audio Recording and Background Mode
  - 백그라운드에서도 실시간으로 오디오 녹음이 가능하도록 함. 실시간 번역에 유용할 듯.
  
- ### Core Bluetooth
  - 혈당 체크기 같은 주변기기들과 페어링이 가능.
  - 최대 2개의 기기들과 연결 가능하며, 느리지만 백그라운드에서도 통신 가능.
  
- ### Location
  - 백그라운드에서도 위치정보를 받을 수 있게 함.
  
- ### Game
  - SpriteKit과 SceneKit으로 게임을 개발 가능.


- ### Gyroscope and Digital Crown
  - 자이로스코프나 가속기, 디지털 크라운의 데이터를 받을 수 있게 함.

<BR>

## Interaction Consideration
- 애플 워치의 사용 특성상 사용자를 기다리게 해서는 안됨.
- 백그라운드 리프레시와 퀵런치 기능이 추가된 이유임.
- 2초의 법칙을 기억할 것.

- ### Anatomy of a Watch app
  - 애플 워치는 '앱'만으로는 부족함.
  - 컴플리케이션과 노티피케이션, 앱이 모두 좋은 사용자 경험을 제공해야 함.

- ### Use rich animations to communicate complex concepts
  - 애플 워치는 화면이 작기 때문에 정보를 이미지와 애니메이션 기반으로 제공할 것을 권장함.
  - 노티피케이션에도 적용하면 좋음.

- ### Planning versus implementing
  - 좋은 애플 워치 사용자 경험을 제공하기 위해서는 구현보다는 기획에 시간을 더 쏟을 것.










  

    
