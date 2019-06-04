# CHAPTER 26: LOCALIZATION
- 국제적으로 성장하려면 에버노트처럼 여러 지역과 국가들의 언어와 포맷에 대응해야함.

## INTERNATIONALIZING YOUR APP
- ### Internationalization
  - 스토리보드나 코드 내의 문자열들을 외부로 꺼내어 외부에서 편집가능 하도록 만드는 단계.
- ### Localization
  - 외부로 꺼내진 문자열들을 번역하는 단계

## LANGUAGE-SPECIFIC THOUGHTS
- 히브리어나 아랍어로 설정하면 자동으로 글씨가 왼쪽에서 오른쪽으로 뒤집음
- 중국어나 일본어는 띄어쓰기가 없기 때문에 라벨이 짧아보일 수 있음.
- 독일어는 반대로 한 단어가 길어지기 쉬움.

## ADDING A LANGUAGE
- Project에서 언어를 추가하면 .strings 파일이 생성됨.
- .strings 파일에서는 세미콜론 찍어줘야 함.

## SEPARATING TEXT FROM CODE
- `NSLocalizedString()`을 사용해서 .strings 파일로부터 특정 키값의 노컬라이즈 값을 받아올 수 있음.
- `value`는 디폴트 값. 디폴터 값을 키값으로 놓으면 동음이의어 때문에 문제가 생길 수 있으므로 주의.
- 컨텍스트를 모르는 번역자를 위해 주석은 아주 중요.

## FORMATTING VALUES
- 통화를 포맷팅 할 때는 환율을 먼저 고려해야 함.
- 길이나 에너지, 질량 값은 SI 단위를 사용.

## RUNNING A LANGUAGE SCHEME
- Manage Scheme > Options 에서 다른 언어로 설정 가능.

## LOCALIZING THE APP
- Editor > Export For Localization으로 xliff 파일을 익스포트 해서 번역함.
- 번역한 파일은 Import 해옴.

## PREVIEWING THE LOCALIZATION
- 스토리보드의 어시스턴트 에디터에서 Preview 모드에서 언어를 바꿔가며 지역화를 확인 가능.
- Double-length Pseudolanguage로 길이를 뻥튀기 해서 확인 가능.
