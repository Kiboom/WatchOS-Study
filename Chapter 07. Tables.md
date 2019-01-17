# Chapter 07. Tables

## Tables in WatchKit
- WatchKit의 테이블 클래스에는 섹션 개념이 없다.
- UIKit처럼 dataSource나 delegate를 구현할 필요가 없다.

## Getting Started
- `WKInterfaceTable`은 사실 그룹 인터페이스이다.
- 그룹 인터페이스이기 때문에 내부 컨텐츠 사이즈에 따라 높이가 자동 조정될 수 있다.
- ### Controlling each row
   - 각각의 행은 row controller 라는 NSObject 클래스로 설정해야 함.
   - UITableView 와는 달리 WKInterfaceTable은 datasource 없이 rowController를 직접 설정함.

## Getting Directions
- `contextForSegue`를 통해 navigating을 설정할 수 있음.
- `table.setRowTypes`를 사용하면 각 행마다 다른 타입의 row controller를 할당할 수 있음.

## Creating multiple sections
- WKInterfaceTable에서는 중첩된 데이터 타입을 넣을 수 없음.
- 다중 섹션을 구현하려면 여러 타입의 row controller를 생성하여 섹션 헤더를 만들어야 함.
