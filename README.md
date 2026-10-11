# NEMANIC · 신성현 포트폴리오

Jekyll 기반 채용·협업용 개인 포트폴리오입니다.

- 공개 주소: https://portfolio.nemanic.dev/
- 자동 배포: GitHub Pages, `main` 브랜치의 저장소 루트 (기존 legacy build)
- 도메인: 기존 `CNAME` 유지. 이 저장소는 다른 NEMANIC 서비스의 설정을 변경하지 않습니다.
- 콘텐츠: `index.html`, `_data/projects.json`, `_includes/project.html`
- 스타일·탐색: `assets/css/style.css`, `assets/js/main.js`

## 로컬 빌드

`Gemfile.lock`의 Jekyll 4.4.1 / Bundler 4.0.17에 맞는 Ruby 환경을 사용합니다.

```sh
bundle install
JEKYLL_ENV=production bundle exec jekyll build
bundle exec jekyll serve
```

GitHub Pages의 기본 빌드 환경과 로컬 Jekyll 버전은 다를 수 있으므로 push 후 Pages 빌드 결과와 실제 공개 도메인도 확인합니다. 별도 워크플로, 호스팅 이전 또는 도메인 변경은 추가하지 않았습니다.

## 콘텐츠 확인 기준 (2026-10-12)

개발 기간·역할·수상은 기존 포트폴리오와 아래 공개 자료를 대조했습니다. 최근 배포와 유지보수는 원래 프로젝트 개발 기간에 합치지 않습니다. 검증 수치·기여율·실제 사용자 수를 추정하지 않습니다.

- [NEMANIC 소개](https://nemanic.dev/about/), [프로젝트 목록](https://nemanic.dev/projects/)
- [AC:RE 공개 소개](https://nemanic.dev/projects/acre/): 회사 내부 자료·비공개 저장소·관리 화면은 사용하지 않음. 정식 운영 전환을 주장하지 않음.
- [꽃동네 소개](https://nemanic.dev/projects/kkotdongnae/), [README](https://github.com/nemanic3/kkotdongnae), [DEPLOYMENT](https://github.com/nemanic3/kkotdongnae/blob/main/docs/DEPLOYMENT.md), [NEMANIC_INTRO](https://github.com/nemanic3/kkotdongnae/blob/main/docs/NEMANIC_INTRO.md)
- [홍익대 졸업봇 소개](https://nemanic.dev/projects/hongik-graduation-bot/), [README](https://github.com/nemanic3/HONGIK_BOT), [최신 배포 검증](https://github.com/nemanic3/HONGIK_BOT/blob/master/docs/CLOUDFLARE_VERIFICATION.md): README의 초기 Kakao OCR/React 설명 대신 최신 배포 문서와 공개 소개의 PaddleOCR/Next.js 구성을 사용. 원래 Team Lead / Backend 역할은 기존 포트폴리오와 README로 확인.
- [다독다독 소개](https://nemanic.dev/projects/dadokdadok/), [README](https://github.com/nemanic3/dadokdadok), [최신 배포 문서](https://github.com/nemanic3/dadokdadok/blob/master/docs/cloudflare-deployment.md): 현재 Vanilla JavaScript·Kakao Daum API·Render·Neon 구성 사용.
- [Tutor Manager 공개 소개](https://nemanic.dev/projects/tutor-manager/): 개발 중으로 표시. 공개 자료에 없는 역할·기간·저장소 링크는 추가하지 않음.

꽃동네·다독다독은 기존 로고 파일을 유지합니다. `hongik-landing.jpg`와 `kkotdongnae-login.jpg`는 NEMANIC 상세 페이지의 공개 로그인 전 화면을 사용합니다. 화면 이미지는 2026-10-12에 확보했으며 실사용자 정보나 성적표를 포함하지 않습니다. 꽃동네 로그인 화면은 펼쳐 보는 실제 서비스 화면 영역에만 배치합니다.
