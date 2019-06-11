# Chapter 27: Accessibility

- 신체가 불편한 사람들을 위해 VoiceOver, Switch Control, Assistive Touch 등의 기능들이 있음.

## Assistive technology overview
- #### Voice Over
  - 시각 장애우들을 위한 기능. 사용자의 손가락 밑에 어떤 컨텐츠가 있는지 읽어 줌.
- #### Zoom
  - 두 손가락으로 스크린 전체를 확대하거나 축소할 수 있음.
- #### Extra-large Watch Face
  - 워치 페이스를 엄청 크게 보여줄 수 있음.

## WatchKit Accessibility API overview
- `WKInterfaceObject`를 상속받는 엘리먼트들은 모두 접근성 관련 메소드가 있음.
- `setIsAccessibilityElement(_:)` 메소드로 접근성 엘리먼트임을 표시함.
  - 접근성 엘리먼트는 VoiceOver가 활성화 되었을 때 스와이프 하거나 더블탭 하는 엘리먼트를 뜻함.
  - 대부분의 엘리먼트들은 기본적으로 접근성 엘리먼트이지만, 이미지나 그룹 엘리먼트의 경우 접근성 여부를 셋팅해줘야함.
- `setAccessibilityLabel(_:)` 메소드로 엘리먼트가 텍스트 정보를 가지고 있음을 표시함.
  - 라벨이 아닌 엘리먼트에도 라벨을 설정할 수 있음.
- `setAccessibilityValue(_:)`로 인터랙티브하게 값이 바뀌는 엘리먼트에 대응 가능.
- `setAccessibilityHint(_:)` 메소드로 어떻게 엘리먼트를 사용하는지 설명 가능.
- `setAccessibilityImageRegions(_:)` 메소드로 이미지를 구역별로 쪼개어 설명 가능.
- `WKAccessibilityIsVoiceOverRunning()`와 같은 글로벌 함수로 접근성 상태 확인 가능.
- 커스텀 엘리먼트들은 `setAccessibilityTraits(_:)`를 사용하여 어떤 성격의 접근성 엘리먼트인지 설정 가능.


