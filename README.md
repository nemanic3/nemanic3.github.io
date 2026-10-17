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

## 콘텐츠 확인 기준 (2026-10-18)

만든 이유는 개발자가 직접 제공한 배경을 반영했습니다. 개발 기간·역할·수상은 기존 포트폴리오와 아래 자료를 대조했습니다. 현재 기능은 README·배포 문서와 코드의 현재 구성을 우선합니다. 최근 배포와 유지보수는 원래 프로젝트 개발 기간에 합치지 않습니다. 검증 수치·기여율·실제 사용자 수를 추정하지 않습니다.

- [NEMANIC 소개](https://nemanic.dev/about/), [프로젝트 목록](https://nemanic.dev/projects/)
- [모일 공개 소개](https://nemanic.dev/projects/moil/): Next.js·OpenNext·Workers·D1. 2026.10은 첫 공개 시점. 가입 전 체험은 저장되지 않으며 은행·증권사·실시간 시세 연결 없음. 비공개 저장소 코드·링크는 공개하지 않음.
- [우리사이 공개 소개](https://nemanic.dev/projects/urisai/): 선택적 위치 공유와 마지막 공유 위치를 구분. 스페인은 개발 계기이며 이용 국가 제한이 아님.
- [뛸때 소개](https://nemanic.dev/projects/runwhen/), [사용 가이드](https://nemanic.dev/projects/runwhen/guide/): 최신 README·구현의 React·Vite·Pages·Functions, 기상청 예보와 개인화 비교 기준을 반영. 계정·DB 없음. 추천 규칙은 초기 제품 가설이며 의학적 분석·안전 보장이 아님.
- [AC:RE 공개 소개](https://nemanic.dev/projects/acre/): 회사 내부 자료·비공개 저장소·관리 화면은 사용하지 않음. 정식 운영 전환을 주장하지 않음.
- [꽃동네 소개](https://nemanic.dev/projects/kkotdongnae/), `README.md`, `docs/DEPLOYMENT.md`, `docs/NEMANIC_INTRO.md`
- [홍익대 졸업봇 소개](https://nemanic.dev/projects/hongik-graduation-bot/), `README.md`, `docs/CLOUDFLARE_DEPLOYMENT.md`: README의 초기 Kakao OCR/React 설명 대신 최신 배포 문서와 공개 소개의 PaddleOCR/Next.js 구성을 사용. 원래 Team Lead / Backend 역할은 기존 포트폴리오와 README로 확인.
- [다독다독 소개](https://nemanic.dev/projects/dadokdadok/), `README.md`, `docs/cloudflare-deployment.md`: 현재 Vanilla JavaScript·Kakao Daum API·Render·Neon 구성 사용.
- [Tutor Manager 공개 소개](https://nemanic.dev/projects/tutor-manager/): 개발 중으로 표시. 직접 과외하며 만든 배경과 기획·웹·서버 개발 범위를 반영. 확인되지 않은 기간·저장소 링크나 네이티브 출시 완료 표현은 추가하지 않음.

꽃동네·다독다독은 기존 로고 파일을 유지합니다. `hongik-landing.jpg`와 `kkotdongnae-login.jpg`는 NEMANIC 상세 페이지의 공개 로그인 전 화면을 사용합니다. 화면 이미지는 2026-10-12에 확보했으며 실사용자 정보나 성적표를 포함하지 않습니다. 꽃동네 로그인 화면은 펼쳐 보는 실제 서비스 화면 영역에만 배치합니다.

## 구현 근거와 편집 범위

이 포트폴리오는 `_data/projects.json` 하나에서 카드와 펼침 설명을 함께 렌더링합니다. 08→01 순서이며 날짜가 확인되지 않은 프로젝트는 기간을 생략합니다. 새 개인 서비스 이미지는 CSS 타이포그래피이며 실제 서비스 화면으로 표시하지 않습니다.

2026-10-18 읽기 전용으로 확인한 자료:

- NEMANIC 홈페이지: `src/lib/site.ts`, `src/lib/project-overview.ts`, 공개 프로젝트 상세 페이지. 서비스 허브는 별도 저장소이며 수정하지 않았습니다.
- 꽃동네: `README.md`, `docs/DEPLOYMENT.md`, `docs/NEMANIC_INTRO.md`, `pubspec.yaml`, `backend/shops/views.py` (확인 리비전 `d4deb16`).
- 홍익대 졸업봇: `README.md`, `docs/CLOUDFLARE_DEPLOYMENT.md`, 프런트엔드 `package.json`, 백엔드 OCR 의존성·배포 구성 (확인 리비전 `a9ec663`).
- 다독다독: `README.md`, `docs/cloudflare-deployment.md`, `backend/goal/views.py` (확인 리비전 `68f7e79`).
- 뛸때: 최신 원격 README와 `src/lib/personalize.ts`, `src/lib/recommend.ts`, `functions/lib/validate.ts`의 변경 범위 (확인 리비전 `7fc8dd3`). 저장소 링크·내부 코드는 공개 페이지에 포함하지 않습니다.
- 모일: 현재 README·패키지 구성과 공개 소개를 대조. 비공개 소스·운영 설정은 이 저장소로 복사하지 않습니다.
- Tutor Manager: 현재 README와 공개 소개를 대조. 공개 페이지에는 개발 범위와 기술·운영 구조만 반영합니다.

과거 검증 기록은 해당 프로젝트의 근거로만 소개합니다. 이번 포트폴리오 수정으로 서비스의 기능·운영 검증을 새로 수행한 것처럼 표현하지 않습니다. 다른 서비스의 저장소, DB, Secrets, DNS 및 배포 설정은 변경하지 않습니다. 기존 PDF는 보존합니다.

링크 검사에서 꽃동네·홍익대 졸업봇·다독다독 저장소도 현재 비공개임을 GitHub API로 확인했습니다. 비로그인 방문자에게 404가 되는 코드·문서 버튼은 제거하고 정상 응답하는 서비스·공개 상세 링크를 유지했습니다. 저장소 공개 범위는 변경하지 않았습니다.
