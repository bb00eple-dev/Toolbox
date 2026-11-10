P. Toolbox v52 · Reader & Prompt Expansion

v52는 v51의 기능을 유지하면서 Pair Log 뷰어, PROMPT RANDOM, PROMPT BACKUP 버전 사진, 메인 타이틀 바 테마를 개선한 버전입니다.

변경 사항
- Pair Log 목록에서 로그 카드를 누르면 바로 별도 열람 뷰어가 열립니다. 목록에서 본문을 접고 펼치는 UI는 제거했습니다.
- 로그 뷰어 스킨 5종: Retro Diner, Letter Garden, Classic Windows, Soft Editorial, Midnight Archive. 선택한 스킨은 다음 열람에도 유지됩니다.
- PROMPT RANDOM의 카메라 앵글, 구도, 포즈, 배경, 분위기, 조명, 효과 태그 확장
- 새로 추가된 태그는 목록과 한국어 자연어 미리보기에서 한국어로 표시하고, 실제 프롬프트 결과는 영어 태그로 출력
- 랜덤 카테고리의 ＋ 버튼으로 같은 카테고리의 선택칸을 추가해 동시에 최대 4개 태그 조합 가능. 개별 랜덤/선택 랜덤도 추가 선택칸을 함께 처리
- PROMPT BACKUP 각 버전에 전용 사진 첨부, 버전 전환 시 해당 사진도 함께 전환
- 게시글 공용 사진은 계속 유지되고 버전 전용 사진과 함께 표시됩니다.
- 버전 탭은 좌측부터 생성 순서대로 유지되며 현재 버전 전환 후에도 모든 버튼이 표시됩니다.
- THEME 설정에서 메인 P. Toolbox 타이틀 바 포인트 색을 기본 견본 8종 또는 HEX 색상으로 지정 가능
- 격자 패턴에서 선 색과 선 사이 색이 각각 보이도록 배경 그라디언트와 격자 크기 수정

배포 방법
1. 기존 GitHub Pages 저장소의 index.html과 sw.js를 이 패키지 파일로 교체합니다.
2. 기존 저장소에 manifest.webmanifest가 있다면 기존 파일을 유지하고, 없다면 패키지의 기본 manifest.webmanifest를 추가합니다. 아이콘 파일은 패키지 파일을 사용하거나 기존 아이콘을 유지해도 됩니다.
3. LocalStorage/IndexedDB를 삭제하거나 초기화하지 마세요.
4. 서비스 워커 캐시 이름은 p-toolbox-shell-v52입니다. 배포 후 앱을 새로고침해 새 캐시를 적용하세요.

데이터 호환성
- 기존 Prompt Backup 게시글의 prompts 필드는 유지됩니다.
- 기존 버전 배열에는 images가 없는 경우 빈 사진 배열로 읽습니다.
- 기존 게시글 공용 images는 계속 표시됩니다. 버전별 images는 각 버전 데이터에 별도로 저장됩니다.
- 기존 Pair Log, Prompt Backup, 룸 데이터 저장 키는 변경하거나 초기화하지 않습니다.

검증 범위
- JavaScript 구문 검사, HTML ID 중복 검사, CSS 파싱, manifest JSON, ZIP 무결성 검사
- 이 실행 환경에서는 Chromium이 관리자 정책으로 로컬/로컬 서버 페이지 접속을 차단해 실제 UI 클릭 테스트는 실행하지 못했습니다. 따라서 실기기 및 GitHub Pages 통합 동작은 배포 후 확인이 필요합니다.
