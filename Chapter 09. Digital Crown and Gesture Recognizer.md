# Chapter 09. Digital Crown and Gesture Recognizer

- Apple Watch 에서는 멀티터치를 제외한 모든 제스처를 사용할 수 있음.
- 제스처 외에도 디지털 크라운을 통해 UI 컨트롤 가능.

## Listening to the Digital Crown
- 디지털 크라운의 변화를 감지하려면 `WKCrownDelegate` 프로토콜을 구현해야 함.
- `crowDidRotate`: 
  - 유저가 디지털 크라운을 돌릴 때마다 호출됨.
  - rotation 값은 0-1
- `crownDidBecomeIdle`: 
  - 디지털 크라운 회전이 멈췄을 때 호출됨.

- WKInterfaceController에는 `crownSequencer`속성이 있음. 
- `crownSequencer.focus()`를 호출하면 디지털크라운으로부터 정보를 받아올 수 있음.

- ### Adding the Move Interaction
  - `move`모드에서는 디지털 크라운 회전 값을 offset 값으로 변환
- ### Adding the Zoom Interaction
  - `zoom`모드에서는 디지털 크라운 회전 값을 zoom 값으로 변환
- ### Adding the Inspect Interaction
  - `move`모드에서는 디지털 크라운 회전 값의 delta를 통해 방향을 판단하여 인덱스를 증감함.
  
## Gestures
- Force Touch Menu를 추가하여 모드를 설정할 수 있도록 함.
- ### Adding the Tab Gesture Recognizer
  - iOS와는 달리 제스처 인식기는 Interface 전체에 걸 수 없고 특정 오브젝트에만 연결 가능.
- ### Adding the Pan Gesture Recognizer
  - `locationInObject()`를 통해 터치 좌표의 이동을 파악함.

    
  
  
