# 🤝 협업 가이드

본 프로젝트는 FE, BE, AI 파트가 하나의 Repository에서 협업합니다.

---

## 🌿 Branch 전략

### 주요 브랜치

- `main` : 최종 배포 및 제출 브랜치
- `develop` : 개발 통합 브랜치

`main`, `develop` 브랜치에는 직접 Push하지 않습니다.

### 작업 브랜치

모든 작업 브랜치는 `develop`에서 생성합니다.

브랜치명은 다음 형식을 사용합니다.

`파트/이슈번호-작업명`

예시:

- `fe/12-login-page`
- `be/13-login-api`
- `ai/15-image-analysis`

작업 완료 후 `develop` 브랜치로 Pull Request를 생성합니다.

---

## 📝 Commit 규칙

커밋 메시지는 다음 형식을 사용합니다.

`타입: 작업 내용`

### Commit Type

| Type | 설명 |
|------|------|
| `feat` | 새로운 기능 추가 |
| `fix` | 버그 수정 |
| `refactor` | 코드 리팩토링 |
| `docs` | 문서 수정 |
| `test` | 테스트 코드 추가 및 수정 |
| `chore` | 환경 설정 및 기타 작업 |
| `style` | 코드 포맷 및 스타일 수정 |

예시:

`feat: 로그인 API 구현`

`fix: 이미지 분석 응답 오류 수정`

`docs: API 명세 수정`

### Commit 원칙

- 하나의 커밋에는 하나의 논리적인 변경만 포함합니다.
- `수정`, `최종`, `진짜 최종`과 같이 의미를 알 수 없는 메시지는 사용하지 않습니다.

---

## 📌 Issue 규칙

작업 시작 전 Issue를 생성합니다.

Issue 제목은 다음 형식을 사용합니다.

`[파트] 작업 내용`

예시:

- `[FE] 로그인 페이지 구현`
- `[BE] 로그인 API 구현`
- `[AI] 이미지 분석 기능 구현`

생성된 Issue 번호를 작업 브랜치명에 사용합니다.

예:

Issue `#15`

→ `ai/15-image-analysis`

---

## 🔀 Pull Request 규칙

작업 완료 후 자신의 작업 브랜치에서 `develop`으로 PR을 생성합니다.

예:

`ai/15-image-analysis` → `develop`

PR 제목은 다음 형식을 사용합니다.

`[파트] #이슈번호 작업 내용`

예:

`[AI] #15 이미지 분석 기능 구현`

PR 본문에 관련 Issue를 연결합니다.

`Closes #15`

PR Merge 전 최소 1명의 팀원에게 리뷰를 받습니다.

---

## 🔄 Merge 규칙

일반적인 개발 작업은 다음 순서로 진행합니다.

`작업 브랜치 → develop → main`

1. 작업 브랜치에서 개발
2. `develop`으로 PR 생성
3. 코드 리뷰
4. `develop`에 Merge
5. FE / BE / AI 통합 테스트
6. 최종 확인 후 `develop` → `main` PR 생성

`main`에는 개발이 완료되고 정상 동작이 확인된 코드만 Merge합니다.

작업이 완료된 브랜치는 Merge 후 삭제합니다.

---

## ⚠️ 주의사항

- `main`, `develop` 직접 Push 금지
- 다른 파트의 코드를 임의로 수정하지 않기
- 큰 변경사항은 작업 전 Issue 또는 팀 회의를 통해 공유하기
- API 명세 변경 시 관련 파트에 반드시 공유하기
- Merge Conflict 발생 시 관련 작업자와 확인 후 해결하기
