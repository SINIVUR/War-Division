# 워 디비전 (WAR DIVISION)

2차대전 × 스팀펑크 × 마법 모바일 RTS. 갤럭시 S23 가로 화면 기준.

## 들어 있는 파일
- `index.html` — 게임 전체 (이 파일 하나로도 실행됨)
- `manifest.webmanifest` — 앱 이름·아이콘·가로 고정 전체화면 설정
- `sw.js` — 오프라인 실행용 서비스 워커
- `icons/` — 앱 아이콘 (192, 512)

## 폰에 앱으로 설치하기 (GitHub Pages)
PWA 설치는 **https 주소**에서만 됩니다. 파일을 폰에서 바로 열면 게임은 되지만 설치 버튼은 안 나와요.

1. GitHub에서 새 저장소를 만들고 (예: `war-division`) 이 폴더 안의 파일을 **그대로** 올립니다.
   (`index.html`이 저장소 맨 위에 있어야 해요.)
2. 저장소 **Settings → Pages** 에서 Source를 `Deploy from a branch`, 브랜치 `main` / 폴더 `/(root)` 로 저장.
3. 1~2분 뒤 `https://<아이디>.github.io/war-division/` 주소가 생깁니다.
4. S23의 **Chrome**으로 그 주소를 열고 → 오른쪽 위 ⋮ → **앱 설치** (또는 "홈 화면에 추가").
5. 홈 화면 아이콘으로 실행하면 주소창 없이 가로 전체화면으로 열리고, 한 번 연 뒤에는 오프라인에서도 실행돼요.

업데이트할 때는 파일을 덮어 올린 뒤 `sw.js`의 `CACHE` 이름(예: `war-division-v3`)을 바꿔 주세요.

## 컴퓨터에서 테스트
폴더에서 `python -m http.server 8000` 실행 후 `http://localhost:8000` 접속.
