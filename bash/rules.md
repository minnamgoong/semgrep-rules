# Bash Semgrep Rules Summary

`bash` 디렉토리 하위의 규칙 목록입니다. (테스트 파일 제외)

## CURL

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `curl-eval` | `WARNING` | curl-eval 잠재적 결함 및 보안 이격율 정비 요망. | `security/curl-eval.yaml` |
| `curl-pipe-bash` | `WARNING` | curl-pipe-bash 잠재적 결함 및 보안 이격율 정비 요망. | `security/curl-pipe-bash.yaml` |

## LANG

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `ifs-tampering` | `WARNING` | ifs-tampering 잠재적 결함 및 보안 이격율 정비 요망. | `security/ifs-tampering.yaml` |
| `iteration-over-ls-output` | `WARNING` | iteration-over-ls-output 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/iteration-over-ls-output.yaml` |
| `unquoted-variable-expansion-in-command` | `INFO` | unquoted-command-substitution-in-command 잠재적 결함 및 보안 이격율 정비 요망. | `correctness/unquoted-expansion.yaml` |
| `useless-cat` | `WARNING` | useless-cat 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/useless-cat.yaml` |
