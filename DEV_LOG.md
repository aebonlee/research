# Research Master - Development Log

> 사회과학 조사방법론 학습 플랫폼
> URL: https://research.dreamitbiz.com
> Repository: https://github.com/aebonlee/Research

---

## 2025-04-09 — 3개 신규 학습 경로 추가

### 개요

기존 8개 학습 경로에 **3개 신규 학습 경로**를 추가하여 총 **11개** 학습 경로 구성 완료.

### 신규 학습 경로

| # | ID | 한글명 | English | 경로 | 색상 | 아이콘 |
|---|-----|---------|---------|------|------|--------|
| 9 | quantitative-methods | 양적연구방법 | Quantitative Methods | `/quantitative-methods` | `#1D4ED8` | `fa-square-poll-vertical` |
| 10 | qualitative-methods | 질적연구방법 | Qualitative Methods | `/qualitative-methods` | `#7E22CE` | `fa-comments` |
| 11 | ahp | AHP연구방법론 | AHP Methodology | `/ahp` | `#B45309` | `fa-layer-group` |

### 수정된 파일 (5개)

| 파일 | 변경 내용 |
|------|-----------|
| `src/config/site.ts` | `LEARNING_PATHS` 배열에 3개 항목 추가 |
| `src/components/layout/Navbar.tsx` | `NAV_ITEMS`에 3개 네비게이션 항목 추가 |
| `src/components/layout/Footer.tsx` | 빠른 링크(Quick Links)에 3개 링크 추가 |
| `src/layouts/PublicLayout.tsx` | 3개 `lazy()` import + `<Route>` 추가 |
| `src/pages/Home.tsx` | 통계 수치 업데이트: 가이드 `8+` → `11+`, 토픽 `48+` → `66+`, 카테고리 `8` → `11` |

### 신규 생성 파일 (3개)

#### 1. `src/pages/quantitative-methods/QuantitativeMethods.tsx` (1,246줄)

양적연구방법론의 전 과정을 7개 섹션으로 구성:

| 섹션 ID | 한글 | English | 아이콘 |
|---------|------|---------|--------|
| `overview` | 양적연구 개요 | Overview | `fa-book-open` |
| `experimental-design` | 실험설계 | Experimental Design | `fa-flask-vial` |
| `survey-method` | 설문조사방법 | Survey Methods | `fa-clipboard-list` |
| `sampling` | 표본추출과 표본크기 | Sampling & Sample Size | `fa-filter` |
| `data-analysis` | 양적자료분석 | Data Analysis | `fa-chart-line` |
| `paper-writing` | 양적연구 논문작성 | Paper Writing | `fa-file-pen` |
| `references` | 참고문헌 | References | `fa-book` |

**주요 콘텐츠:**
- 양적연구 패러다임 (실증주의, 연역적 접근)
- 실험설계 유형 (진실험, 준실험, 전실험)
- 설문지 설계 원칙 및 리커트 척도
- 확률/비확률 표본추출, G*Power 표본크기 산정
- 기술통계, t-검정, ANOVA, 회귀분석, SEM
- IMRaD 논문 구조 및 APA 양식
- 참고문헌 18건 (Creswell, Bryman, Field, Hair, Cohen 등)

#### 2. `src/pages/qualitative-methods/QualitativeMethods.tsx` (1,142줄)

질적연구의 주요 접근법과 분석 방법을 7개 섹션으로 구성:

| 섹션 ID | 한글 | English | 아이콘 |
|---------|------|---------|--------|
| `overview` | 질적연구 개요 | Overview | `fa-eye` |
| `grounded-theory` | 근거이론 | Grounded Theory | `fa-seedling` |
| `phenomenology` | 현상학적 연구 | Phenomenology | `fa-brain` |
| `case-study` | 사례연구 | Case Study | `fa-magnifying-glass` |
| `data-collection` | 질적자료 수집과 분석 | Data Collection & Analysis | `fa-database` |
| `trustworthiness` | 질적연구 신뢰성 확보 | Trustworthiness | `fa-shield-halved` |
| `references` | 참고문헌 | References | `fa-book` |

**주요 콘텐츠:**
- 질적연구 패러다임 (해석주의, 구성주의, 비판이론, 후기구조주의)
- Creswell의 5대 접근법 (내러티브, 현상학, 근거이론, 문화기술지, 사례연구)
- 근거이론 3대 전통 (Glaser, Strauss & Corbin, Charmaz)
- 개방코딩 → 축코딩 → 선택코딩, 패러다임 모형
- Moustakas 기술적 현상학 / van Manen 해석학적 현상학
- Yin의 사례연구 설계, Stake의 사례연구 유형
- 주제분석(Braun & Clarke), 내용분석, 담론분석
- Lincoln & Guba 신뢰성 기준 (Credibility, Transferability, Dependability, Confirmability)
- 삼각검증, 참여자 확인, 동료 검토, 반성성
- 참고문헌 22건 (Creswell, Charmaz, Glaser & Strauss, Lincoln & Guba, Yin, Moustakas 등)

#### 3. `src/pages/ahp/Ahp.tsx` (1,138줄)

AHP(분석적 계층화 과정) 방법론을 7개 섹션으로 구성:

| 섹션 ID | 한글 | English | 아이콘 |
|---------|------|---------|--------|
| `overview` | AHP 개요 | AHP Overview | `fa-circle-info` |
| `hierarchy` | 계층구조 설계 | Hierarchy Design | `fa-sitemap` |
| `pairwise` | 쌍대비교와 척도 | Pairwise Comparison | `fa-scale-balanced` |
| `consistency` | 일관성 검증 | Consistency Verification | `fa-check-double` |
| `software` | AHP 소프트웨어 활용 | Software Tools | `fa-laptop-code` |
| `paper-writing` | AHP 논문작성 | Paper Writing | `fa-file-pen` |
| `references` | 참고문헌 | References | `fa-book` |

**주요 콘텐츠:**
- AHP 개요 (Saaty, 1980), MCDM 비교 (AHP vs ANP)
- 계층구조 설계 원칙 (상호배타성, 포괄성, 독립성, 측정가능성)
- Saaty 9점 척도, 역수 속성, n(n-1)/2 비교 수
- 고유벡터법, 기하평균법, 3×3 행렬 계산 예시
- CI/RI/CR 공식, RI 테이블 (n=1~10), CR < 0.1 기준
- Expert Choice, Super Decisions, Excel, R, Python 도구 비교
- 논문 구조, 가중치 테이블, 민감도 분석
- 참고문헌 (Saaty, 조근태, Vaidya & Kumar, Ishizaka & Labib 등)

### 기술 스택

- **프레임워크:** React 19 + TypeScript
- **빌드 도구:** Vite 7.3
- **라우팅:** React Router (lazy loading)
- **다국어:** `useLanguage()` 훅 (한국어/영어)
- **배포:** GitHub Pages (gh-pages)

### 페이지 공통 패턴

모든 학습 페이지는 동일한 구조를 따름:

```
SECTIONS 배열 → 개별 Section 컴포넌트 → Main 컴포넌트
├── SEOHead (title, description)
├── guide-page > guide-layout
│   ├── guide-sidebar (목차 네비게이션)
│   └── guide-content (섹션별 조건부 렌더링)
│       ├── h2 > h3 > p, ul, ol
│       ├── table.guide-table (비교표)
│       ├── TipBox (type: tip/warning/important/danger)
│       └── guide-section-nav (이전/다음 버튼)
```

### 커밋 이력

| 해시 | 메시지 |
|------|--------|
| `48b332b` | feat: 3개 신규 학습 경로 추가 (양적연구방법, 질적연구방법, AHP연구방법론) |

### 전체 학습 경로 목록 (11개)

| # | 경로 | 한글명 | 색상 |
|---|------|--------|------|
| 1 | `/research-design` | 연구설계 | `#1E40AF` |
| 2 | `/sampling` | 표본추출 | `#7C3AED` |
| 3 | `/measurement` | 측정과 척도 | `#059669` |
| 4 | `/survey` | 설문조사법 | `#D97706` |
| 5 | `/experiment` | 실험연구 | `#DC2626` |
| 6 | `/qualitative` | 질적연구 | `#0891B2` |
| 7 | `/statistics` | 통계분석 | `#9333EA` |
| 8 | `/ethics` | 연구윤리 | `#EA580C` |
| 9 | `/quantitative-methods` | 양적연구방법 | `#1D4ED8` |
| 10 | `/qualitative-methods` | 질적연구방법 | `#7E22CE` |
| 11 | `/ahp` | AHP연구방법론 | `#B45309` |

---

## 이전 개발 이력

### 2025-04-08 — 참고문헌 추가, 푸터 개선, 파비콘

- 커밋 `368ede5`: 기존 8개 학습 페이지에 참고문헌 섹션 추가, 푸터 2열 배치 개선, 파비콘 생성

### 2025-04-07 — gh-pages 배포 설정

- 커밋 `5ac1177`: gh-pages 배포 설정, OG 이미지 추가, 테마 수정

### 2025-04-06 — 초기 구축

- 커밋 `3aa96b8`: 사회과학 조사방법론 학습 사이트 초기 구축 (8개 학습 경로)
- 커밋 `3fa5432`: package-lock.json 추가
- 커밋 `8f75739`: CNAME 설정 (research.dreamitbiz.com)
- 커밋 `2567fb9`: Initial commit
