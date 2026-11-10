P. TOOLBOX v55 · READER REDESIGN

배포
1. 기존 GitHub 저장소의 index.html과 sw.js를 v55 파일로 교체합니다.
2. 기존 manifest.webmanifest와 아이콘은 유지해도 됩니다.
3. LocalStorage 및 IndexedDB를 초기화하지 마세요.

이번 수정
- Pair Log 열람 화면의 시각 디자인을 전면 재구성했습니다.
- 전체 화면 독립형 열람 레이아웃을 유지하면서, 본문을 카드 안에 가두지 않고 넓은 문서 영역으로 표시합니다.
- 제목, 날짜, 메타데이터, 태그의 크기와 위계를 분리했습니다.
- 기존 6개 스킨을 서로 다른 디자인 언어로 재설계했습니다: Editorial Paper, Diner Note, Old Letter, Soft Windows, Midnight Ink, Botanical Index.
- 스킨별 배경/글자/포인트 색상 커스터마이징 및 로그별 저장 구조는 유지됩니다.
- 본문 이미지, 표, 인용문, 제목 등 리치 콘텐츠 표시 규칙을 각 스킨에 맞게 정리했습니다.
- 로그 작성/수정 화면에서 선택한 스킨을 해당 로그에 저장하고 열람 화면에서 불러오는 기존 흐름은 유지했습니다.

검증
- 인라인 JavaScript 구문 검사
- 서비스 워커 구문 검사
- CSS 파싱 검사
- HTML 중복 ID 검사
- 매니페스트 JSON 및 ZIP 무결성 검사

주의
- 이번 버전은 로그 뷰어 디자인 집중 수정판입니다. 기존 페어, 백업 게시판, 랜덤 프롬프트 기능은 v54 상태를 유지합니다.
- 기존 LocalStorage와 IndexedDB 자료를 삭제하거나 초기화하지 마세요.
- 실제 모바일 기기에서의 화면/터치 확인은 별도로 필요합니다.
