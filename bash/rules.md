# Bash Semgrep Rules Summary

`bash` 디렉토리 하위의 규칙 목록입니다. (테스트 파일 제외)

## CURL

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `curl-eval` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/curl-eval.yaml` |
| `curl-pipe-bash` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/curl-pipe-bash.yaml` |

## LANG

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `ifs-tampering` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/ifs-tampering.yaml` |
| `iteration-over-ls-output` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/iteration-over-ls-output.yaml` |
| `unquoted-variable-expansion-in-command` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `correctness/unquoted-expansion.yaml` |
| `useless-cat` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/useless-cat.yaml` |
