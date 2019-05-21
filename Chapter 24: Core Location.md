# Core Location
- 디바이스의 현재 위치를 알게 해주는 프레임워크
- 아이폰 기기가 근처에 없어도 사용 가능

## Getting Started
- ### Getting Location
  - `When in use`와 `Always` 두 옵션으로 나뉨
  - Info.plist에 사용 목적 명시
  
- ### Requesting user authorization
  - `CLLocationManager`를 사용하여 권한 상태 파악
  - `.notDetermined`, `.restricted`, `.denied`, `.authrizedAlways`, `.authorizedWhenInUse` 다섯 가지로 상태가 나뉨.
  - delegate를 설정하여 권한 상태 변경 감지

- ### Using the location
  - 로케이션 매지너의 `requestLocation()` 를 사용하여 위치 데이터 받아옴

- ### Handling location errors
  - `locationManager(manager:didFailWithError:)`를 사용하여 에러 처리
  
- ### Limiting location queries
  - 아이폰이 연결 안되어있을 때는 Accuracy 값을 `kCLLocationAccuracyHundredMeters`로 설정하는 것이 적당함.

## Coordination
- watchOS에서는 위치정보를 계속 받아올 수 없으며 백그라운드 모드에서 위치정보 업데이트도 안됨.
- 따라서 아이폰과 연결하여 아이폰이 백그라운드에서 받아온 위치정보를 공유받는 것이 더 빠르고 효율적으로 변화를 감지할 수 있음.
- ### Background location updates
  - 타겟 설정에서 Background Mode를 켜기
  - iOS9부터는 로케이션 매니저의 `allowsBackgroundLocationUpdates` 값을 true로 설정해야함.

## Optimization
- 로케이션 매니저의 `allowDeferredLocationUpdatesUntilTraveled(_:timeout:)`를 사용하면 배터리 사용을 최적화 할 수 있음.
- 특정 조건에 맞을 때까지 위치정보를 캐싱하게 됨.
  
  
