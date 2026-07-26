# 개발 작업 흐름

## 로컬 역할

```text
C:\Users\able2\.gemini\antigravity\scratch\Portfolio
└─ 기존 HTML 프로젝트

C:\Users\able2\portfolio-react
└─ 새 React 프로젝트
```

두 저장소의 파일을 직접 섞지 않습니다. 기존 HTML의 파일이 필요하면 용도와 이름을 확인한 후 React 저장소의 규칙에 맞춰 선별 복사합니다.

## 새 기능 작업 순서

1. 로컬 `main`을 최신 상태로 맞춥니다.
2. 작업 목적에 맞는 `feature/*`, `fix/*`, `docs/*` 브랜치를 만듭니다.
3. 로컬 개발 서버에서 작업합니다.
4. 화면과 기능을 확인합니다.
5. 관련 파일만 커밋합니다.
6. 작업 브랜치를 GitHub에 푸시합니다.
7. 변경사항을 검토한 후 `beta`에 병합합니다.
8. 전체 검수가 끝난 변경만 `main`에 병합합니다.
9. 배포 결과를 확인합니다.

## React 전환 단계

### Phase 1 — 기반

- Vite + React 구성
- 라우팅과 빌드 설정
- 전역 스타일 초기화
- 디자인 토큰 작성
- 공통 레이아웃 구성

### Phase 2 — Home

- Home 구조 분석
- Header와 Navigation
- Hero 및 Home 전용 섹션
- Footer와 Contact
- 반응형과 애니메이션
- 기존 Home과 시각 비교

### Phase 3 — 공통 시스템

- Button, Card, SectionTitle 등 공통 UI 확정
- 이미지와 데이터 규칙 적용
- 페이지 레이아웃 통일
- 접근성과 성능 기준 점검

### Phase 4 — 나머지 페이지

권장 순서:

1. About
2. Projects
3. Research
4. Articles
5. Lectures
6. Awards
7. Contact
8. 상세 페이지

### Phase 5 — 공개 준비

- 전체 링크와 라우팅
- 모바일·태블릿·데스크톱
- 이미지 최적화
- 메타 태그와 공유 이미지
- 프로덕션 빌드
- `beta` 검수
- `main` 병합 및 `v2.0.0` 태그

## 작업 완료 기준

기능 구현만 끝났다고 완료로 보지 않습니다. 다음 조건을 모두 만족해야 합니다.

- 요구한 화면과 기능이 동작함
- 콘솔 오류가 없음
- 주요 반응형 화면에서 깨지지 않음
- 파일과 컴포넌트 이름이 규칙에 맞음
- 임시 파일과 사용하지 않는 에셋이 없음
- 빌드가 성공함
- 관련 문서가 현재 구현과 일치함
