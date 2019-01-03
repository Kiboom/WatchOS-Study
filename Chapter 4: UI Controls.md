# Chapter 04: UI Control

- 대부분의 WKInterfaceObject는 UIKit에도 있는 뷰이지만, 몇몇은 WatchKit에만 있는 애들이다.

## The timer object
- `Group`은 인터페이스 객체들을 쉽게 정렬하기 위해 고안된 클래스
- `Timer`를 사용하면 DateFormatter를 사용하지 않고도 쉽게 날짜와 시간을 보여줄 수 있다.

- ### Wiring Timer
  - 타이머를 작동시킬 시작버튼을 생성함.
  - `Timer`는 Date 객체를 인자로 받아서 시간을 설정한다.
  
## Using a label and buttons to control weight
  - `spacing` 속성을 조정하여 Group 내의 요소 간의 간격을 조절할 수 있음.

## Using a slider object to control doneness
  - `Slider`를 사용하여 굽기 정도를 조절할 수 있게 함.

## Integrating the timer
  - `timerRunning` 플래그를 사용하여 버튼을 눌렀을 때 타이머를 시작하거나 멈추게 함.

## Interacting with scrolling
  - `interfaceDidScrollToTop()`, `interfaceOffsetDidScrollToTop()`, `interfaceOffsetDidScrollToBottom()` 세 가지 메소드를 사용하여 화면의 스크롤 위치를 감지할 수 있음.
  
## Using the switch to change units
  - `Switch`를 사용하여 메트릭 시스템 사용 여부를 정할 수 있게 함.
  
 
