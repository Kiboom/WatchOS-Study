# Layout

- WatchKit에서는 Constraint 대신 콘텐츠 사이즈와 간격으로 레이아웃 함.

## Understanding layout in WatchKit
- ### Layout Groups
  - 인터페이스 오브젝트를 묶는 역할.
  - `WKInterfaceObject`를 상속받기 때문에 인터페이스 오브젝트처럼 배경이나 Corner Radius 값 등을 설정할 수 있음.
  - #### Layout
    - 그룹 내 레이아웃의 방향을 가로나 세로로 설정할 수 있음.
  - #### Insets
   - 그룹 내 컨텐츠와의 패딩값
   - 애플 워치 스크린에 자체 패딩이 있기 때문에 인터페이스 요소들은 스크린 모서리에 딱 붙이는게 권장사항. 
   - 하지만 컨텐츠를 중앙 정렬하고 싶으면 Inset 값을 더 주면 됨.
  - #### Spacing
    - 그룹 내의 요소들 간의 간격

- ### Content Size
  - 그룹 내 컨텐츠의 종합 사이즈
  - WatchKit에서는 모든 레이아웃을 자동으로 처리해줌.
  - SizeToFitContents를 설정하면 컨텐츠 사이즈가 자동 계산됨.
  
- ### Relative Spacing
  - 부모 뷰의 크기와 위치에 대해 상대적인 크기와 위치를 가질 수 있음.

## Laying it all out
## Collecting Metadata
## Laying out buttons
- Relative Spacing을 사용하여 버튼 두개를 레이아웃
## Dynamic Layouts
- 버튼을 눌렀을 때 collapsedCommentLabel을 expandedCommentLabel로 바꿔치기.
## Auto Rotating
- `WKExtension.shared().isAutorotating = true` 를 사용하여 회전 가능하게 하기.
