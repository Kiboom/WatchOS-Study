# Chapter 1: Hello, Apple Watch!

## Getting started
- iPhone 앱 `view controllers` 를 쓴다면, Watch 앱은 `interface controllers` 를 사용한다.
- WatchKit App을 Target으로 추가하면 `WatchKit App` 폴더와 `WatchKit App Extension` 폴더가 생김.
- 각각 `Interface.storyboard`와 `InterfaceController.swift` 파일이 들어있음.

## Hello, World!
- Watch용 스토리보드에서는 Size Inspector 탭이 없다.
- Property Inspector 탭의 Alignment와 Size 섹션에서 크기와 위치를 조정한다.

## Setting label tet in code
- `willActivate()` 메소드에서 라벨 텍스트를 셋팅한다.

## Emoji!
- 라벨의 Font를 System - System으로 바꾸면 조정할수 있음.

## Casting emoji fortunes
- iPhone 앱 타겟과 공유하고 싶은 코드 파일은 `Target Membership`에서 `WatchKit App Extension` 을 선택해준다.

## Refreshing the fortune
- Label을 Button으로 교체한다.
- Height를 `Relative to Container`를 선택하면 스크린 높이를 꽉 채운다. 계수를 조정하면 스크린 높이에 비례해서 설정됨.
- `WatchKit App` 폴더의 Asset에 + 버튼을 눌러서 Image Set을 추가한다.
- 해당 에셋의 Attribute Inspector에서 Devices를`Apple Watch`로 선택해주고, 
- Screen Width를 `Individual Widths`로 바꿔주면 스크린 사이즈마다 다른 이미지를 넣을 수 있다.
