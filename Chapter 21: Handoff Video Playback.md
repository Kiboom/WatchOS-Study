# Chapter 21: Handoff Video Playback

- 멀티미디어 파일 재생과 커스텀 UI, 그리고 Handoff에 대해 배워볼 것

## Playing Video
- 동영상 재생을 위한 가장 간편한 방법은 WKInterfaceController에서 `presentMediaPlayerController(with:options:completion:)`를 실행하는 것.
- remote content URL도 재생 가능함.
- 여러 Playback options를 설정할 수 있음.

## Making custom interface
- 커스텀 UI를 위해서는 `WKInterfaceMovie`와 `WKInterfaceInlineMovie` 두가지 옵션이 있음.
- 둘 다 거의 비슷한데 후자가 더 커스텀 UI 생성에는 플렉서블함.

## Handoff
- 핸드오프는 아이폰과 워치 사이의 seamless한 작업 교환을 뜻함.
- iCloud 계정과 Bluetooth 4.0, iCloud 페어링이 필요함.

## Configuring activity types
- Info.plist에서 작업 타입명을 설정함.

## User Activities
- 핸드오프는 User Activity라는 개념을 바탕으로 하고 있음.
- Handoff는 NSUserActivity라는 패키지화된 정보로 작업 상태를 저장하고 전달함.

