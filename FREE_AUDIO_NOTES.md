# 무료 음원 연결 현황

2026-10-20 업데이트. 실행 파일: 같은 폴더의 index.html.

## 연결 방식

음원은 파일에 내장되지 않았으며 Wikimedia Commons 외부 서버에서 재생한다. 인터넷이 필요하다. 원본 제공 페이지의 이용 조건을 확인하고 제작자·원본 링크·라이선스 링크·파일 변경 여부를 학습 화면과 보호자 공간에 표기했다. 최초 재생 버튼을 누르기 전에는 외부 음원 파일을 로드하지 않는다.

| 앱 곡 | 자료 종류 | 제작자 | 조건 |
|---|---|---|---|
| 작은 별 / Twinkle, Twinkle, Little Star | 같은 피아노 연주 파일 | John Casale | CC BY-SA 2.5 |
| The Alphabet Song | 선율 예제 | CambridgeBayWeather | CC BY-SA 3.0 |
| Old MacDonald Had a Farm | 선율 예제 | CambridgeBayWeather | CC BY-SA 3.0 |
| Row, Row, Row Your Boat | 선율 예제 | CambridgeBayWeather | CC BY-SA 3.0 |
| Baa, Baa, Black Sheep | 선율 예제 | CambridgeBayWeather | CC BY-SA 3.0 |
| Mary Had a Little Lamb | 영어 가창 | Celestianpower | 제작자 Public domain 선언 |
| London Bridge Is Falling Down | 선율 예제 | CambridgeBayWeather | CC BY-SA 3.0 |
| Itsy Bitsy Spider | 영어 가창 영상 | Anaheim Libraries / Angel Sauceda Garcia | CC BY 3.0 |
| Hot Cross Buns | 선율 예제 | CambridgeBayWeather | CC BY-SA 3.0 |

총 10개 곡 화면에 9개 파일을 연결했다. 작은 별에는 한국어 가창이 없다. 선율 예제의 가창 여부·발음·음질은 실제 청취 검수를 거치지 않았으므로 완성된 보컬 학습 음원으로 간주하지 않는다.

## 한국 전래동요 무료 자료

- 꼭꼭 숨어라: 한국저작권위원회, 국악연주곡_꼭꼭숨어라_해금, CC BY.
  https://gongu.copyright.or.kr/gongu/wrt/wrt/view.do?menuNo=200020&wrtSn=13262896
- 대문놀이: 한국저작권위원회, 국악연주곡_동대문놀이_해금, CC BY.
  https://gongu.copyright.or.kr/gongu/wrt/wrt/view.do?menuNo=200020&wrtSn=13262904

이 두 곡은 공식 제공 페이지와 조건만 확인했고 앱 내 재생 파일은 연결하지 못했다. 공식 페이지를 열거나 다운로드한 파일을 기기 내에서 여는 방법을 제공한다. 나머지 48곡은 음원 준비 중으로 표시한다.

## 확인 범위와 남은 작업

현재 실행 환경의 네트워크 정책이 음원 다운로드를 차단한다(Node fetch EACCES). 브라우저 자동화 표면도 없다. 출처·라이선스 문서는 웹 도구로 확인했으며 실제 음원 청취·재생·모바일 형식 지원은 확인하지 못했다. 코드 검사는 60곡 목록, 연결 10곡 필터, 출처 표기, 미연결 상태, 단어·퀴즈, 단일 HTML 번들을 확인했다.

원본 파일의 라이선스·출처·직접 재생 주소는 noraerang/dist/free-audio.js에 보관한다. CC BY-SA 음원을 수정 배포할 때에는 해당 음원의 동일조건변경허락 요건을 준수해야 한다. 앱 코드를 곧바로 동일 라이선스라고 선언한 것은 아니다.

기존 PRD의 ‘60곡 실제 가창 + 반주’ 완료 기준은 아직 충족되지 않았다. 60곡 무료 가창 확보가 끝난 것으로 표시하지 않는다.

## 수정 후 단일 파일 만들기

noraerang 폴더에서 Node.js로 build.cjs를 실행하면 상위 폴더의 index.html을 다시 생성한다. verify.cjs는 네트워크·브라우저 없이 실행하는 기능 검사다. audio-update.cjs는 이미 적용된 일회성 마이그레이션 기록이므로 다시 실행하지 않는다.
