# Chapter 08. Navigation

WatchKit의 네비게이션은 네가지 컨셉을 가지고 있음.
- Hierarchical
- Page-based
- Modal
- Menu

WatchKit의 네비게이션 기능은 제한적이어서 모달을 제외하고는 다른 네비게이션과 조합이 불가능.

## Getting around in WatchKit

- ### Hierarchical Navigation
  - 네비게이션 스택에 쌓는 역할을 함.
  - 스토리보드에서 Control-drag를 하거나 `pushController(withName:context:)`를 사용하면 푸쉬할 수 있음.
  - `context` 파라미터를 통해 이전 화면에서 다음 화면으로 데이터 전달 가능

- ### Page-based Navigation
  - WKInterfaceController의 그룹
  - 각각의 페이지는 독립된 정보와 기능을 담고 있음.
  - 따라서 Hierarchical 과는 다르게 페이지간에 데이터를 주고 받을 수 없음.

- ### Modal Navigation
  - Modal present 효과로 뷰컨트롤러가 나오게 함.
  - 빌트인 cancel 버튼이 있음.
  - 모달을 띄울 때 context 전달 가능.
  - 다른 타입의 네비게이션을 모달로 보여줄 수 있음.

- ### Menus
  - 포스 터치 했을 때 나오는 메뉴
  - 뷰컨트롤러 스토리보드에 Menus 요소를 추가하면 설정 가능함.

## Getting Started
- ### A modally-presented, paged-based palette
  - `presentController(withNamesAndContexts:)`를 사용하면 페이지 컨트롤러를 모달로 띄울 수 있음.
  - `willActive()` 메소드는 `viewWillAppear()` 와 같은 기능을 함.

- ### Pushing a Child Controller
- ### Using Menus
  - 스토리보드에 메뉴 요소를 추가하더라도 시각적으로 보이는 건 없음. 
  - 다만 컨트롤러의 IBAction에 연결하면, 해당 컨트롤러를 포스터치 했을 때 메뉴가 보여짐.
