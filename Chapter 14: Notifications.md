# Chapter 14: Notifications
- iOS 10과 watchOS 3 부터 아이폰과 워치 앱에서 모두 노티를 설정 가능.
- watchOS는 short look과 long look 노티가 있음.

## Getting Started
- 아이폰에서 로컬 및 리모트 노티를 받으면 iOS는 아이폰에 보여줄 지 워치에 보여줄 지 결정함.
- 현재 사용 중인 디바이스에 노티를 보여줌. (둘 다 사용 안하고 있으면 워치에 보여줌)
- ### Short Look
  - 노티가 와서 사용자가 손목을 들어서 보면 노티를 요약해서 보여줌 (`Short Look`)
  - 사용자가 몇 초간 응시하고 있으면 디테일한 버전인 `Long Look`을 보여줌.
- ### Long Look
  - Long Look은 스크롤 가능하고 커스터마이징 가능한 노티임.
  - Long Look은 네가지 커스텀 액션을 보여줄 수 있으며, 아이폰을 통해 등록 해야함
  - Dismiss 버튼은 항상 보여줌.

## Creating a custom notification
- ### Static Notification
  - 스토리보드에서 노티피케이션 화면 생성 가능. 노티 종류마다 다른 씬을 생성해줘야 함.
  - 다이나믹 노티가 작동 안 할 때를 대비해서 스태틱 노티는 중요함.
  - 스태틱 노티는 마치 런치스크린 or StatelessWidget과 같아서 화면을 갱신하는 코드를 돌릴 수 없음.
  - `notificationAlertLabel` 만 아울렛으로 연결하여 변경할 수 있음. 시스템이 노티 데이터를 통해 자동으로 셋팅.
- ### Dynamic Notification
  - 스토리보드에서 스태틱 노티 씬을 누르고 `Has Dynamic Interface`를 체크하면 자동으로 다이나믹 노티 씬이 생성됨.
  - 코드를 통해 다이나믹하게 화면 갱신 가능.
  
