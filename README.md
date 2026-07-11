# 이유정 · Yoojeong Lee — Portfolio

AI Product Manager & Strategist 개인 포트폴리오 웹페이지입니다.
`index.html` 하나로 완결된 정적 페이지라 별도 빌드 없이 바로 배포됩니다.

## 🚀 GitHub Pages로 올리기

1. GitHub에서 새 저장소를 만듭니다. 이름을 `<username>.github.io`로 하면 주소가 `https://<username>.github.io`가 됩니다. (일반 이름도 가능 — 이 경우 주소는 `https://<username>.github.io/<repo>`)
2. 이 폴더를 그대로 올립니다:
   ```bash
   cd ~/Desktop/prj-portfolio
   git init
   git add index.html README.md 이력서_이유정_Jun2026_kor.pdf
   git commit -m "portfolio site"
   git branch -M main
   git remote add origin https://github.com/<username>/<repo>.git
   git push -u origin main
   ```
3. 저장소 → **Settings → Pages → Source**를 `main` 브랜치 `/ (root)`로 지정 → 저장.
4. 1~2분 뒤 안내된 주소로 접속하면 배포 완료입니다.

> 💡 이력서 PDF 다운로드 버튼이 동작하려면 `이력서_이유정_Jun2026_kor.pdf`도 함께 커밋하세요.

## 📸 프로필 사진 넣기

이 폴더에 **`profile.jpg`** 라는 이름으로 사진을 저장하면 Hero(상단)에 자동으로 표시됩니다.
파일이 없으면 `YJ` 이니셜 플레이스홀더가 대신 보입니다.

- 권장: 세로형(portrait), **4:5 비율**, 800×1000px 이상, 인물 중심
- 파일명을 정확히 `profile.jpg`로 (소문자, 확장자 `.jpg`)
- PNG를 쓰려면 `index.html`에서 `src="profile.jpg"` 를 `src="profile.png"` 로 바꿔 주세요.

## 🎨 커스터마이징

모두 `index.html` 한 파일 안에 있습니다.

- **색상 / 테마** — 파일 상단 `:root`의 CSS 변수(`--accent`, `--brass`, `--paper` 등)만 바꾸면 전체 톤이 바뀝니다. 라이트·다크 모두 정의되어 있습니다.
- **문구 / 프로젝트** — `<section>` 블록의 텍스트를 수정하세요. 프로젝트 카드는 `data-cat` 속성(`strategy`/`genai`/`biz`/`data`)으로 상단 필터에 연결됩니다.
- **연락처** — 이메일(`yoojeonglee12@gmail.com`)과 LinkedIn 주소가 여러 곳에 들어 있으니 함께 바꿔 주세요.
- **폰트** — Pretendard(본문·한글) + IBM Plex Mono(라벨·데이터)를 CDN으로 불러옵니다. 오프라인/인트라넷에서는 시스템 폰트로 자연스럽게 대체됩니다.

## 포함 기능

- **한국어 / 영어 언어 토글** (우측 상단 `KO · EN`) — 전체 콘텐츠 이중언어 지원
- 라이트/다크 테마 토글 + OS 설정 자동 감지
- 스크롤 등장 애니메이션 · 지표 카운트업 · 프로젝트 필터 · 섹션 스크롤 스파이
- 모바일 반응형, 접근성(키보드 포커스, `prefers-reduced-motion`) 대응
