# Go Semgrep Rules Summary

`go` 디렉토리 하위의 규칙 목록입니다. (테스트 파일 제외)

## AWS-LAMBDA
\n| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `tainted-sql-string` | `ERROR` | Go 보안 및 무결성 관리: tainted-sql-string 점검 처리 하세요. | `security/tainted-sql-string.yaml` |
\n## GRPC
\n| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `grpc-client-insecure-connection` | `ERROR` | Go 보안 및 무결성 관리: grpc-client-insecure-connection 점검 처리 하세요. | `security/grpc-client-insecure-connection.yaml` |
| `grpc-server-insecure-connection` | `ERROR` | Go 보안 및 무결성 관리: grpc-server-insecure-connection 점검 처리 하세요. | `security/grpc-server-insecure-connection.yaml` |
\n## JWT-GO
\n| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `jwt-go-none-algorithm` | `ERROR` | Go 보안 및 무결성 관리: jwt-go-none-algorithm 점검 처리 하세요. | `security/jwt-none-alg.yaml` |
\n## LANG
\n| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `dangerous-command-write` | `ERROR` | Go 보안 및 무결성 관리: dangerous-command-write 점검 처리 하세요. | `security/audit/dangerous-command-write.yaml` |
| `dangerous-exec-cmd` | `ERROR` | Go 보안 및 무결성 관리: dangerous-exec-cmd 점검 처리 하세요. | `security/audit/dangerous-exec-cmd.yaml` |
| `dangerous-exec-command` | `ERROR` | Go 보안 및 무결성 관리: dangerous-exec-command 점검 처리 하세요. | `security/audit/dangerous-exec-command.yaml` |
| `dangerous-syscall-exec` | `ERROR` | Go 보안 및 무결성 관리: dangerous-syscall-exec 점검 처리 하세요. | `security/audit/dangerous-syscall-exec.yaml` |
| `filepath-clean-misuse` | `ERROR` | Go 보안 및 무결성 관리: filepath-clean-misuse 점검 처리 하세요. | `security/filepath-clean-misuse.yaml` |
| `gosql-sqli` | `ERROR` | Go Lang 다이렉트 SQL 쿼리 가압 단의 인젝션 우려 탑승. | `security/audit/sqli/gosql-sqli.yaml` |
| `pg-orm-sqli` | `ERROR` | Go Lang 다이렉트 SQL 쿼리 가압 단의 인젝션 우려 탑승. | `security/audit/sqli/pg-orm-sqli.yaml` |
| `pg-sqli` | `ERROR` | Go Lang 다이렉트 SQL 쿼리 가압 단의 인젝션 우려 탑승. | `security/audit/sqli/pg-sqli.yaml` |
| `pgx-sqli` | `ERROR` | Go Lang 다이렉트 SQL 쿼리 가압 단의 인젝션 우려 탑승. | `security/audit/sqli/pgx-sqli.yaml` |
| `reflect-makefunc` | `ERROR` | Go 보안 및 무결성 관리: reflect-makefunc 점검 처리 하세요. | `security/audit/reflect-makefunc.yaml` |
| `tainted-sql-string` | `ERROR` | Go 보안 및 무결성 관리: tainted-sql-string 점검 처리 하세요. | `security/injection/tainted-sql-string.yaml` |
\n## OTTO
\n| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `dangerous-execution` | `ERROR` | Go 보안 및 무결성 관리: dangerous-execution 점검 처리 하세요. | `security/audit/dangerous-execution.yaml` |
\n## TEMPLATE
\n| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `go-ssti` | `ERROR` | Go 보안 및 무결성 관리: go-ssti 점검 처리 하세요. | `security/ssti.yaml` |
