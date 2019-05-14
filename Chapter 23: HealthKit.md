# Chapter 23: HealthKit

- watchOS에서는 건강 앱처럼 HealthKit을 지원하는 앱을 만들 수 있다.
- HealthKit을 통해 건강과 관련된 거의 모든 데이터에 접근하고 추적할 수 있다.


## Getting Started
- watchOS 4부터 HealthKit에는 다음 기능들이 추가됨.
  - workout session을 생성할 수 있음. 센서 데이터를 받아오고 포그라운드에서 계속 돌 수 있는 모드로 만들어 줌.
  - iOS와 같은 API 인터페이스
  - iOS와 워치간의 심레스한 데이터 싱크
  - iOS 건강 앱에 데이터를 더할 수 있음.
  - 운동 데이터를 백그라운드에서 수집 가능.
  
- HealthKit을 사용하려면 HealthKit entitlement를 제공해야함.

## Asking for permission
- `HealthDataService().authorizeHealthKitAccess`를 통해서 HealthKit 데이터의 읽고쓰기 권한 획득.

## Creating workout sessions
- HKWorkoutSession을 시작하면 워치를 워크아웃 모드로 만듬.
- 디지털 크라운을 눌러서 앱을 종료하기 전까지 앱이 포그라운드에 머무름.
- 심박수나 거리와 같은 추가적인 센서 데이터를 받을 수 있음.
- 백그라운드에서 운동 데이터를 계속 수집하도록 설정할 수도 있음.

## Saving a workout
- `HKHealthStore.save()`를 사용해서 HKWorkout 객체를 저장함.

## Displaying data while working out
- `HKAnchoredObjectQuery`를 사용하면 세션 중에도 데이터를 받아올 수 있음.
