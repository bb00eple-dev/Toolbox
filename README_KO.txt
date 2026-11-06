P. TOOLBOX v36 · GITHUB PAGES 배포

1. ZIP 파일의 내용을 전부 압축 해제합니다.
2. GitHub 저장소의 최상위(root)에 다음 구조 그대로 업로드합니다.

   index.html
   manifest.webmanifest
   sw.js
   icons/
     pwa-192.png
     pwa-512.png
     pwa-512-maskable.png

3. GitHub 저장소 Settings → Pages에서 배포할 브랜치와 /(root)를 선택합니다.
4. 배포된 https:// 주소로 접속합니다.
5. 로그인 후 설정 → 앱 설치를 누르거나 브라우저 메뉴에서 앱 설치 / 홈 화면에 추가를 선택합니다.

주요 기능
- PROMPT RANDOM / OUTFIT RANDOM / PROMPT EDITOR
- PROMPT BACKUP / PHOTO GALLERY
- PAIR BOARD: 캐릭터 2인 등록, 페어 사진 보관, 대화 로그 백업
- 설정 → JSON 내보내기 / 가져오기

저장 안내
- 현재 공간의 데이터는 같은 브라우저의 사이트 저장소(IndexedDB 및 localStorage)에 보관됩니다.
- GitHub Pages는 정적 호스팅이므로 데이터가 GitHub 저장소나 다른 기기로 자동 동기화되지는 않습니다.
- 브라우저 변경, 기기 변경, 사이트 데이터 초기화에 대비해 설정에서 JSON 백업 파일을 주기적으로 내보내 보관하세요.
- JSON 가져오기는 ID가 겹치지 않는 자료를 병합하며 기존 자료를 덮어쓰지 않습니다.

PWA 안내
- 앱 설치에는 GitHub Pages의 HTTPS 주소로 접속해야 합니다.
- Android/Chrome: 브라우저 메뉴의 앱 설치 또는 설정의 앱 설치 버튼을 사용하세요.
- iPhone/iPad: Safari 공유 메뉴 → 홈 화면에 추가를 사용하세요.
