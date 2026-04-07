# Go Semgrep Rules Summary

`go` 디렉토리 하위의 규칙 목록입니다. (테스트 파일 제외)

## AWS-LAMBDA

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `- id: database-sqli` | `WARNING` | 잠재적 SQL 인젝션 경로에 대한 검토가 필요합니다. | `security/database-sqli.yaml` |
| `tainted-sql-string` | `ERROR` | Go 보안 및 무결성 관리: tainted-sql-string 점검 처리 하세요. | `security/tainted-sql-string.yaml` |

## GORILLA

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `- id: handler-assignment-from-multiple-sources` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/handler-assignment-from-multiple-sources.yaml` |
| `- id: session-cookie-missing-httponly` | `WARNING` | 쿠키 보안 속성(Secure/HttpOnly) 누출 우려 점검. | `security/audit/session-cookie-missing-httponly.yaml` |
| `- id: session-cookie-missing-secure` | `WARNING` | 쿠키 보안 속성(Secure/HttpOnly) 누출 우려 점검. | `security/audit/session-cookie-missing-secure.yaml` |
| `- id: session-cookie-samesitenone` | `WARNING` | 쿠키 보안 속성(Secure/HttpOnly) 누출 우려 점검. | `security/audit/session-cookie-samesitenone.yaml` |
| `- id: websocket-missing-origin-check` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/websocket-missing-origin-check.yaml` |

## GORM

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `- id: gorm-dangerous-method-usage` | `WARNING` | 위험한 메서드 호출 피로도 점검. | `security/audit/gorm-dangerous-methods-usage.yaml` |

## GRPC

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `grpc-client-insecure-connection` | `ERROR` | Go 보안 및 무결성 관리: grpc-client-insecure-connection 점검 처리 하세요. | `security/grpc-client-insecure-connection.yaml` |
| `grpc-server-insecure-connection` | `ERROR` | Go 보안 및 무결성 관리: grpc-server-insecure-connection 점검 처리 하세요. | `security/grpc-server-insecure-connection.yaml` |

## JWT-GO

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `- id: hardcoded-jwt-key` | `WARNING` | JWT 토큰 서명 및 디코드 검증 누락 여부 점검. | `security/jwt.yaml` |
| `jwt-go-none-algorithm` | `ERROR` | Go 보안 및 무결성 관리: jwt-go-none-algorithm 점검 처리 하세요. | `security/jwt-none-alg.yaml` |
| `- id: jwt-go-parse-unverified` | `WARNING` | JWT 토큰 서명 및 디코드 검증 누락 여부 점검. | `security/audit/jwt-parse-unverified.yaml` |

## LANG

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `- id: avoid-bind-to-all-interfaces` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/net/bind_all.yaml` |
| `- id: avoid-ssh-insecure-ignore-host-key` | `WARNING` | 보안 옵션 누사 및 예방 단속 필요. | `security/audit/crypto/insecure_ssh.yaml` |
| `- id: bad-tmp-file-creation` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/bad_tmp.yaml` |
| `channel-guarded-with-mutex` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/channel-guarded-with-mutex.yaml` |
| `- id: cookie-missing-httponly` | `WARNING` | 쿠키 보안 속성(Secure/HttpOnly) 누출 우려 점검. | `security/audit/net/cookie-missing-httponly.yaml` |
| `- id: cookie-missing-secure` | `WARNING` | 쿠키 보안 속성(Secure/HttpOnly) 누출 우려 점검. | `security/audit/net/cookie-missing-secure.yaml` |
| `dangerous-command-write` | `ERROR` | Go 보안 및 무결성 관리: dangerous-command-write 점검 처리 하세요. | `security/audit/dangerous-command-write.yaml` |
| `dangerous-exec-cmd` | `ERROR` | Go 보안 및 무결성 관리: dangerous-exec-cmd 점검 처리 하세요. | `security/audit/dangerous-exec-cmd.yaml` |
| `dangerous-exec-command` | `ERROR` | Go 보안 및 무결성 관리: dangerous-exec-command 점검 처리 하세요. | `security/audit/dangerous-exec-command.yaml` |
| `dangerous-syscall-exec` | `ERROR` | Go 보안 및 무결성 관리: dangerous-syscall-exec 점검 처리 하세요. | `security/audit/dangerous-syscall-exec.yaml` |
| `- id: dynamic-httptrace-clienttrace` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/net/dynamic-httptrace-clienttrace.yaml` |
| `eqeq-is-bad` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `correctness/useless-eqeq.yaml` |
| `exported_loop_pointer` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `correctness/looppointer.yaml` |
| `filepath-clean-misuse` | `ERROR` | Go 보안 및 무결성 관리: filepath-clean-misuse 점검 처리 하세요. | `security/filepath-clean-misuse.yaml` |
| `- id: formatted-template-string` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/net/formatted-template-string.yaml` |
| `- id: fs-directory-listing` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/net/fs-directory-listing.yaml` |
| `go-unsafe-deserialization-interface` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/deserialization/unsafe-deserialization-interface.yaml` |
| `gosql-sqli` | `ERROR` | Go Lang 다이렉트 SQL 쿼리 가압 단의 인젝션 우려 탑승. | `security/audit/sqli/gosql-sqli.yaml` |
| `hidden-goroutine` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/hidden-goroutine.yaml` |
| `- id: import-text-template` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/xss/import-text-template.yaml` |
| `incorrect-default-permission` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `correctness/permissions/file_permission.yaml` |
| `- id: insecure-module-used` | `WARNING` | 보안 옵션 누사 및 예방 단속 필요. | `security/audit/crypto/bad_imports.yaml` |
| `integer-overflow-int16` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `correctness/overflow/overflow.yaml` |
| `- id: math-random-used` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/crypto/math_random.yaml` |
| `- id: md5-used-as-password` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/md5-used-as-password.yaml` |
| `- id: missing-ssl-minversion` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/crypto/missing-ssl-minversion.yaml` |
| `- id: no-direct-write-to-responsewriter` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/xss/no-direct-write-to-responsewriter.yaml` |
| `- id: no-fprintf-to-responsewriter` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/xss/no-fprintf-to-responsewriter.yaml` |
| `- id: no-interpolation-in-tag` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/xss/no-interpolation-in-tag.yaml` |
| `- id: no-interpolation-js-template-string` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/xss/no-interpolation-js-template-string.yaml` |
| `- id: no-io-writestring-to-responsewriter` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/xss/no-io-writestring-to-responsewriter.yaml` |
| `- id: no-printf-in-responsewriter` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/xss/no-printf-in-responsewriter.yaml` |
| `open-redirect` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/injection/open-redirect.yaml` |
| `- id: parsing-external-entities-enabled` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/xxe/parsing-external-entities-enabled.yaml` |
| `- id: path-traversal-inside-zip-extraction` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/zip.yaml` |
| `pg-orm-sqli` | `ERROR` | Go Lang 다이렉트 SQL 쿼리 가압 단의 인젝션 우려 탑승. | `security/audit/sqli/pg-orm-sqli.yaml` |
| `pg-sqli` | `ERROR` | Go Lang 다이렉트 SQL 쿼리 가압 단의 인젝션 우려 탑승. | `security/audit/sqli/pg-sqli.yaml` |
| `pgx-sqli` | `ERROR` | Go Lang 다이렉트 SQL 쿼리 가압 단의 인젝션 우려 탑승. | `security/audit/sqli/pgx-sqli.yaml` |
| `- id: potential-dos-via-decompression-bomb` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/decompression_bomb.yaml` |
| `- id: pprof-debug-exposure` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/net/pprof.yaml` |
| `- id: raw-html-format` | `WARNING` | HTML 템플릿 가속 피싱 대응. | `security/injection/raw-html-format.yaml` |
| `reflect-makefunc` | `ERROR` | Go 보안 및 무결성 관리: reflect-makefunc 점검 처리 하세요. | `security/audit/reflect-makefunc.yaml` |
| `- id: reverseproxy-director` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/reverseproxy-director.yaml` |
| `- id: sha224-hash` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/crypto/sha224-hash.yaml` |
| `- id: shared-url-struct-mutation` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/shared-url-struct-mutation.yaml` |
| `- id: ssl-v3-is-insecure` | `WARNING` | 보안 옵션 누사 및 예방 단속 필요. | `security/audit/crypto/ssl.yaml` |
| `- id: string-formatted-query` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/database/string-formatted-query.yaml` |
| `tainted-sql-string` | `ERROR` | Go 보안 및 무결성 관리: tainted-sql-string 점검 처리 하세요. | `security/injection/tainted-sql-string.yaml` |
| `tainted-url-host` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/injection/tainted-url-host.yaml` |
| `- id: tls-with-insecure-cipher` | `WARNING` | 보안 옵션 누사 및 예방 단속 필요. | `security/audit/crypto/tls.yaml` |
| `- id: unescaped-data-in-htmlattr` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/net/unescaped-data-in-htmlattr.yaml` |
| `- id: unescaped-data-in-js` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/net/unescaped-data-in-js.yaml` |
| `- id: unescaped-data-in-url` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/net/unescaped-data-in-url.yaml` |
| `- id: unsafe-reflect-by-name` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/unsafe-reflect-by-name.yaml` |
| `- id: unsafe-template-type` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/xss/template-html-does-not-escape.yaml` |
| `use-filepath-join` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `correctness/use-filepath-join.yaml` |
| `- id: use-of-md5` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/crypto/use_of_weak_crypto.yaml` |
| `- id: use-of-unsafe-block` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/unsafe.yaml` |
| `- id: use-of-weak-rsa-key` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/crypto/use_of_weak_rsa_key.yaml` |
| `- id: use-tls` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/net/use-tls.yaml` |
| `useless-if-conditional` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `maintainability/useless-ifelse.yaml` |
| `- id: wip-xss-using-responsewriter-and-printf` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/net/wip-xss-using-responsewriter-and-printf.yaml` |

## OTTO

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `dangerous-execution` | `ERROR` | Go 보안 및 무결성 관리: dangerous-execution 점검 처리 하세요. | `security/audit/dangerous-execution.yaml` |

## TEMPLATE

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `- id: go-insecure-templates` | `WARNING` | 보안 옵션 누사 및 예방 단속 필요. | `security/insecure-types.yaml` |
| `go-ssti` | `ERROR` | Go 보안 및 무결성 관리: go-ssti 점검 처리 하세요. | `security/ssti.yaml` |
