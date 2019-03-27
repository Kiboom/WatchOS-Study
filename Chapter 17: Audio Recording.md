# Chapter 17: Audio Recording

- watch OS2 부터 멀티미티어 파일의 녹음과 재생 기능이 추가됨.

## Audio Playback
- watchOS에서 오디오를 재생하는 방법에는 2가지가 있음
  - 빌트인 미디어 플레이어
    - `presentMediaPlayerController(with:options:completion:)’ 메소드를 사용
    - url을 넘기면 음원을 재생하는 컨트롤러가 등장
  - 커스텀 미디어 플레이어
  
## Building an audio Player
- 빌트인 미디어 플레이어는 심플하고 좋지만, 플레이어를 끄면 재생이 멈춘다는 문제가 있음.
- 이 문제를 해결하려면 플레이어를 직접 만들면 됨.
- `WKAudioFilePlayer`를 사용하여 오디오를 재생하면 블루투스 헤드폰이나 실제기기에서만 소리가 나옴.
- `WKAudioFilePlayer`에 `WKAudioFilePlayerItem`을 넣어서 소리를 재생함.

## Background audio playback
- 백그라운드 재생을 위해서는 Info.plist에서 `Required Background Modes`를 입력해야함.


## Recording an audio
- watchOS 4부터 Unified Process Runtime 덕분에 Watch App과 WatchKit Extension 사이에 단일 샌드박스에 접근할 수 있게 됨.
