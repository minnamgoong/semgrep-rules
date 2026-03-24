# Go Semgrep Rules Summary

`go` 디렉토리 하위의 규칙 목록입니다. (테스트 파일 제외)

## AWS-LAMBDA

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `database-sqli` | `WARNING` | 잠재적 SQL 인젝션 경로에 대한 검토가 필요합니다. | `security/database-sqli.yaml` |
| `tainted-sql-string` | `ERROR` | Go 보안 및 무결성 관리: tainted-sql-string 점검 처리 하세요. | `security/tainted-sql-string.yaml` |

## GORILLA

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `handler-assignment-from-multiple-sources` | `WARNING` | handler-assignment-from-multiple-sources 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/handler-assignment-from-multiple-sources.yaml` |
| `session-cookie-missing-httponly` | `WARNING` | 쿠키 보안 속성(Secure/HttpOnly) 누출 우려 점검. | `security/audit/session-cookie-missing-httponly.yaml` |
| `session-cookie-missing-secure` | `WARNING` | 쿠키 보안 속성(Secure/HttpOnly) 누출 우려 점검. | `security/audit/session-cookie-missing-secure.yaml` |
| `session-cookie-samesitenone` | `WARNING` | 쿠키 보안 속성(Secure/HttpOnly) 누출 우려 점검. | `security/audit/session-cookie-samesitenone.yaml` |
| `websocket-missing-origin-check` | `WARNING` | websocket-missing-origin-check 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/websocket-missing-origin-check.yaml` |

## GORM

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `gorm-dangerous-method-usage` | `WARNING` | 위험한 메서드 호출 피로도 점검. | `security/audit/gorm-dangerous-methods-usage.yaml` |

## GRPC

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `grpc-client-insecure-connection` | `ERROR` | Go 보안 및 무결성 관리: grpc-client-insecure-connection 점검 처리 하세요. | `security/grpc-client-insecure-connection.yaml` |
| `grpc-server-insecure-connection` | `ERROR` | Go 보안 및 무결성 관리: grpc-server-insecure-connection 점검 처리 하세요. | `security/grpc-server-insecure-connection.yaml` |

## JWT-GO

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `hardcoded-jwt-key` | `WARNING` | JWT 토큰 서명 및 디코드 검증 누사 점검. | `security/jwt.yaml` |
| `jwt-go-none-algorithm` | `ERROR` | Go 보안 및 무결성 관리: jwt-go-none-algorithm 점검 처리 하세요. | `security/jwt-none-alg.yaml` |
| `jwt-go-parse-unverified` | `WARNING` | JWT 토큰 서명 및 디코드 검증 누사 점검. | `security/audit/jwt-parse-unverified.yaml` |

## LANG

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `avoid-bind-to-all-interfaces` | `WARNING` | avoid-bind-to-all-interfaces 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/net/bind_all.yaml` |
| `avoid-ssh-insecure-ignore-host-key` | `WARNING` | 보안 옵션 누사 및 예방 단속 필요. | `security/audit/crypto/insecure_ssh.yaml` |
| `bad-tmp-file-creation` | `WARNING` | bad-tmp-file-creation 잠재적 결함 및 보안 이격율 정비 요망. | `security/bad_tmp.yaml` |
| `channel-guarded-with-mutex` | `WARNING` | channel-guarded-with-mutex 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/channel-guarded-with-mutex.yaml` |
| `cookie-missing-httponly` | `WARNING` | 쿠키 보안 속성(Secure/HttpOnly) 누출 우려 점검. | `security/audit/net/cookie-missing-httponly.yaml` |
| `cookie-missing-secure` | `WARNING` | 쿠키 보안 속성(Secure/HttpOnly) 누출 우려 점검. | `security/audit/net/cookie-missing-secure.yaml` |
| `dangerous-command-write` | `ERROR` | Go 보안 및 무결성 관리: dangerous-command-write 점검 처리 하세요. | `security/audit/dangerous-command-write.yaml` |
| `dangerous-exec-cmd` | `ERROR` | Go 보안 및 무결성 관리: dangerous-exec-cmd 점검 처리 하세요. | `security/audit/dangerous-exec-cmd.yaml` |
| `dangerous-exec-command` | `ERROR` | Go 보안 및 무결성 관리: dangerous-exec-command 점검 처리 하세요. | `security/audit/dangerous-exec-command.yaml` |
| `dangerous-syscall-exec` | `ERROR` | Go 보안 및 무결성 관리: dangerous-syscall-exec 점검 처리 하세요. | `security/audit/dangerous-syscall-exec.yaml` |
| `dynamic-httptrace-clienttrace` | `WARNING` | dynamic-httptrace-clienttrace 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/net/dynamic-httptrace-clienttrace.yaml` |
| `eqeq-is-bad` | `INFO` | hardcoded-eq-true-or-false 잠재적 결함 및 보안 이격율 정비 요망. | `correctness/useless-eqeq.yaml` |
| `exported_loop_pointer` | `WARNING` | exported_loop_pointer 잠재적 결함 및 보안 이격율 정비 요망. | `correctness/looppointer.yaml` |
| `filepath-clean-misuse` | `ERROR` | Go 보안 및 무결성 관리: filepath-clean-misuse 점검 처리 하세요. | `security/filepath-clean-misuse.yaml` |
| `formatted-template-string` | `WARNING` | formatted-template-string 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/net/formatted-template-string.yaml` |
| `fs-directory-listing` | `WARNING` | fs-directory-listing 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/net/fs-directory-listing.yaml` |
| `go-unsafe-deserialization-interface` | `WARNING` | go-unsafe-deserialization-interface 잠재적 결함 및 보안 이격율 정비 요망. | `security/deserialization/unsafe-deserialization-interface.yaml` |
| `gosql-sqli` | `ERROR` | Go Lang 다이렉트 SQL 쿼리 가압 단의 인젝션 우려 탑승. | `security/audit/sqli/gosql-sqli.yaml` |
| `hidden-goroutine` | `WARNING` | hidden-goroutine 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/hidden-goroutine.yaml` |
| `import-text-template` | `WARNING` | import-text-template 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/xss/import-text-template.yaml` |
| `incorrect-default-permission` | `WARNING` | incorrect-default-permission 잠재적 결함 및 보안 이격율 정비 요망. | `correctness/permissions/file_permission.yaml` |
| `insecure-module-used` | `WARNING` | 보안 옵션 누사 및 예방 단속 필요. | `security/audit/crypto/bad_imports.yaml` |
| `integer-overflow-int16` | `WARNING` | integer-overflow-int32 잠재적 결함 및 보안 이격율 정비 요망. | `correctness/overflow/overflow.yaml` |
| `math-random-used` | `WARNING` | math-random-used 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/crypto/math_random.yaml` |
| `md5-used-as-password` | `WARNING` | md5-used-as-password 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/md5-used-as-password.yaml` |
| `missing-ssl-minversion` | `WARNING` | missing-ssl-minversion 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/crypto/missing-ssl-minversion.yaml` |
| `no-direct-write-to-responsewriter` | `WARNING` | no-direct-write-to-responsewriter 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/xss/no-direct-write-to-responsewriter.yaml` |
| `no-fprintf-to-responsewriter` | `WARNING` | no-fprintf-to-responsewriter 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/xss/no-fprintf-to-responsewriter.yaml` |
| `no-interpolation-in-tag` | `WARNING` | no-interpolation-in-tag 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/xss/no-interpolation-in-tag.yaml` |
| `no-interpolation-js-template-string` | `WARNING` | no-interpolation-js-template-string 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/xss/no-interpolation-js-template-string.yaml` |
| `no-io-writestring-to-responsewriter` | `WARNING` | no-io-writestring-to-responsewriter 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/xss/no-io-writestring-to-responsewriter.yaml` |
| `no-printf-in-responsewriter` | `WARNING` | no-printf-in-responsewriter 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/xss/no-printf-in-responsewriter.yaml` |
| `open-redirect` | `WARNING` | open-redirect 잠재적 결함 및 보안 이격율 정비 요망. | `security/injection/open-redirect.yaml` |
| `parsing-external-entities-enabled` | `WARNING` | parsing-external-entities-enabled 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/xxe/parsing-external-entities-enabled.yaml` |
| `path-traversal-inside-zip-extraction` | `WARNING` | path-traversal-inside-zip-extraction 잠재적 결함 및 보안 이격율 정비 요망. | `security/zip.yaml` |
| `pg-orm-sqli` | `ERROR` | Go Lang 다이렉트 SQL 쿼리 가압 단의 인젝션 우려 탑승. | `security/audit/sqli/pg-orm-sqli.yaml` |
| `pg-sqli` | `ERROR` | Go Lang 다이렉트 SQL 쿼리 가압 단의 인젝션 우려 탑승. | `security/audit/sqli/pg-sqli.yaml` |
| `pgx-sqli` | `ERROR` | Go Lang 다이렉트 SQL 쿼리 가압 단의 인젝션 우려 탑승. | `security/audit/sqli/pgx-sqli.yaml` |
| `potential-dos-via-decompression-bomb` | `WARNING` | potential-dos-via-decompression-bomb 잠재적 결함 및 보안 이격율 정비 요망. | `security/decompression_bomb.yaml` |
| `pprof-debug-exposure` | `WARNING` | pprof-debug-exposure 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/net/pprof.yaml` |
| `raw-html-format` | `WARNING` | HTML 템플릿 가속 피싱 대응. | `security/injection/raw-html-format.yaml` |
| `reflect-makefunc` | `ERROR` | Go 보안 및 무결성 관리: reflect-makefunc 점검 처리 하세요. | `security/audit/reflect-makefunc.yaml` |
| `reverseproxy-director` | `WARNING` | reverseproxy-director 잠재적 결함 및 보안 이격율 정비 요망. | `security/reverseproxy-director.yaml` |
| `sha224-hash` | `WARNING` | sha224-hash 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/crypto/sha224-hash.yaml` |
| `shared-url-struct-mutation` | `WARNING` | shared-url-struct-mutation 잠재적 결함 및 보안 이격율 정비 요망. | `security/shared-url-struct-mutation.yaml` |
| `ssl-v3-is-insecure` | `WARNING` | 보안 옵션 누사 및 예방 단속 필요. | `security/audit/crypto/ssl.yaml` |
| `string-formatted-query` | `WARNING` | string-formatted-query 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/database/string-formatted-query.yaml` |
| `tainted-sql-string` | `ERROR` | Go 보안 및 무결성 관리: tainted-sql-string 점검 처리 하세요. | `security/injection/tainted-sql-string.yaml` |
| `tainted-url-host` | `WARNING` | tainted-url-host 잠재적 결함 및 보안 이격율 정비 요망. | `security/injection/tainted-url-host.yaml` |
| `tls-with-insecure-cipher` | `WARNING` | 보안 옵션 누사 및 예방 단속 필요. | `security/audit/crypto/tls.yaml` |
| `unescaped-data-in-htmlattr` | `WARNING` | unescaped-data-in-htmlattr 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/net/unescaped-data-in-htmlattr.yaml` |
| `unescaped-data-in-js` | `WARNING` | unescaped-data-in-js 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/net/unescaped-data-in-js.yaml` |
| `unescaped-data-in-url` | `WARNING` | unescaped-data-in-url 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/net/unescaped-data-in-url.yaml` |
| `unsafe-reflect-by-name` | `WARNING` | unsafe-reflect-by-name 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/unsafe-reflect-by-name.yaml` |
| `unsafe-template-type` | `WARNING` | unsafe-template-type 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/xss/template-html-does-not-escape.yaml` |
| `use-filepath-join` | `WARNING` | use-filepath-join 잠재적 결함 및 보안 이격율 정비 요망. | `correctness/use-filepath-join.yaml` |
| `use-of-md5` | `WARNING` | use-of-md5 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/crypto/use_of_weak_crypto.yaml` |
| `use-of-unsafe-block` | `WARNING` | use-of-unsafe-block 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/unsafe.yaml` |
| `use-of-weak-rsa-key` | `WARNING` | use-of-weak-rsa-key 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/crypto/use_of_weak_rsa_key.yaml` |
| `use-tls` | `WARNING` | use-tls 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/net/use-tls.yaml` |
| `useless-if-conditional` | `WARNING` | useless-if-body 잠재적 결함 및 보안 이격율 정비 요망. | `maintainability/useless-ifelse.yaml` |
| `wip-xss-using-responsewriter-and-printf` | `WARNING` | wip-xss-using-responsewriter-and-printf 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/net/wip-xss-using-responsewriter-and-printf.yaml` |

## OTTO

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `dangerous-execution` | `ERROR` | Go 보안 및 무결성 관리: dangerous-execution 점검 처리 하세요. | `security/audit/dangerous-execution.yaml` |

## TEMPLATE

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `go-insecure-templates` | `WARNING` | 보안 옵션 누사 및 예방 단속 필요. | `security/insecure-types.yaml` |
| `go-ssti` | `ERROR` | Go 보안 및 무결성 관리: go-ssti 점검 처리 하세요. | `security/ssti.yaml` |
