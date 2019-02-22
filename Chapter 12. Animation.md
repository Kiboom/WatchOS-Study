# Chapter 12. Animation

## Animation Overview
- WatchKit에는 아래 세가지 종류의 애니메이션이 있다.
- ### Implicit Animation
  - 테이블에는 행 삽입 삭제 애니메이션 메소드가 기본 내장되어 있음.
  - InterfaceController 에는 스크롤 애니메이션 메소드가 기본 내장되어 있음.
- ### Property Animation
  - UIKit처럼 `animate()` 메소드를 사용해서 특정 프로퍼티에 애니메이션 걸 수 있다.
  - 투명도, 크기, 위치, 색상 값에 애니메이션 걸 수 있음.
  - WKInterfaceGroup의 경우 Content Inset에도 애니메이션 적용 가능.
- ### Animated Images
  - 여러 이미지를 묶어서 재생하는 애니메이션.
  - WKImageAnimatable 프로토콜을 구현하고 있는 뷰 위에서 실행 가능.
  - WKInterfaceGroup, WKInterfaceButton, WKInterfaceImage에서 실행 가능.

## Animated images: a paradox?
- 애니메이션 이미지도 **이미지**다.
- 애니메이션 이미지도 일반 이미지처럼 취급 가능하다. 예를 들어 높이 조절 애니메이션을 줄 수도 있다.
- 애니메이션 걸 이미지 파일들에 같은 이름을 부여하고 접미사에만 숫자를 다르게 주면 됨. 그런 다음 WKInterfaceImage의 `setImageNamed`메소드를 사용하면 됨.
