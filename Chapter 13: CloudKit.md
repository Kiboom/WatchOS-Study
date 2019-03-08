# Chapter 13. CloudKit
- CloudKit은 watchOS1 때 생겼다가 2에서 없어졌다가 3에서 다시 생김.
- 배터리 소모를 줄이기 위해 아이폰과 통신하며, 아이폰이 없을 때는 와이파이로 연결.

## Getting Started
- Info.plist에서 `WKCompanionAppBundleIdentifier`에 유니크한 앱 아이디 적어주기.
- `Cloud Dashboard`에서 레코드 상황 확인 가능.

## CloudKit: an aerial view
- ### 클라우드 킷의 장점
  - 모든 디바이스에서 동기화 가능. 넉넉한 무료 공간과 네트워크 환경을 제공.
  - 사용자 인증에서 자유로움.
  - 애플에서 개발자의 요구를 받아들여 CloudKit을 발전시키는 중.

- ### Container, database, zone
  - 앱마다 iCloud 서버에 `Container`가 생김.
  - 컨테이너 안에는 public database와 private database, shared database가 있음.
  - zone을 사용하여 사용자끼리 묶을 수 있음.

- ### Operation vs convenience API
  - convenience API를 통해 단일 레코드에 대한 작업과 여러 batch processing 작업들을 처리할 수 있음.
  - CKOperation은 Operation의 하위 클래스로서, 디펜던시와 우선순위 설정, 서비스 품질 설정, 특정 키 페치, 작업 취소 등을 할 수 있음.
  
- ### Getting notifications of changes to a database
  - `CKDatabaseSubscription` 객체를 구독함으로써 서버와 동기화 가능.
  - 애플에서는 사일런트 노티를 권장함.
  - 만약 사용자가 노티를 허용 안한다면, 변경사항을 수동으로 땡겨오도록 해야 함.

- ### Fetching and handling changes to a database
  - 
  
## Watch app vs iOS app
  - CloudKit과 연결하는 클래스를 iOS app과 Watch app이 공유하도록 설정.
