# Chapter 20: Advanced Complications

- 컴플리케이션의 시간여행 기능을 알아볼 것

## Traveling Through Time
- ### How Time Travel Works
  - 타임라인 엔트리 데이터를 넘기면 사용자가 디지털 크라운으로 선택한 시간에 맞는 데이터를 보여줌
  - ClockKit에서는 (PickerView처럼) forward와 backward를 설정할 수 있음.
  
- ### Providing the Data
  - `getTimelineStartDate`와 `getTimelineEndDate`라는 메소드를 통해 과거와 미래 데이터를 전달할 수 있음.

- ### Animating Through TIme
  - 시간을 이동할 때 트랜지션 효과를 줄 수 있음.
  - None: 애니메이션 없음
  - Always: 모든 변화에 대해 트랜지션 효과 줌
  - Grouped: 타임라인 엔트리 내의 특정 그룹에만 애니메이션을 줄 수 있음.
  
## Keep your data current
- ClockKit은 몇몇 API를 통해 데이터를 추가 제공하거나 invalidate 시킬 수 있음.
- 또한 언제 앱을 꺠워서 데이터를 더 받아올 지 설정할 수 있음.
- 또한 푸시 노티를 통해 컴플리케이션을 업데이트 할 수 있음.

- ### Budgeting your time
  - 시스템에서는 각 컴플리케이션에 time budget을 부여하여 할당받은 시간 내에 업데이트를 하도록 함.
- ### Scheduled Update
  - 컴플리케이션 업데이트를 위해 업데이트를 예약할 수 있음.
  - 기존의 데이터를 무효화 하려면 `reloadTimeline(for:)`를 실행
  - 새로운 데이터를 추가 하려면 `extendTimeline(for:)`를 실행
  - 새로운 데이터가 없으면 메소드 호출이 없음.
- ### Updating from the Watch app
  - 워치 앱을 열었을 때 시스템에 컴플리케이션을 업데이트 하도록 요청할 수 있음.
- ### Updating from the iPhone app
  - 아이폰 앱을 통하여 컴플리케이션 업데이트 가능
- ### Updating from a server
  - 푸시 노티를 통하여 컴플리케이션 업데이트 가능


## Privacy in complications
  - `getPrivacyBehavior()` 메소드를 통해 민감정보를 보호할 수 있음.
