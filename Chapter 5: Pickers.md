# Chapter 5: Pickers

- 초창기 WatchKit에는 디지털 크라운과 직접 연동되는 UI 요소가 별로 없었음.
  - 디지털 크라운의 장점은 스크린을 직접 터치하지 않고도 화면을 조작할 수 있다는 점.
  - 즉, 손가락으로 화면을 가릴 일이 없음. 더 많은 정보를 보여줄 수 있게 됨.
  - 태생적으로 작은 화면을 가진 Watch에게 있어서 정말 유용한 기능.
- watchOS2 부터 `WKInterfacePicker`가 처음 나왔는데, iOS의 `UIPickerView`와 동일한 역할을 함.
- `WKInterfacePicker`의 장점은 스크린을 직접 터치하지 않고도 디지털 크라운을 사용하여 아이템을 선택할 수 있음.
- 이전 챕터에서 만들었던 프로젝트의 UI들을 WKInterfacePicker로 교체해보는 작업을 해볼 것.

## Getting Started
- 이전 챕터의 프로젝트에서 타이머를 제외한 모든 UI와 관련 코드들을 제거함.
- 직접 화면을 터치하지 않고도 UI를 조작할 수 있는 `WKInterfacePicker`로 대체할 예정.

## Picker display styles
- `WKInterfacePicker`에는 세 가지 종류가 있음. 각각의 특성에 맞게 선택해서 사용하면 됨.
- ### The list style
  - 우리가 iOS에서 익히 봐왔던 전통적인 Picker 모양.
  - 기존의 UIPickerView 에서는 텍스트 기반의 피커뷰였고, 이미지를 넣으려면 별도의 UIView를 만들어서 넘겨줘야 했는데,
  - `WKInterfacePicker` 에서는 텍스트와 이미지 둘 다 쉽게 넣을 수 있게 됨.
- ### The stacked style
  - 풀스크린의 이미지를 보여주기 위한 Picker임.
  - Picker를 스크롤하면 마치 카드 스택을 넘기는 것 같은 효과를 줄 수 있음.
  - 사진 앨범이나 카드 게임 같은 거에 쓰면 좋을 듯.
  - list style 와는 달리 풀스크린 피커뷰이기 때문에 이전 아이템이 피커뷰에서 보이지 않음.
  - 이미지를 보여주기 위한 Picker이기 때문에 텍스트를 보여줄 수 없음. 텍스트를 넣으면 빈 화면이 나옴.
- ### The sequence style
  - stacked style과 거의 비슷한데, Picker를 스크롤 할 때 애니메이션 효과가 없음.
  - 트랜지션 효과 없이 이미지만 착착착 바꾸는 방식.
  - 스크롤하면 이미지를 연달아서 주루룩 보여주기 때문에 애니메이션처럼 보일 수 있음.
  - 피커뷰를 스크롤했을 때 각 단계별로 이미지가 조금씩 바뀌는 효과를 주고 싶을 때 유용함.
  
## Your first picker
- 기존의 프로젝트를 피커뷰 기반으로 바꿔볼 것
- `WKInterfacePicker`는 스토리보드에서만 생성 가능하고 관련된 속성도 스토리보드에서만 설정 가능함. 런타임 중에는 변경 불가.
- 대신 피커에 들어가는 아이템들은 반드시 코드로만 작성해서 넣어줘야 함.
- `WKPickerItem`을 사용하여 피커의 아이템을 설정할 수 있음.
- 피커를 스크롤하려면 먼저 탭해야 함.

## A sequence-style picker
- list style 과 거의 비슷함. 다만 `WKPickerItem`에서 text 대신 contentImage를 설정해주면 됨.
- 그래픽 처리 능력이 부족한 워치를 위해, 이미지는 가능한 최적화해줘야 함. 여기서는 배경을 까맣게 칠해서 불필요한 투명도를 없앰.
