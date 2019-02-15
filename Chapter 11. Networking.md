# Networking
- watchOS 2부터  URLSession을 사용하여 네트워킹을 하게 되어 훨씬 쉬워짐.
- (아이폰과 연결이 안 돼있어도) 애플 워치가 와이파이를 통해 아이폰에게 네트워킹을 요청할 수 있음.


## Getting Started
- ### URLSession 요약
  - URLSession을 사용하면 async하게 네트워킹이 가능함.
  - foreground와 background 네트워킹도 가능함.
  - data, download, upload 세가지 타입의 네트워킹 태스크를 실행 가능.


## Calling the web service
- `PopulationService` 클래스에서 `getRankInCountry`를 호출하여 데이터 페치.
- 받아온 data를 decoder를 사용하여 파싱.
- Info.plist의 `App Transport Security` 를 설정하여 http 통신도 가능하도록 설정.

(이하 UI 구현 코드이므로 생략)
