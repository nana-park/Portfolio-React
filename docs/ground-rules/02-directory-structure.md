# 폴더 구조

## 기본 원칙

- 환경별로 소스 폴더를 복제하지 않습니다.
- 공통 UI, 페이지, 기능, 데이터, 스타일과 에셋의 역할을 분리합니다.
- 특정 페이지에서만 사용하는 코드는 해당 페이지 가까이에 둡니다.
- 두 곳 이상에서 실제로 재사용할 때 공통 영역으로 이동합니다.

## 목표 구조

```text
Portfolio-React/
├─ docs/
│  └─ ground-rules/
├─ public/
│  ├─ favicon/
│  ├─ fonts/
│  └─ static/
├─ src/
│  ├─ app/
│  │  ├─ App.jsx
│  │  ├─ router.jsx
│  │  └─ providers.jsx
│  ├─ assets/
│  │  ├─ icons/
│  │  ├─ images/
│  │  └─ videos/
│  ├─ components/
│  │  ├─ layout/
│  │  └─ ui/
│  ├─ data/
│  ├─ features/
│  ├─ hooks/
│  ├─ pages/
│  ├─ styles/
│  │  ├─ reset.css
│  │  ├─ tokens.css
│  │  ├─ typography.css
│  │  ├─ animations.css
│  │  └─ globals.css
│  ├─ utils/
│  └─ main.jsx
├─ .gitignore
├─ index.html
├─ package.json
└─ vite.config.js
```

## 영역별 역할

### `docs/`

개발 및 운영 규칙과 설계 결정을 보관합니다. 실제 화면에서 불러오는 콘텐츠는 두지 않습니다.

### `public/`

빌드 과정에서 변환할 필요 없이 주소가 그대로 유지되어야 하는 파일을 둡니다. 파비콘, 공유 이미지, 정적 다운로드 파일 등이 대상입니다.

### `src/assets/`

컴포넌트에서 import하여 사용하는 이미지, 아이콘과 영상을 둡니다.

### `src/components/ui/`

Button, Tag, SectionTitle처럼 여러 화면에서 재사용하는 작은 UI를 둡니다.

### `src/components/layout/`

Header, Navigation, Footer, Container처럼 페이지 구조를 구성하는 공통 컴포넌트를 둡니다.

### `src/pages/`

라우트 단위의 화면을 둡니다. Home 전용 섹션은 다음처럼 Home 페이지 안에서 관리합니다.

```text
src/pages/home/
├─ HomePage.jsx
├─ HomePage.css
└─ sections/
   ├─ HeroSection.jsx
   ├─ HistorySection.jsx
   └─ VisionSection.jsx
```

### `src/features/`

여러 컴포넌트와 상태, 데이터 처리가 함께 필요한 독립 기능을 둡니다. 예: article-filter, project-gallery, contact-form.

### `src/data/`

프로젝트, 경력, 아티클처럼 코드와 분리된 구조화 콘텐츠를 둡니다.

### `src/styles/`

사이트 전체 디자인 토큰과 전역 스타일만 둡니다. 페이지 전용 스타일을 전역 파일에 계속 추가하지 않습니다.

## 금지 구조

다음과 같은 중복 폴더는 만들지 않습니다.

```text
stage/
beta/
production/
backup/
final/
final-new/
real-final/
```

환경과 버전은 Git 브랜치, 커밋과 태그로 구분합니다.
