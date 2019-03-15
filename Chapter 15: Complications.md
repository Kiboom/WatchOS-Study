
# Chapter 15: Complication
- watchOS에서 컴플리케이션은 점점 더 중요해지고 있음. 
- 모든 앱은 하나 이상의 컴플리케이션을 포함해야 함.

## A new category of interaction
- 컴플리케이션이 활성화된 상태에서는 아래와 같은 장점이 있음.
  - 메모리에 앱을 유지하고 업데이트를 시키므로 런치 속도가 엄청 빠름.
  - 하루에 50번의 푸쉬를 받을 수 있음.
  - Apple Watch Face Gallery에서 컴플리케이션이 보여짐
  
- ClockKit을 사용하여 컴플리케이션을 개발하게 됨.

## Adding a complication
- Watch Kit App Extension 타겟에서 Complication Configuration을 설정함.
- 데이터 소스 클래스와 패밀리 지원, 컴플리케이션 그룹 등을 설정할 수 있음.

## Creating the data source
- `NSObject`와 `CLKComplicationDataSource`를 충족하는 클래스를 데이터소스 클래스로 삼을 수 있음.
- 데이터 소스의 역할은 컴플리케이션에 쓰일 데이터를 템플릿으로 패키징해주는 역할을 함.
- 컴플리케이션은 손목을 들었을 때 바로 데이터를 확인할 수 있어야 하므로, 데이터 소스는 최대한 빨리 반응해야함.
  - 따라서 오래 걸리는 네트워킹이나 연산을 하면 안됨. 이미 있는 데이터를 패키징만 해줘야.
  
## Launching from a complication
- Handoff API로 `handleUserActivity(_:)`를 사용하면 컴플리케이션으로 앱을 런칭했는지 알 수 있음.

## Complication templates
- 컴플리케이션 템플릿은 데이터 타입과 데이터의 시각적 정렬을 정의함.
- 컴플리케이션 패밀리마다 여러 템플릿을 가질 수 있음.

## Data providers
- 템플릿은 데이터를 직접 받지 않고 `Provider`로 래핑해서 받음.
- 텍스트나 이미지나 시간 등의 정보를 Provider를 통해서 래핑하면 시스템이 알아서 포맷팅해줌.

## Timeline entries
- `getCurrentTimelineEntry(for:, withHandler:)’를 구현하면 특정 시간에 특정 템플릿을 제공할 수 있음.
