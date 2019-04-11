# Chapter 19: Advanced Watch Connectivity

- userInfo 모드를 사용하여 앱 간에 데이터를 전송할 것임.
- Application Context Transfer와 비슷하지만, 최근 하나만 보내는 것이 아닌 전체 데이터를 보낼 수 있음.

## User info transfers
- User info transfer는 iOS와 watch앱 간에 데이터를 전송하는 것.
- FIFO로 데이터가 누적되어 전송됨.
- 한 번 전송이 시작되면 WCSession이 데이터 전송을 보장함. 즉, 보내는 쪽 앱이 더이상 동작하지 않더라도 계속 전송이 진행됨.
- `transferUserInfo(_:)`와 `session(:)` 델리게이트 메소드가 서로 쌍을 이뤄서 동작함.


## Interactive messaging
- 두 앱이 모두 활성화 되어있을 때 실시간으로 메시지를 주고받을 수 있는 세션을 생성할 수 있음.
- iPhone 앱은 Foreground에 없어도 메시지를 주고받을 수 있음.
