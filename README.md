# 엔조이모션클럽 홈페이지 시안

`index.html` 하나로 완결되는 반응형 원페이지 시안입니다. 별도 빌드나 서버 없이 브라우저에서 파일을 열면 바로 보입니다.

## 미리보기

- **공개 주소: https://cmyoungh-ui.github.io/enjoymotionclub/**
- `index.html` 파일을 브라우저로 열기
- 또는 폴더에서 `python3 -m http.server 8000` 실행 후 `http://localhost:8000` 접속

## 배포

GitHub Pages(`main` 브랜치 `/` 루트)로 자동 배포됩니다. 이 폴더에서 고친 뒤 커밋·push하면 1~2분 안에 위 주소에 반영됩니다.

```
git add -A && git commit -m "수정 내용" && git push origin main
```

- 저장소: https://github.com/cmyoungh-ui/enjoymotionclub
- Pages는 HTML을 최대 10분간 캐시합니다(캐시 지운 새로고침 또는 사파리 개인정보 보호 탭으로 바로 확인).

## 구성

| 파일 | 설명 |
| --- | --- |
| `index.html` | 페이지 전체 (HTML + CSS + 최소 JS 포함) |
| `assets/hero-banner.png` | 히어로 배경 (원본) |
| `assets/hero-banner.webp` | 히어로 배경 (경량 버전, 87KB) |
| `assets/studio-real.jpg` | 스튜디오 공간 실제 사진 (1200×1600) |
| `assets/studio-real.webp` | 같은 사진 경량 버전 (131KB) |
| `assets/schedule.jpg` | 시간표 이미지 (라이트박스용) |
| `assets/schedule.webp` | 시간표 경량 버전 |
| `assets/pricing.jpg` | 수강료 이미지 (라이트박스용) |
| `assets/pricing.webp` | 수강료 경량 버전 |
| `assets/clip-1.mp4` … `assets/clip-6.mp4` | 실제 수업 영상 6편 (H.264 / 720×1280 / 무음, 0.4–3.1MB) |
| `assets/clip-1-poster.jpg` … `assets/clip-6-poster.jpg` | 각 영상의 포스터 프레임 (720×1280, 약 50KB) |
| `assets/studio-balance.jpg` | 밸런스 패드 수업 사진 (945×1614, 아이폰 상단 바·검은 여백 제거) |
| `assets/studio-balance.webp` | 같은 사진 경량 버전 (59KB) |
| `assets/practice-sunlit.jpg` | 햇살 아래 요가·호흡 실제 사진 (1600×900, EXIF 제거) |
| `assets/practice-sunlit.webp` | 같은 사진 경량 버전 (62KB) |
| `assets/community-clinic.jpg` | 화성FC ORANGE RE:BON 헬스케어 클리닉 현장 사진 (1600×900, EXIF 제거) |
| `assets/community-clinic.webp` | 같은 사진 경량 버전 (71KB) |

`<picture>`로 webp를 먼저 불러오고, 지원하지 않는 브라우저는 원본 PNG/JPG를 사용합니다.

## 섹션

1. 상단 고정 내비게이션 — 프로그램 / 수업 모습 / 사회공헌 / 시간표 / 수강료 / 오시는 길 + `체험 예약`
2. 히어로 — 화성 FC 공식 파트너 배지, 메인 카피, 체험 예약·블로그 CTA
3. 핵심 정보 스트립 — 새벽 요가, 평일 운영시간, 1:1 레슨, 무료 주차
4. 프로그램 — 베이직·하타 요가 / 새벽 요가 / 모션 트레이닝(모션탭 센서·6 스테이션 서킷) / 1:1 개인 레슨 + 햇살 아래 요가 실제 사진(`practice-sunlit`)
5. 수업 모습 — 실제 수업 영상 6편(클릭 재생) + 밸런스·코어 사진 + 모션탭·6 스테이션 설명
6. 공간 소개 — 스튜디오 사진 + 편의시설
7. 사회공헌 — 화성FC ORANGE RE:BON 헬스케어 클리닉 사진 + 초등학교 돌봄친구들·지역사회 프로그램
8. 운영시간 & 시간표 — 요약 카드 + 주간 시간표 표 + 시간표 이미지(클릭 시 확대)
9. 수강료 & 혜택 — 4개 요금 카드 + 체험비 페이백 배너 + 수강료 이미지(클릭 시 확대)
10. 오시는 길 & 채널 — 주소·전화·운영시간·편의시설 + 네이버 플레이스·인스타그램·블로그·당근
11. 푸터 — 사업자 정보, 바로가기
12. 모바일 하단 고정 바 — 전화 / 체험 예약

## 수정할 때

- 색상: `index.html` 상단 `:root`의 `--brand`, `--brand-soft`, `--cream`, `--ink` 값만 바꾸면 전체 톤이 바뀝니다.
- 시간표: `table.timetable`의 셀 텍스트를 고치면 됩니다. 이미지(`assets/schedule.jpg`)는 별도로 교체해야 합니다.
- 수강료: `.price-card`의 금액과 `회당` 문구를 함께 맞춰 주세요.

## 참고

- 폰트는 Pretendard(CDN) → Noto Sans KR → 시스템 폰트 순으로 대체됩니다. 오프라인에서는 시스템 폰트로 보입니다.
- `og:image`는 `https://cmyoungh-ui.github.io/enjoymotionclub/assets/hero-banner.png` 절대 주소로 지정되어 있습니다. 커스텀 도메인을 붙이면 그 주소로 바꿔 주세요.
- 사업자등록번호와 대표자명은 푸터에 표기되어 있습니다. 공개하지 않으려면 해당 줄을 지우면 됩니다.
- 영상은 `preload="metadata"` + `poster`라서 재생 버튼을 누르기 전에는 영상 본체를 내려받지 않습니다. 영상에는 소리(오디오 트랙)가 없습니다.
- 영상을 바꿀 때는 같은 이름(`clip-N.mp4`)으로 교체하고 `clip-N-poster.jpg`를 함께 바꾸면 됩니다. 세로 영상은 `9:16`으로 꽉 차게(object-fit: cover) 보입니다.
