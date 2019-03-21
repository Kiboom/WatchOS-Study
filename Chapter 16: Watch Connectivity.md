# Chapter 16: Watch Connectivity

- iPhone과 Apple Watch 간의 통신은 사용자 경험에 있어서 중요함.
- watchOS 2부터 더 풍부한 통신이 가능하도록 `WatchConnectivity` 라는 프레임워크가 생김.

## Setting up Watch Connectivity
- 통신을 위해서는 각 기기의 AppDelegate에서 `WCSessionDelegate`를 사용하여 Connectivity Session을 설정해야함.
- ### WCSessionDelegate
  - `sessionDidBecomeInactive(_ session: WCSession)`: 사용자가 다른 애플 워치로 연결을 변경했을 때 호출됨. 전송됐지만 삭제 처리되지 않은 데이터들을 정리할 수 있음.
  - `sessionDidDeactivate(_ session: WCSession)`: 더이상 보낼 데이터가 없을 때 세션을 종료함. 다른 워치에 연결해서 새로운 세션을 시작하려면 여기서 activate 해줘야함.
  - ‘session(_ session: WCSession, activationDidCompleteWith activationState: WCSessionActivationState, error: Error?)’ 메소드는 세션 activation이 끝났을 때 호출됨.
- WCSession은 싱글톤임. 한 앱에서 하나의 세션만 가질 수 있음.
- ### Watch Connectivity setup
  - Watch 앱에서도 iPhone과 같이 `WCSessionDelegate`를 설정해주면 됨.
  
## Device-to-device communication
- ### Interactive messaging
  - iPhone과 Watch가 둘 다 활성화 되어있을 때 인터랙티브 메시지로 즉각 전송됨.
  - 베스트 시나리오지만, 둘 다 활성화 되어있을 일은 별로 없기 때문에 Background Transfer도 고려할 것.
  
- ### Background transfer
- 두 기기 중 하나만 활성화 되어있을 때는 백그라운드에서 데이터를 보낼 수 있음.
- 배터리 상태와 전송 대기 상태를 고려해서 최적의 시간에 데이터를 전송함.
  - #### User info transfers
    - FIFO 방식으로 데이터를 전송함.
    - 딕셔너리의 형태로 전송함.

  - #### File Transfer 
    - 로컬 파일이나 옵셔널 딕셔너리를 전달할 수 있음.
    - User info transfer처럼 백그라운드에서 큐에 저장됨.
  
  - ### Application context transfer
    - User info transfer처럼 딕셔너리를 전달할 수 있음. 
    - 차이점은 context를 전달하기 때문에 항상 최신 데이터를 전송함.
    - 딕셔너리에는 Property List에 부합하는 타입만 넣을 수 있음.
 
