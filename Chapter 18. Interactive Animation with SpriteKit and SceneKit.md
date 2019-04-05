# Interactive Animation with SpriteKit and SceneKit

- SpriteKit과 SceneKit은 2D, 3D 게임 개발을 위한 프레임워크
- 게임 용도 뿐만 아니라 인터랙션에도 사용 가능

## Introducing SpriteKit and SceneKit
- UIKit과 SpriteKit과 SceneKit의 좌표계는 각각 다름
- UIKit의 기본 요소는 `view`이고, SpriteKit과 SceneKit의 기본 요소는 `node`임
- ### Nodes
  - UIKit과는 다르게 SpriteKit과 SceneKit에서 노드의 좌표는 좌상단이 아닌 중앙값임.
- ### Scenes
  - 스토리보드의 Scene과 비슷한 개념. 
  - Scene에는 화면에 표시될 모든 노드들을 포함함.
- ### Actions
  - 노드에 붙은 애니메이션
  - `node.run(action)`을 통해 호출함.
  - 스토리보드에서 편집할 수 있음. 코드에서도 편집 가능.
- ### Physics
  - 노드는 그저 화면에 표시되는 모양일 뿐임. 여기에 물리적 효과를 줄 수 있음.
  - Particle Generator를 통해 입자들이 날아다니는 효과를 줄 수 있음.


## Migrating From iOS
- ### Graphic Renderings
  - iOS와 watchOS의 아키텍처가 다르기 때문에 iOS에서 사용했던 몇몇 기능들은 watchOS에서 사용이 제한됨.
- Scene 파일을 watchOS 타겟과 공유.
- Gesture Recognizer를 통해 물리 효과를 제어 가능
- iOS와 watchOS의 디바이스 방향 문제 때문에 별도의 변환 코드가 필요.

## SceneKit
- 3D 그래픽을 보여주기 위한 프레임워크
- `SCNScene`을 상속받은 3D 그래픽 씬을 만들고 3D 오브젝트 노드와 카메라를 설정함.
