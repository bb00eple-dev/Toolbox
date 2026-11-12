P. Toolbox v66 · Window Frame / Wallpaper Scope / CJK Font

배포 파일:
- index.html
- sw.js

기존 GitHub Pages 저장소에는 실제 변경된 index.html과 sw.js만 교체하세요.
manifest.webmanifest와 아이콘은 변경하지 않았으므로 유지합니다.
LocalStorage / IndexedDB를 초기화하지 마세요.

이번 변경 사항:
- 테마 패턴을 body 바깥 배경에만 표시하고, P. Toolbox 윈도우 내부 main 캔버스에는 배경 이미지를 완전히 제거
- 앱 전체 윈도우(타이틀바, 내비게이션, 콘텐츠 포함)에 독립적인 이중 외곽 프레임 적용
- 기존 창 너비와 내부 카드 디자인은 그대로 유지
- 페어 D-DAY 표시 옵션에 PLAIN / NO DECORATION 추가
- 장식형 D-DAY는 캐릭터 A/B 사진 아래에서 충분한 여백을 확보해 독립 섹션으로 표시
- Google Fonts의 Noto Sans KR, SC, TC, HK를 불러와 한국어/중국어 문자 범위 지원
- Pair Board 화면 및 로그 작성/열람 기본 글꼴에 CJK 폰트 스택 적용
- 로그 글꼴 선택 메뉴에 "Noto Sans CJK · 한글/중국어" 추가 및 기본 선택으로 설정
- 기존 D-DAY 스타일 값, LocalStorage/IndexedDB, 게시글/이미지 레코드 변경 또는 초기화 없음

폰트:
- Google Fonts에서 온라인으로 글꼴을 불러옵니다.
- 인터넷 연결이 없거나 Google Fonts에 접근할 수 없으면 Malgun Gothic / Microsoft YaHei / PingFang SC 등 설치된 시스템 글꼴로 대체됩니다.
- Noto CJK는 KR/SC/TC/HK 언어별 글꼴을 별도로 지정해 한국어, 중국어 간체·번체를 처리합니다.

검증:
- 중복 ID 검사: 중복 없음
- 인라인 JavaScript 문법 검사: 오류 없음
- CSS 구문 파싱: 오류 없음
- ZIP 무결성 검사: 통과
- 실제 화면 확인은 현재 실행 환경의 브라우저 탐색이 관리자 정책으로 차단되어 완료하지 못함
- 배포 후 실제 PC/모바일 브라우저에서 테마 패턴, D-DAY 간격/무장식 옵션, 글꼴 표시를 확인해야 함
