# Yaml Semgrep Rules Summary

`yaml` 디렉토리 하위의 규칙 목록입니다. (테스트 파일 제외)

## ARGO
\n| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `argo-workflow-parameter-command-injection` | `ERROR` | Argo 워크플로우 매개변수 가동 중 원격 명령어 주입(Command Injection) 우려가 수렴됩니다. | `security/argo-workflow-parameter-command-injection.yaml` |
\n## GITHUB-ACTIONS
\n| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `curl-eval` | `ERROR` | curl-eval 보안 인젝션 및 런타임 버그 전사 예방 점검. | `security/curl-eval.yaml` |
| `detect-shai-hulud-backdoor` | `ERROR` | detect-shai-hulud-backdoor 보안 인젝션 및 런타임 버그 전사 예방 점검. | `security/detect-shai-hulud-backdoor.yaml` |
| `github-script-injection` | `ERROR` | github-script-injection 보안 인젝션 및 런타임 버그 전사 예방 점검. | `security/github-script-injection.yaml` |
| `run-shell-injection` | `ERROR` | run-shell-injection 보안 인젝션 및 런타임 버그 전사 예방 점검. | `security/run-shell-injection.yaml` |
\n## OPENAPI
\n| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `use-of-basic-authentication` | `ERROR` | use-of-basic-authentication 보안 인젝션 및 런타임 버그 전사 예방 점검. | `security/use-of-basic-authentication.yaml` |
\n## SEMGREP
\n| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `- id: duplicate-id` | `ERROR` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `duplicate-id.yaml` |
| `duplicate-pattern` | `ERROR` | Semgrep 규칙 저작 메타 데이터 정합성 점검: duplicate-pattern 누락 경보. | `duplicate-pattern.yaml` |
| `metadata-cwe` | `ERROR` | Semgrep 규칙 저작 메타 데이터 정합성 점검: metadata-cwe 누락 경보. | `metadata-cwe.yaml` |
| `metadata-cwe-prohibited-or-discouraged` | `ERROR` | Semgrep 규칙 저작 메타 데이터 정합성 점검: metadata-cwe-prohibited-or-discouraged 누락 경보. | `metadata-cwe-prohibited-or-discouraged.yaml` |
| `metadata-license` | `ERROR` | Semgrep 규칙 저작 메타 데이터 정합성 점검: metadata-license 누락 경보. | `metadata-license.yaml` |
| `metadata-owasp` | `ERROR` | Semgrep 규칙 저작 메타 데이터 정합성 점검: metadata-owasp 누락 경보. | `metadata-owasp.yaml` |
| `metadata-references` | `ERROR` | Semgrep 규칙 저작 메타 데이터 정합성 점검: metadata-references 누락 경보. | `metadata-references.yaml` |
| `unsatisfiable-rule` | `ERROR` | Semgrep 규칙 저작 메타 데이터 정합성 점검: unsatisfiable-rule 누락 경보. | `unsatisfiable.yaml` |
