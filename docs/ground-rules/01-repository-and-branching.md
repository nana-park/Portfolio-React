# 저장소와 브랜치 운영

## 저장소 역할

### `nana-park/Portfolio`

- 기존 HTML 포트폴리오의 원본과 이력을 보존합니다.
- React 개발을 위해 기존 파일을 덮어쓰거나 대규모로 재배치하지 않습니다.
- React 사이트가 완전히 검수되기 전까지 기존 운영 사이트의 기준입니다.

### `nana-park/Portfolio-React`

- React로 재구축하는 모든 소스 코드와 문서를 관리합니다.
- HTML 저장소의 파일은 필요한 것만 선별하여 복사합니다.
- 기존 저장소의 임시 파일, 백업 이미지, 수정 스크립트를 통째로 가져오지 않습니다.

## 영구 브랜치

### `main`

- 언제든 배포할 수 있는 안정 버전만 둡니다.
- 로컬에서 직접 기능 개발하지 않습니다.
- 테스트되지 않은 변경을 직접 푸시하지 않습니다.

### `beta`

- 여러 기능을 합쳐 전체 화면을 검수하는 통합 브랜치입니다.
- `stage/`, `beta/`, `production/`과 같은 환경별 복제 폴더를 만들지 않습니다.
- React 최초 골격이 준비된 후 생성합니다.

## 작업 브랜치

작업은 `main` 또는 팀에서 정한 기준 브랜치에서 새 브랜치를 만들어 시작합니다.

- `feature/home-design-system`
- `feature/about-page`
- `feature/project-card`
- `fix/mobile-navigation`
- `docs/update-ground-rules`
- `chore/update-dependencies`

한 브랜치에는 하나의 목적만 포함합니다.

## 병합 흐름

일반적인 기능 개발은 다음 순서를 따릅니다.

```text
feature/* → beta → main
```

- `feature/*`에서 개별 기능을 구현하고 확인합니다.
- `beta`에서 여러 페이지와 반응형 동작을 함께 검수합니다.
- 안정성이 확인된 변경만 `main`으로 병합합니다.
- 긴급 수정은 `fix/*`에서 처리하되, 수정 내용을 `beta`에도 반영합니다.

## 커밋 규칙

커밋은 작고 되돌릴 수 있는 단위로 작성합니다.

```text
feat: add home hero section
fix: correct mobile navigation overflow
docs: update asset naming rules
style: align project card spacing
refactor: extract shared section header
chore: update build configuration
```

완성되지 않은 서로 다른 작업을 하나의 커밋에 섞지 않습니다.
