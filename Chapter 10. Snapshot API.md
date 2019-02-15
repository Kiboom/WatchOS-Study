## The Dock
- 독은 앱들을 미니어처처럼 카드 형식으로 보여준다.
- 앱을 나가면 시스템은 앱의 스냅샷을 떠서 독에서 보여준다.

## Snapshot API
- 스냅샷이 최신 상태를 반영할 수 있도록 잘 설계해야 한다.

- ### Snapshot Tips
  - 스냅샷은 작은 형태로 보이기 때문에 폰트 굵기 등의 UI를 최적화해야함.
  - 중요한 정보들만 강조해서 보여주기.
  - 진행상황이나 성공여부 화면을 보여주면 효과적임.
  - 스냅샷은 앱의 런치스크린이자 프리뷰 이미지라는 것을 기억할 것.
  - 스냅샷을 바꾸더라도 사용자가 예측가능하고 논리적인 형태로 바꿀 것.
  - 사용 시나리오의 타임라인을 염두에 두고 스냅샷을 구성할 것.
  - 사용자의 특성에 맞게 스냅샷을 커스터마이징하여 보여줄 것.

- ### 시스템
  - 최소 한 시간에 한 번은 시스템이 독에 있는 앱들의 스냅샷을 업데이트 해줌.
  
- ### Refresh lifecycle
  - `scheduleSnapshotRefresh(withPreferredDate:userInfo:scheduledCompletion:)` 메소드를 사용하면 새로운 스냅샷 촬영을 예약할 수 있음.
  - 시스템이 앱을 깨워서 스냅샷을 촬영할 때 아래와 같은 순서로 메소드가 호출됨. 각 단계에서 스냅샷의 생김새를 정할 수 있음.
    - 1) The root interface controller's awake(withContext:) method
    - 2) The root interface controller's willActivate() method
    - 3) The extension delegate's handle(_:) method
  - `setTaskCompleted(restoredDefaultState:estimatedSnapshotExpiration:userInfo:)` 메소드를 호출하면 시스템이 스냅샷을 갱신
  - 스냅샷을 예약하고 일정 시간내에 종료를 해야함. 네트워킹 작업과 같은 무거운 작업은 지양할 것.
  
## Working with snapshots
- `handle(:)` 델리게이트 메소드에서 `WKRefreshBackgroundTask` 작업들을 핸들링 할 수 있음.
- 시뮬레이터에서 시계 화면으로 돌아간 상태에서 Xcode의 `Debug\Simulate UI Snapshot` 기능을 실행하면 스냅샷을 시뮬레이팅 할 수 있음.
