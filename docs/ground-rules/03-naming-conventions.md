# 파일명과 코드 이름 규칙

## 공통 원칙

- 이름만 보고 역할과 내용을 예상할 수 있어야 합니다.
- `final`, `new`, `temp`, `copy`, 날짜만 붙인 이름은 사용하지 않습니다.
- 같은 종류의 파일은 같은 규칙을 적용합니다.
- 약어는 널리 이해되는 경우에만 사용합니다.

## 폴더 이름

영문 소문자 `kebab-case`를 사용합니다.

```text
home/
project-gallery/
ground-rules/
```

## React 컴포넌트

파일명과 컴포넌트 이름 모두 `PascalCase`를 사용하며 서로 일치시킵니다.

```text
Header.jsx              → function Header()
ProjectCard.jsx         → function ProjectCard()
HomePage.jsx            → function HomePage()
HeroSection.jsx         → function HeroSection()
```

하나의 컴포넌트 파일은 기본적으로 하나의 대표 컴포넌트를 내보냅니다.

## Hook

`use`로 시작하는 `camelCase`를 사용합니다.

```text
useMediaQuery.js
useScrollPosition.js
useOutsideClick.js
```

## 일반 JavaScript와 데이터

역할이 드러나는 `camelCase`를 사용합니다.

```text
formatDate.js
projectData.js
articleCategories.js
```

여러 상수만 보관하는 파일은 용도를 명확히 표현합니다.

```text
routes.js
designTokens.js
socialLinks.js
```

## CSS

전역 역할 파일은 영문 소문자 `kebab-case`를 사용합니다.

```text
design-tokens.css
typography.css
globals.css
```

컴포넌트 전용 CSS는 컴포넌트와 동일한 `PascalCase` 이름을 사용합니다.

```text
ProjectCard.jsx
ProjectCard.css
```

CSS 클래스는 `kebab-case`를 사용하고 의미 기반으로 작성합니다.

```css
.project-card {}
.project-card__title {}
.project-card--featured {}
```

색상이나 위치만 설명하는 이름은 피합니다.

```text
권장: project-card__title
비권장: orange-text, left-box
```

## 이미지와 영상

모든 에셋 파일은 영문 소문자 `kebab-case`를 사용합니다.

```text
home-hero-team.webp
project-hopzie-thumbnail.webp
award-japan-government.webp
article-ai-accessibility-cover.webp
```

권장 형식:

```text
[영역]-[콘텐츠]-[용도].[확장자]
```

반응형 또는 크기 변형이 실제로 필요하면 마지막에 규격을 붙입니다.

```text
home-hero-team-mobile.webp
home-hero-team-desktop.webp
profile-nahyun-640.webp
profile-nahyun-1280.webp
```

다음 이름은 사용하지 않습니다.

```text
image1.png
new-image-final.png
uploaded_media_12345.png
수정본2.png
```

## 문서

일반 문서는 영문 소문자 `kebab-case`를 사용합니다. 읽는 순서가 중요한 문서 묶음에만 숫자 접두사를 사용합니다.

```text
README.md
01-repository-and-branching.md
02-directory-structure.md
```

## Boolean과 이벤트 이름

Boolean 값은 상태를 질문처럼 읽을 수 있게 작성합니다.

```text
isOpen
isLoading
hasError
canNavigate
```

이벤트 처리 함수는 `handle`로 시작합니다.

```text
handleMenuOpen
handleProjectSelect
handleFormSubmit
```
