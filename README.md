# 한진개발 홈페이지

운영 주소: https://majitap.github.io/hanjin/
스테이지(시안 확인용): https://majitap.github.io/hanjin/stage/

대구 및 인근 건설 현장의 인력 공급을 안내하는 반응형 정적 사이트입니다.
GitHub Pages에서 `main` 브랜치의 저장소 루트(`/`)를 배포합니다.
패키지 설치나 빌드 명령이 필요하지 않습니다.

## 파일

- `index.html`: 배경 영상 첫 화면, 회사소개·인력공급·진행절차·문의 섹션, 문의 창, 운영 주소 메타데이터
- `styles.css`: PC·모바일 화면, 상단 메뉴, 문의 창
- `script.js`: 상단 메뉴 전환, 배경 영상 정지/재생, 스크롤 표시, 문의 창, 입력 검증, 문의 전송과 내용 복사
- `email.js`: Web3Forms 전송, 응답 확인과 오류 안내
- `assets/`: 로고, 배경 영상과 포스터, 문의 창 사진
  - `hero.mp4`: Pexels 무료 라이선스 영상 (Sururi Ballıdağ, https://www.pexels.com/video/28823325/)
    영상 왼쪽의 광고판이 보이지 않도록 넓은 화면에서는 오른쪽 기준으로 확대해 잘라 보여줍니다.
  - `hero-poster.jpg`: 영상이 로딩되기 전에 보이는 첫 장면
- `.nojekyll`: 정적 파일 직접 배포
- `stage/`: 운영 반영 전에 시안을 확인하는 사본입니다. 검색 노출을 막고(`noindex`), 문의 전송은 루트의 `email.js`를 함께 사용합니다.
  운영에 반영할 때는 `stage/`의 HTML·CSS·JS를 루트로 옮기면서 `../` 경로와 `noindex`, `og:url`을 운영 기준으로 바꿉니다.

## 문의 메일

문의 접수에는 Web3Forms를 사용합니다. 운영 문의 수신 주소는 아래 관리 화면에서 설정합니다.
운영 폼 관리: https://app.web3forms.com/forms/8304c623-6777-4d4a-8711-2b4ab01175df/settings

수신 주소는 Web3Forms에서 인증한 뒤 해당 운영 폼의 Settings → Recipient Emails에서 설정합니다.
HTML의 `data-access-key`는 Web3Forms가 공개 사용하도록 발급한 폼 식별자입니다.
메일 계정 비밀번호나 비밀 API 키를 저장소에 넣지 마세요.

무료 요금제는 계정 전체 월 250건이며, 기본 메일 안내문과 서비스 브랜딩이 포함됩니다.
전송 실패 시 입력 내용이 유지되며, 응답이 불확실하면 중복 접수 전에 전화로 확인하도록 안내합니다.

## 회사 정보 변경

`index.html`에서 대표번호 `053-558-8338`, 회사 이메일 `daebaq54@naver.com`,
주소 `대구 서구 달서로 2`와 서비스 안내를 수정합니다.
웹 폼 수신 주소 변경은 Web3Forms 설정에서도 별도로 진행해야 합니다.

CSS 또는 JavaScript 수정 후에는 HTML의 파일 버전 쿼리도 갱신하여 이전 파일 캐시를 방지합니다.
