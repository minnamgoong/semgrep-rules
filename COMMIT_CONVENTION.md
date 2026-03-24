# 📝 커밋 컨벤션 가이드 (Commit Convention Guide)

이 프로젝트는 변경사항을 추적하고 가독성을 높이기 위해 **Conventional Commits** 규격을 따릅니다. 모든 커밋 메시지는 아래 규칙을 준수해 주세요.

---

## 📌 기본 형식 (Structure)

```text
<type>(<scope>): <subject>

<body>
<footer>
```

*   **`<type>`**: 커밋의 성격 (필수)
*   **`<scope>`**: 영향을 받는 모듈 또는 영역 (선택, 예: `java`, `spring`, `ci`)
*   **`<subject>`**: 변경 사항에 대한 짧은 설명 (필수, 한글/영어 모두 가능)

---

## 🏷️ 커밋 타입 (Commit Types)

| 타입 (Type) | 의미 (Meaning) | 예시 (Example) |
| :--- | :--- | :--- |
| **`feat`** | 새로운 기능 또는 규칙 추가 | `feat(java): 신규 암호화 검증 규칙 추가` |
| **`fix`** | 버그, 오탐(False Positive) 수정 | `fix(spring): SQL 인젝션 규칙 패턴 정교화` |
| **`docs`** | 문서 작성 및 수정 (`.md`, 주석 등) | `docs: COMMIT_CONVENTION.md 가이드 추가` |
| **`style`** | 코드 포맷팅, 스타일 수정 (로직 영향 없음) | `style: 들여쓰기 공백 및 오타 수정` |
| **`refactor`** | 구조적 리팩토링 (기능 추가/수정 없음) | `refactor: 중복 분석 패스 코드 분할` |
| **`test`** | 테스트 코드 추가 및 수정 | `test(go): 신규 API 탐지 테스트용 코드 보강` |
| **`perf`** | 성능 최적화 | `perf: 파일 순회 시 스레드 병렬성 개선` |
| **`build`** | 빌드 시스템, 라이브러리 의존성 변경 | `build: python yaml 라이브러리 버전 갱신` |
| **`ci`** | GitHub Actions, GitLab CI 등 CI 설정 | `ci: Pull Request 시 분석 자동화 워크플로 추가` |
| **`chore`** | 중요 로직이 없는 기타 잡무 처리 | `chore: 불필요한 예비 디렉토리 제거` |
| **`info`** | 정보성 변경 (번역 등) | `info(java): 규칙 설명 한글 번역 업데이트` |
| **`revert`** | 이전 합병/커밋 단위 되돌리기 | `revert: "feat: 신규 API ..." 커밋 복구` |

---

## 💡 작성 팁 (Tips)
1.  **제목(Subject)** 끝에 마침표(`.`)를 찍지 않습니다.
2.  **본문(Body)**과 **꼬리말(Footer)**은 가독성을 위해 한 줄을 띄우고 작성합니다.
3.  **Breaking Change**(하위 호환성이 깨지는 변경)가 있을 경우 타입 뒤에 **`!`**를 붙입니다. 
    *   *예시: `refactor!(java): 핵심 분석 엔진 파이프라인 전면 교체`*
