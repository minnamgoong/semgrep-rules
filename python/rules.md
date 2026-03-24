# Python Semgrep Rules Summary

`python` 디렉토리 하위의 규칙 목록입니다. (테스트 파일 제외)

## AIRFLOW

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `formatted-string-bashoperator` | `ERROR` | BashOperator 내부 가동 인자에 가변 합사가 포착되었습니다. 외부 주입 우려 노출을 전사 단속하십시오. | `security/audit/formatted-string-bashoperator.yaml` |

## ATTR

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `attr-mutable-initializer` | `WARNING` | attr-mutable-initializer 잠재적 결함 및 보안 이격율 정비 요망. | `correctness/mutable-initializer.yaml` |

## AWS-LAMBDA

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `5.2.4` | `ERROR` | os 모듈 가동에 event 오염 인자가 유입됩니다. 인젝션 위험이 극에 달하므로 subprocess를 고용하세요. | `security/dangerous-system-call.yaml` |
| `5.2.4` | `WARNING` | tainted-code-exec 잠재적 결함 및 보안 이격율 정비 요망. | `security/tainted-code-exec.yaml` |
| `5.3.8` | `ERROR` | asyncio 쉘 연산에 가변 인자가 합사되었습니다. 명령어 주입 우려가 있으니 shlex 세척을 권장합니다. | `security/dangerous-asyncio-shell.yaml` |
| `5.3.8` | `ERROR` | subprocess 구동 시 shell=True 탑재 탑재로 보안 이탈율이 높습니다. 가변 인자 결합을 철회하십시오. | `security/dangerous-subprocess-use.yaml` |
| `5.3.8` | `ERROR` | os 바이너리 스폰 가동에 event 가변 오염이 흐릅니다. 쉘 명령어 덤프 RCE 차단을 위해 전사 단속하십시오. | `security/dangerous-spawn-process.yaml` |
| `5.3.8` | `ERROR` | create_subprocess_exec 버퍼에 외부 데이터 합치기가 발견되었습니다. 인젝션 예방을 위해 필터링 하세요. | `security/dangerous-asyncio-create-exec.yaml` |
| `5.3.8` | `ERROR` | subprocess_exec 가동 시 유저 리스트 오염 인자가 흐릅니다. 가변 탑재를 배제하십시오. | `security/dangerous-asyncio-exec.yaml` |
| `dynamodb-filter-injection` | `ERROR` | DynamoDB 쿼리 필터에 $EVENT 유입 인자가 도주합니다. NoSQL 인젝션 예방을 위해 정적 할당 하십시오. | `security/dynamodb-filter-injection.yaml` |
| `mysql-sqli` | `WARNING` | 잠재적 SQL 인젝션 경로에 대한 검토가 필요합니다. | `security/mysql-sqli.yaml` |
| `psycopg-sqli` | `WARNING` | 잠재적 SQL 인젝션 경로에 대한 검토가 필요합니다. | `security/psycopg-sqli.yaml` |
| `pymssql-sqli` | `WARNING` | 잠재적 SQL 인젝션 경로에 대한 검토가 필요합니다. | `security/pymssql-sqli.yaml` |
| `pymysql-sqli` | `WARNING` | 잠재적 SQL 인젝션 경로에 대한 검토가 필요합니다. | `security/pymysql-sqli.yaml` |
| `sqlalchemy-sqli` | `WARNING` | 잠재적 SQL 인젝션 경로에 대한 검토가 필요합니다. | `security/sqlalchemy-sqli.yaml` |
| `tainted-html-response` | `WARNING` | HTML 템플릿 가속 피싱 대응. | `security/tainted-html-response.yaml` |
| `tainted-html-string` | `WARNING` | tainted-html-string 잠재적 결함 분기 정비 요망. | `security/tainted-html-string.yaml` |
| `tainted-pickle-deserialization` | `WARNING` | tainted-pickle-deserialization 잠재적 결함 및 보안 이격율 정비 요망. | `security/tainted-pickle-deserialization.yaml` |
| `tainted-sql-string` | `ERROR` | Lambda 가동 내 동적 SQL 조립이 탐지되었습니다. Parameterized Query를 사용하여 요인을 차단하십시오. | `security/tainted-sql-string.yaml` |

## BOKEH

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `bokeh-deprecated-apis` | `WARNING` | bokeh-deprecated-apis 잠재적 결함 및 보안 이격율 정비 요망. | `maintainability/deprecated/deprecated_apis.yaml` |

## BOTO3

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `hardcoded-token` | `WARNING` | hardcoded-token 잠재적 결함 및 보안 이격율 정비 요망. | `security/hardcoded-token.yaml` |

## CLICK

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `use-click-secho` | `ERROR` | click.echo()와 style() 수동 배합 대신 click.secho() 연쇄 고용을 권장합니다. | `best-practice/echo-style.yaml` |

## CORRECTNESS

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `check-is-none-explicitly` | `WARNING` | check-is-none-explicitly 잠재적 결함 및 보안 이격율 정비 요망. | `check-is-none-explicitly.yaml` |
| `socket-shutdown-close` | `WARNING` | socket-shutdown-close 잠재적 결함 및 보안 이격율 정비 요망. | `socket-shutdown-close.yaml` |
| `suppressed-exception-handling-finally-break` | `WARNING` | suppressed-exception-handling-finally-break 잠재적 결함 및 보안 이격율 정비 요망. | `suppressed-exception-handling-finally-break.yaml` |

## CRYPTOGRAPHY

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `crypto-mode-without-authentication` | `ERROR` | 무결성 검증 없는 암호화 운영 모드가 사용되었습니다. GCM 등 AEAD 모드로 교정하세요. | `security/mode-without-authentication.yaml` |
| `empty-aes-key` | `WARNING` | empty-aes-key 잠재적 결함 및 보안 이격율 정비 요망. | `security/empty-aes-key.yaml` |
| `insecure-cipher-algorithm-arc4` | `WARNING` | 보안 옵션 누사 및 예방 단속 필요. | `security/insecure-cipher-algorithms-arc4.yaml` |
| `insecure-cipher-algorithm-blowfish` | `WARNING` | 보안 옵션 누사 및 예방 단속 필요. | `security/insecure-cipher-algorithms-blowfish.yaml` |
| `insecure-cipher-algorithm-idea` | `WARNING` | 보안 옵션 누사 및 예방 단속 필요. | `security/insecure-cipher-algorithms.yaml` |
| `insecure-cipher-mode-ecb` | `WARNING` | 보안 옵션 누사 및 예방 단속 필요. | `security/insecure-cipher-mode-ecb.yaml` |
| `insecure-hash-algorithm-md5` | `WARNING` | 보안 옵션 누사 및 예방 단속 필요. | `security/insecure-hash-algorithms-md5.yaml` |
| `insecure-hash-algorithm-sha1` | `WARNING` | 보안 옵션 누사 및 예방 단속 필요. | `security/insecure-hash-algorithms.yaml` |
| `insufficient-dsa-key-size` | `WARNING` | insufficient-dsa-key-size 잠재적 결함 및 보안 이격율 정비 요망. | `security/insufficient-dsa-key-size.yaml` |
| `insufficient-ec-key-size` | `WARNING` | insufficient-ec-key-size 잠재적 결함 및 보안 이격율 정비 요망. | `security/insufficient-ec-key-size.yaml` |
| `insufficient-rsa-key-size` | `WARNING` | insufficient-rsa-key-size 잠재적 결함 및 보안 이격율 정비 요망. | `security/insufficient-rsa-key-size.yaml` |

## DISTRIBUTED

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `require-encryption` | `WARNING` | require-encryption 잠재적 결함 및 보안 이격율 정비 요망. | `security.yaml` |

## DJANGO

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `access-foreign-keys` | `WARNING` | access-foreign-keys 잠재적 결함 및 보안 이격율 정비 요망. | `performance/access-foreign-keys.yaml` |
| `avoid-insecure-deserialization` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 avoid-insecure-deserialization 전사 단속이 요구됩니다. | `security/audit/avoid-insecure-deserialization.yaml` |
| `avoid-mark-safe` | `WARNING` | avoid-mark-safe 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/avoid-mark-safe.yaml` |
| `avoid-query-set-extra` | `WARNING` | avoid-query-set-extra 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/query-set-extra.yaml` |
| `avoid-raw-sql` | `WARNING` | avoid-raw-sql 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/raw-query.yaml` |
| `class-extends-safestring` | `WARNING` | class-extends-safestring 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/xss/class-extends-safestring.yaml` |
| `command-injection-os-system` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 command-injection-os-system 전사 단속이 요구됩니다. | `security/injection/command/command-injection-os-system.yaml` |
| `conflicting-path-assignment` | `ERROR` | path for `$URL` is uselessly assigned twice | `maintainability/duplicate-path-assignment.yaml` |
| `context-autoescape-off` | `WARNING` | context-autoescape-off 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/xss/context-autoescape-off.yaml` |
| `csv-writer-injection` | `ERROR` | CSV 가동 인자 인젝션 방어를 조율 하십시오. | `security/injection/csv-writer-injection.yaml` |
| `custom-expression-as-sql` | `WARNING` | custom-expression-as-sql 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/custom-expression-as-sql.yaml` |
| `debug-template-tag` | `WARNING` | debug-template-tag 잠재적 결함 분기 정비 요망. | `security/audit/templates/debug-template-tag.yaml` |
| `direct-use-of-httpresponse` | `WARNING` | direct-use-of-httpresponse 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/xss/direct-use-of-httpresponse.yaml` |
| `django-compat-2_0-signals-weak` | `WARNING` | The weak argument to django.dispatch.signals.Signal.disconnect() is removed in D... | `compatibility/django-2_0-compat.yaml` |
| `django-db-model-save-super` | `WARNING` | django-db-model-save-super 잠재적 결함 및 보안 이격율 정비 요망. | `correctness/model-save.yaml` |
| `django-no-csrf-token` | `WARNING` | django-no-csrf-token 잠재적 결함 및 보안 이격율 정비 요망. | `security/django-no-csrf-token.yaml` |
| `django-secure-set-cookie` | `WARNING` | django-secure-set-cookie 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/secure-cookies.yaml` |
| `django-using-request-post-after-is-valid` | `WARNING` | django-using-request-post-after-is-valid 잠재적 결함 및 보안 이격율 정비 요망. | `security/django-using-request-post-after-is-valid.yaml` |
| `extends-custom-expression` | `WARNING` | extends-custom-expression 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/extends-custom-expression.yaml` |
| `filter-with-is-safe` | `WARNING` | filter-with-is-safe 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/xss/filter-with-is-safe.yaml` |
| `formathtml-fstring-parameter` | `WARNING` | HTML 템플릿 가속 피싱 대응. | `security/audit/xss/formathtml-fstring-parameter.yaml` |
| `global-autoescape-off` | `WARNING` | global-autoescape-off 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/xss/global-autoescape-off.yaml` |
| `globals-as-template-context` | `ERROR` | globals() 전역 인출 피칭 국면을 경보합니다. | `security/globals-as-template-context.yaml` |
| `globals-misuse-code-execution` | `WARNING` | globals-misuse-code-execution 잠재적 결함 및 보안 이격율 정비 요망. | `security/injection/code/globals-misuse-code-execution.yaml` |
| `hashids-with-django-secret` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 hashids-with-django-secret 전사 단속이 요구됩니다. | `security/hashids-with-django-secret.yaml` |
| `html-magic-method` | `WARNING` | HTML 템플릿 가속 피싱 대응. | `security/audit/xss/html-magic-method.yaml` |
| `html-safe` | `WARNING` | HTML 템플릿 가속 피싱 대응. | `security/audit/xss/html-safe.yaml` |
| `locals-as-template-context` | `ERROR` | locals() 직접 전사로 내부 탑재 변수가 외부에 탈주 폭주하는 위험 레이어를 점검합니다. | `security/locals-as-template-context.yaml` |
| `mass-assignment` | `WARNING` | mass-assignment 잠재적 결함 분기 정비 요망. | `security/injection/mass-assignment.yaml` |
| `missing-throttle-config` | `WARNING` | missing-throttle-config 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/django-rest-framework/missing-throttle-config.yaml` |
| `nan-injection` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 nan-injection 전사 단속이 요구됩니다. | `security/nan-injection.yaml` |
| `no-csrf-exempt` | `WARNING` | no-csrf-exempt 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/csrf-exempt.yaml` |
| `no-null-string-field` | `ERROR` | Avoid using null on string-based fields such as CharField and TextField. If a st... | `correctness/string-field-null-checks.yaml` |
| `nontext-field-must-set-null-true` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 nontext-field-must-set-null-true 전사 단속이 요구됩니다. | `correctness/nontext-field-must-set-null-true.yaml` |
| `open-redirect` | `WARNING` | open-redirect 잠재적 결함 및 보안 이격율 정비 요망. | `security/injection/open-redirect.yaml` |
| `password-empty-string` | `ERROR` | 빈 문자열로 패스워드가 세팅되는 안티 무방비 보안 지점을 진압합니다. | `security/passwords/password-empty-string.yaml` |
| `path-traversal-file-name` | `WARNING` | path-traversal-file-name 잠재적 결함 및 보안 이격율 정비 요망. | `security/injection/path-traversal/path-traversal-file-name.yaml` |
| `path-traversal-join` | `WARNING` | path-traversal-join 잠재적 결함 및 보안 이격율 정비 요망. | `security/injection/path-traversal/path-traversal-join.yaml` |
| `path-traversal-open` | `WARNING` | path-traversal-open 잠재적 결함 및 보안 이격율 정비 요망. | `security/injection/path-traversal/path-traversal-open.yaml` |
| `raw-html-format` | `WARNING` | raw-html-format 잠재적 결함 분기 정비 요망. | `security/injection/raw-html-format.yaml` |
| `reflected-data-httpresponse` | `WARNING` | reflected-data-httpresponse 잠재적 결함 및 보안 이격율 정비 요망. | `security/injection/reflected-data-httpresponse.yaml` |
| `reflected-data-httpresponsebadrequest` | `WARNING` | reflected-data-httpresponsebadrequest 잠재적 결함 및 보안 이격율 정비 요망. | `security/injection/reflected-data-httpresponsebadrequest.yaml` |
| `request-data-fileresponse` | `WARNING` | request-data-fileresponse 잠재적 결함 및 보안 이격율 정비 요망. | `security/injection/request-data-fileresponse.yaml` |
| `request-data-write` | `WARNING` | request-data-write 잠재적 결함 및 보안 이격율 정비 요망. | `security/injection/request-data-write.yaml` |
| `sql-injection-db-cursor-execute` | `WARNING` | sql-injection-db-cursor-execute 잠재적 결함 및 보안 이격율 정비 요망. | `security/injection/sql/sql-injection-using-db-cursor-execute.yaml` |
| `sql-injection-using-extra-where` | `WARNING` | sql-injection-using-extra-where 잠재적 결함 및 보안 이격율 정비 요망. | `security/injection/sql/sql-injection-extra.yaml` |
| `sql-injection-using-raw` | `WARNING` | sql-injection-using-raw 잠재적 결함 및 보안 이격율 정비 요망. | `security/injection/sql/sql-injection-using-raw.yaml` |
| `sql-injection-using-rawsql` | `WARNING` | sql-injection-using-rawsql 잠재적 결함 및 보안 이격율 정비 요망. | `security/injection/sql/sql-injection-rawsql.yaml` |
| `ssrf-injection-requests` | `ERROR` | 서버 측 요청 위조(SSRF) 누출 피싱 주소 교정. | `security/injection/ssrf/ssrf-injection-requests.yaml` |
| `ssrf-injection-urllib` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 ssrf-injection-urllib 전사 단속이 요구됩니다. | `security/injection/ssrf/ssrf-injection-urllib.yaml` |
| `subprocess-injection` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 subprocess-injection 전사 단속이 요구됩니다. | `security/injection/command/subprocess-injection.yaml` |
| `tainted-sql-string` | `ERROR` | 동적 SQL 문자열 결합 유출이 포착되어 Parameterized 쿼리를 독촉합니다. | `security/injection/tainted-sql-string.yaml` |
| `tainted-url-host` | `WARNING` | tainted-url-host 잠재적 결함 및 보안 이격율 정비 요망. | `security/injection/tainted-url-host.yaml` |
| `template-autoescape-off` | `WARNING` | template-autoescape-off 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/xss/template-autoescape-off.yaml` |
| `template-blocktranslate-no-escape` | `INFO` | template-blocktranslate-no-escape 잠재적 결함 분기 정비 요망. | `security/audit/xss/template-blocktranslate-no-escape.yaml` |
| `template-translate-as-no-escape` | `INFO` | template-translate-as-no-escape 잠재적 결함 분기 정비 요망. | `security/audit/xss/template-translate-as-no-escape.yaml` |
| `template-var-unescaped-with-safeseq` | `WARNING` | template-var-unescaped-with-safeseq 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/xss/template-var-unescaped-with-safeseq.yaml` |
| `unvalidated-password` | `WARNING` | unvalidated-password 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/unvalidated-password.yaml` |
| `use-count-method` | `ERROR` | .count() 헬퍼 가동으로 쿼리 집계 가속을 도모 하세요. | `performance/upsell-count.yaml` |
| `use-decimalfield-for-money` | `ERROR` | 금액 필드에 부동 소수점 오차를 막기 위해 DecimalField를 사수 하십시오. | `correctness/use-decimalfield-for-money.yaml` |
| `use-django-environ` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 use-django-environ 전사 단속이 요구됩니다. | `best-practice/upsell_django_environ.yaml` |
| `use-earliest-or-latest` | `ERROR` | use-earliest-or-latest 보안 인젝션 및 런타임 버그 전사 예방 점검. | `performance/upsell_earliest_latest.yaml` |
| `use-json-response` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 use-json-response 전사 단속이 요구됩니다. | `best-practice/json_response.yaml` |
| `use-none-for-password-default` | `ERROR` | 비밀번호 기본 데이터에 무효 인자 바인딩을 권장합니다. | `security/passwords/use-none-for-password-default.yaml` |
| `use-onetoonefield` | `WARNING` | use-onetoonefield 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/use-onetoonefield.yaml` |
| `user-eval` | `WARNING` | user-eval 잠재적 결함 및 보안 이격율 정비 요망. | `security/injection/code/user-eval.yaml` |
| `user-eval-format-string` | `WARNING` | user-eval-format-string 잠재적 결함 및 보안 이격율 정비 요망. | `security/injection/code/user-eval-format-string.yaml` |
| `user-exec` | `WARNING` | user-exec 잠재적 결함 및 보안 이격율 정비 요망. | `security/injection/code/user-exec.yaml` |
| `user-exec-format-string` | `WARNING` | user-exec-format-string 잠재적 결함 및 보안 이격율 정비 요망. | `security/injection/code/user-exec-format-string.yaml` |
| `xss-html-email-body` | `WARNING` | HTML 템플릿 가속 피싱 대응. | `security/injection/email/xss-html-email-body.yaml` |
| `xss-send-mail-html-message` | `WARNING` | HTML 템플릿 가속 피싱 대응. | `security/injection/email/xss-send-mail-html-message.yaml` |

## DOCKER

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `docker-arbitrary-container-run` | `WARNING` | docker-arbitrary-container-run 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/docker-arbitrary-container-run.yaml` |

## FASTAPI

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `wildcard-cors` | `WARNING` | wildcard-cors 잠재적 결함 및 보안 이격율 정비 요망. | `security/wildcard-cors.yaml` |

## FLASK

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `avoid-accessing-request-in-wrong-handler` | `WARNING` | avoid-accessing-request-in-wrong-handler 잠재적 결함 및 보안 이격율 정비 요망. | `correctness/access-request-in-wrong-handler.yaml` |
| `avoid_app_run_with_bad_host` | `WARNING` | avoid_app_run_with_bad_host 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/app-run-param-config.yaml` |
| `avoid_hardcoded_config_TESTING` | `WARNING` | avoid_hardcoded_config_TESTING 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/hardcoded-config.yaml` |
| `avoid_send_file_without_path_sanitization` | `WARNING` | avoid_send_file_without_path_sanitization 잠재적 결함 및 보안 이격율 정비 요망. | `security/secure-static-file-serve.yaml` |
| `avoid_using_app_run_directly` | `WARNING` | avoid_using_app_run_directly 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/app-run-security-config.yaml` |
| `csv-writer-injection` | `ERROR` | 내장 csv 모듈에 검증 실종 동동 데이터를 공급 중입니다. 매크로 주입 방어를 위해 특수 서식 이격을 거치세요. | `security/injection/csv-writer-injection.yaml` |
| `dangerous-template-string` | `ERROR` | 가변 스트링 합사를 통한 동적 템플릿 생산이 잡혔습니다. SSTI 예방을 위해 객체 렌더링 양식을 쓰세요. | `security/dangerous-template-string.yaml` |
| `debug-enabled` | `WARNING` | debug-enabled 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/debug-enabled.yaml` |
| `direct-use-of-jinja2` | `WARNING` | direct-use-of-jinja2 잠재적 결함 및 보안 이격율 정비 요망. | `security/xss/audit/direct-use-of-jinja2.yaml` |
| `directly-returned-format-string` | `WARNING` | directly-returned-format-string 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/directly-returned-format-string.yaml` |
| `eval-injection` | `ERROR` | eval() 연산 버퍼에 가변 사용자 동적 연산 입력이 관여합니다. 원격 코드 실행(RCE) 타격을 유발하므로 즉각 피하십시오. | `security/injection/user-eval.yaml` |
| `exec-injection` | `ERROR` | exec() 연산 버퍼에 가변 사용자 동적 인가 데이터가 합사됩니다. RCE 극심한 타격이 상존하니 중지하십시오. | `security/injection/user-exec.yaml` |
| `explicit-unescape-with-markup` | `WARNING` | explicit-unescape-with-markup 잠재적 결함 및 보안 이격율 정비 요망. | `security/xss/audit/explicit-unescape-with-markup.yaml` |
| `flask-api-method-string-format` | `ERROR` | 컨트롤러 연산에 유저 가변 문자열이 수동 가압됩니다. 인젝션 등 우회 타격 부재를 조심하십시오. | `security/flask-api-method-string-format.yaml` |
| `flask-cache-query-string` | `WARNING` | flask-cache-query-string 잠재적 결함 및 보안 이격율 정비 요망. | `caching/query-string.yaml` |
| `flask-class-method-get-side-effects` | `WARNING` | flask-class-method-get-side-effects 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/get-class-method-with-side-effects.yaml` |
| `flask-cors-misconfiguration` | `WARNING` | flask-cors-misconfiguration 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/flask-cors-misconfiguration.yaml` |
| `flask-deprecated-apis` | `WARNING` | flask-deprecated-apis 잠재적 결함 및 보안 이격율 정비 요망. | `maintainability/deprecated/deprecated-apis.yaml` |
| `flask-duplicate-handler-name` | `WARNING` | flask-duplicate-handler-name 잠재적 결함 및 보안 이격율 정비 요망. | `correctness/same-handler-name.yaml` |
| `flask-url-for-external-true` | `WARNING` | flask-url-for-external-true 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/flask-url-for-external-true.yaml` |
| `flask-wtf-csrf-disabled` | `WARNING` | flask-wtf-csrf-disabled 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/wtf-csrf-disabled.yaml` |
| `hashids-with-flask-secret` | `ERROR` | Flask SECRET_KEY를 HashIDs Salt로 오용했습니다. 해시 파싱 중 무력화 위협이 있으니 전용 값을 할당하세요. | `security/hashids-with-flask-secret.yaml` |
| `host-header-injection-python` | `INFO` | host-header-injection-python 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/host-header-injection-python.yaml` |
| `insecure-deserialization` | `ERROR` | 취약한 역직렬화 라이브러리가 감지되었습니다. RCE 공격 위험을 막기 위해 JSON 등 안전한 형태를 이용하세요. | `security/insecure-deserialization.yaml` |
| `make-response-with-unknown-content` | `WARNING` | make-response-with-unknown-content 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/xss/make-response-with-unknown-content.yaml` |
| `nan-injection` | `ERROR` | 유저 입력이 typecast(float 등) 안으로 직접 유출됩니다. 데이터 연산 우회 조작이 발견될 수 있으니 검사하세요. | `security/injection/nan-injection.yaml` |
| `open-redirect` | `ERROR` | 외부 유입 주소 파라미터가 가공 없이 redirect()로 유출됩니다. 오픈 리디렉션 피싱 방지를 위해 사전 검출 검사하세요. | `security/open-redirect.yaml` |
| `os-system-injection` | `ERROR` | os.system() 가승 연산 버퍼에 동적 조합이 도칩니다. Command Injection 피싱 격량을 타개하기 위해 철회하십시오. | `security/injection/os-system-injection.yaml` |
| `path-traversal-open` | `ERROR` | open() 가동에 유저 노출 경로 데이터가 전사됩니다. 로컬 파일 시스템 탈취를 막고자 사전에 정적 이격 시키세요. | `security/injection/path-traversal-open.yaml` |
| `raw-html-format` | `WARNING` | raw-html-format 잠재적 결함 분기 정비 요망. | `security/injection/raw-html-concat.yaml` |
| `render-template-string` | `WARNING` | render-template-string 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/render-template-string.yaml` |
| `response-contains-unsanitized-input` | `WARNING` | response-contains-unsanitized-input 잠재적 결함 및 보안 이격율 정비 요망. | `security/unsanitized-input.yaml` |
| `secure-set-cookie` | `WARNING` | secure-set-cookie 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/secure-set-cookie.yaml` |
| `ssrf-requests` | `ERROR` | HTTP 발송 인자에 오염 입력이 통과 탑재됩니다. SSRF 탈취를 예방하기 위해 조율 주소를 엄밀하게 교정하세요. | `security/injection/ssrf-requests.yaml` |
| `subprocess-injection` | `ERROR` | subprocess 가동 인자에 가변 오염 입력이 포착되었습니다. 커맨드 인젝션 격퇴를 위해 파라미터 분할 배열형을 고수하십시오. | `security/injection/subprocess-injection.yaml` |
| `tainted-sql-string` | `ERROR` | 동적 SQL 문자열 결합이 포착되었습니다. SQL Injection 배후 차단을 위해 Parameterized Query를 사수하세요. | `security/injection/tainted-sql-string.yaml` |
| `tainted-url-host` | `WARNING` | tainted-url-host 잠재적 결함 및 보안 이격율 정비 요망. | `security/injection/tainted-url-host.yaml` |
| `template-autoescape-off` | `WARNING` | template-autoescape-off 잠재적 결함 및 보안 이격율 정비 요망. | `security/xss/audit/template-autoescape-off.yaml` |
| `template-unescaped-with-safe` | `WARNING` | template-unescaped-with-safe 잠재적 결함 및 보안 이격율 정비 요망. | `security/xss/audit/template-unescaped-with-safe.yaml` |
| `template-unquoted-attribute-var` | `WARNING` | template-unquoted-attribute-var 잠재적 결함 및 보안 이격율 정비 요망. | `security/xss/audit/template-unquoted-attribute-var.yaml` |
| `unescaped-template-extension` | `WARNING` | unescaped-template-extension 잠재적 결함 및 보안 이격율 정비 요망. | `security/unescaped-template-extension.yaml` |
| `use-jsonify` | `ERROR` | 수동 딕셔너리 연계 반환보다 flask.jsonify() 내장 헬퍼를 이용하여 안정성을 유치할 것을 권합합니다. | `best-practice/use-jsonify.yaml` |

## JINJA2

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `incorrect-autoescape-disabled` | `WARNING` | incorrect-autoescape-disabled 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/autoescape-disabled-false.yaml` |
| `missing-autoescape-disabled` | `WARNING` | missing-autoescape-disabled 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/missing-autoescape-disabled.yaml` |

## JWT

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `jwt-python-exposed-credentials` | `ERROR` | JWT 토큰 페이로드에 기밀 정보가 노출되었습니다. 페이로드는 암호화되지 않으므로 유출 위험이 큽니다. | `security/jwt-exposed-credentials.yaml` |
| `jwt-python-exposed-data` | `WARNING` | JWT 토큰 서명 및 디코드 검증 누사 점검. | `security/audit/jwt-exposed-data.yaml` |
| `jwt-python-hardcoded-secret` | `ERROR` | 하드코딩된 JWT 비밀키가 발견되었습니다. 보안 누출 예방을 위해 환경 변수나 보안 저장소로 이전하세요. | `security/jwt-hardcode.yaml` |
| `jwt-python-none-alg` | `ERROR` | JWT 서명 검증에서 none 알고리즘 사용이 감지되었습니다. 변조 토큰 우회를 피하기 위해 명시적 암호화를 지정하세요. | `security/jwt-none-alg.yaml` |
| `unverified-jwt-decode` | `ERROR` | JWT 디코딩 시 verify=False 플래그가 발견되었습니다. 무결성 검증을 위해 누출 옵션을 활성화하십시오. | `security/unverified-jwt-decode.yaml` |

## LANG

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `5.2.4` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 dangerous-system-call 전사 단속이 요구됩니다. | `security/dangerous-system-call.yaml` |
| `5.2.4` | `WARNING` | exec-detected 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/exec-detected.yaml` |
| `5.2.4` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 dangerous-system-call-audit 전사 단속이 요구됩니다. | `security/audit/dangerous-system-call-audit.yaml` |
| `5.2.4` | `WARNING` | eval-detected 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/eval-detected.yaml` |
| `5.2.4` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 dangerous-system-call-tainted-env-args 전사 단속이 요구됩니다. | `security/audit/dangerous-system-call-tainted-env-args.yaml` |
| `5.2.4` | `WARNING` | dynamic-urllib-use-detected 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/dynamic-urllib-use-detected.yaml` |
| `5.3.8` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 dangerous-os-exec 전사 단속이 요구됩니다. | `security/dangerous-os-exec.yaml` |
| `5.3.8` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 dangerous-subprocess-use 전사 단속이 요구됩니다. | `security/dangerous-subprocess-use.yaml` |
| `5.3.8` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 dangerous-spawn-process 전사 단속이 요구됩니다. | `security/dangerous-spawn-process.yaml` |
| `5.3.8` | `ERROR` | 비동기 쉘 가압에 세척 누사가 엿보입니다. | `security/audit/dangerous-asyncio-shell-tainted-env-args.yaml` |
| `5.3.8` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 dangerous-asyncio-shell-audit 전사 단속이 요구됩니다. | `security/audit/dangerous-asyncio-shell-audit.yaml` |
| `5.3.8` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 dangerous-asyncio-create-exec-audit 전사 단속이 요구됩니다. | `security/audit/dangerous-asyncio-create-exec-audit.yaml` |
| `5.3.8` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 dangerous-os-exec-tainted-env-args 전사 단속이 요구됩니다. | `security/audit/dangerous-os-exec-tainted-env-args.yaml` |
| `5.3.8` | `ERROR` | 하위 프로세스 생성 드라이버 인젝션 전담 점검. | `security/audit/dangerous-subprocess-use-audit.yaml` |
| `5.3.8` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 dangerous-subprocess-use-tainted-env-args 전사 단속이 요구됩니다. | `security/audit/dangerous-subprocess-use-tainted-env-args.yaml` |
| `5.3.8` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 dangerous-asyncio-exec-tainted-env-args 전사 단속이 요구됩니다. | `security/audit/dangerous-asyncio-exec-tainted-env-args.yaml` |
| `5.3.8` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 dangerous-os-exec-audit 전사 단속이 요구됩니다. | `security/audit/dangerous-os-exec-audit.yaml` |
| `5.3.8` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 dangerous-spawn-process-tainted-env-args 전사 단속이 요구됩니다. | `security/audit/dangerous-spawn-process-tainted-env-args.yaml` |
| `5.3.8` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 dangerous-spawn-process-audit 전사 단속이 요구됩니다. | `security/audit/dangerous-spawn-process-audit.yaml` |
| `5.3.8` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 dangerous-asyncio-create-exec-tainted-env-args 전사 단속이 요구됩니다. | `security/audit/dangerous-asyncio-create-exec-tainted-env-args.yaml` |
| `5.3.8` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 dangerous-asyncio-exec-audit 전사 단속이 요구됩니다. | `security/audit/dangerous-asyncio-exec-audit.yaml` |
| `6.2.2` | `WARNING` | 보안 옵션 누사 및 예방 단속 필요. | `security/insecure-hash-function.yaml` |
| `6.3.2` | `WARNING` | 보안 옵션 누사 및 예방 단속 필요. | `security/insecure-uuid-version.yaml` |
| `9.1.1` | `INFO` | request-with-http 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/insecure-transport/requests/request-with-http.yaml` |
| `9.1.1` | `INFO` | request-session-with-http 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/insecure-transport/requests/request-session-with-http.yaml` |
| `9.1.3` | `WARNING` | weak-ssl-version 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/weak-ssl-version.yaml` |
| `9.1.3` | `WARNING` | no-set-ciphers 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/insecure-transport/ssl/no-set-ciphers.yaml` |
| `9.2.1` | `INFO` | request-session-http-in-with-context 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/insecure-transport/requests/request-session-http-in-with-context.yaml` |
| `aiopg-sqli` | `WARNING` | 잠재적 SQL 인젝션 경로에 대한 검토가 필요합니다. | `security/audit/sqli/aiopg-sqli.yaml` |
| `arbitrary-sleep` | `ERROR` | 가동 루프 내 sleep 병목 지점을 확인하세요. | `best-practice/sleep.yaml` |
| `asyncpg-sqli` | `WARNING` | 잠재적 SQL 인젝션 경로에 대한 검토가 필요합니다. | `security/audit/sqli/asyncpg-sqli.yaml` |
| `avoid-bind-to-all-interfaces` | `INFO` | avoid-bind-to-all-interfaces 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/network/bind.yaml` |
| `avoid-jsonpickle` | `WARNING` | avoid-jsonpickle 잠재적 결함 및 보안 이격율 정비 요망. | `security/deserialization/avoid-jsonpickle.yaml` |
| `avoid-pickle` | `WARNING` | avoid-pickle 잠재적 결함 및 보안 이격율 정비 요망. | `security/deserialization/pickle.yaml` |
| `avoid-pyyaml-load` | `ERROR` | 취약한 PyYAML load() 가동이 식별되었습니다. RCE 예방을 위해 safe_load()로 대두 전개 처리 하십시오. | `security/deserialization/avoid-pyyaml-load.yaml` |
| `avoid-unsafe-ruamel` | `ERROR` | 동격의 Yaml 파서 인 안전하지 않은 로드 형태 포착. safe 로드 구성을 승인하세요. | `security/deserialization/avoid-unsafe-ruamel.yaml` |
| `baseclass-attribute-override` | `WARNING` | baseclass-attribute-override 잠재적 결함 및 보안 이격율 정비 요망. | `correctness/baseclass-attribute-override.yaml` |
| `cannot-cache-generators` | `WARNING` | cannot-cache-generators 잠재적 결함 및 보안 이격율 정비 요망. | `correctness/cannot-cache-generators.yaml` |
| `code-after-unconditional-return` | `WARNING` | code after return statement will not be executed | `maintainability/return.yaml` |
| `dangerous-annotations-usage` | `INFO` | 위험한 메서드 호출 피로도 점검. | `security/audit/dangerous-annotations-usage.yaml` |
| `dangerous-globals-use` | `WARNING` | 위험한 메서드 호출 피로도 점검. | `security/dangerous-globals-use.yaml` |
| `dangerous-interactive-code-run` | `WARNING` | 위험한 메서드 호출 피로도 점검. | `security/dangerous-code-run.yaml` |
| `dangerous-interactive-code-run-audit` | `WARNING` | 위험한 메서드 호출 피로도 점검. | `security/audit/dangerous-code-run-audit.yaml` |
| `dangerous-interactive-code-run-tainted-env-args` | `WARNING` | 위험한 메서드 호출 피로도 점검. | `security/audit/dangerous-code-run-tainted-env-args.yaml` |
| `dangerous-subinterpreters-run-string` | `WARNING` | 위험한 메서드 호출 피로도 점검. | `security/dangerous-subinterpreters-run-string.yaml` |
| `dangerous-subinterpreters-run-string-audit` | `WARNING` | 위험한 메서드 호출 피로도 점검. | `security/audit/dangerous-subinterpreters-run-string-audit.yaml` |
| `dangerous-subinterpreters-run-string-tainted-env-args` | `WARNING` | 위험한 메서드 호출 피로도 점검. | `security/audit/dangerous-subinterpreters-run-string-tainted-env-args.yaml` |
| `dangerous-testcapi-run-in-subinterp` | `WARNING` | 위험한 메서드 호출 피로도 점검. | `security/dangerous-testcapi-run-in-subinterp.yaml` |
| `dangerous-testcapi-run-in-subinterp-audit` | `WARNING` | 위험한 메서드 호출 피로도 점검. | `security/audit/dangerous-testcapi-run-in-subinterp-audit.yaml` |
| `dangerous-testcapi-run-in-subinterp-tainted-env-args` | `WARNING` | 위험한 메서드 호출 피로도 점검. | `security/audit/dangerous-testcapi-run-in-subinterp-tainted-env-args.yaml` |
| `default-mutable-dict` | `ERROR` | 가변 Dict를 함수 기본 인자로 탑재하여 전역 버퍼 오염을 유도하는 Pitfall을 경보합니다. None 분기가 요망됩니다. | `correctness/common-mistakes/default-mutable-dict.yaml` |
| `default-mutable-list` | `ERROR` | 가변 List 기본 인자 탑재로 인한 버퍼 공유 격량. None 매핑으로 필터 하세요. | `correctness/common-mistakes/default-mutable-list.yaml` |
| `dict-del-while-iterate` | `WARNING` | dict-del-while-iterate 잠재적 결함 및 보안 이격율 정비 요망. | `correctness/dict-modify-iterating.yaml` |
| `disabled-cert-validation` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 disabled-cert-validation 전사 단속이 요구됩니다. | `security/audit/network/disabled-cert-validation.yaml` |
| `file-object-redefined-before-close` | `WARNING` | file-object-redefined-before-close 잠재적 결함 및 보안 이격율 정비 요망. | `correctness/file-object-redefined-before-close.yaml` |
| `formatted-sql-query` | `WARNING` | formatted-sql-query 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/formatted-sql-query.yaml` |
| `hardcoded-password-default-argument` | `WARNING` | hardcoded-password-default-argument 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/hardcoded-password-default-argument.yaml` |
| `hardcoded-tmp-path` | `WARNING` | hardcoded-tmp-path 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/hardcoded-tmp-path.yaml` |
| `http-not-https-connection` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 http-not-https-connection 전사 단속이 요구됩니다. | `security/audit/network/http-not-https-connection.yaml` |
| `httpsconnection-detected` | `WARNING` | httpsconnection-detected 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/httpsconnection-detected.yaml` |
| `identical-is-comparison` | `ERROR` | 참조 검증에 있어 식별율을 수비 타개 하세요. | `correctness/common-mistakes/is-comparison-string.yaml` |
| `improper-list-concat` | `INFO` | improper-list-concat 잠재적 결함 및 보안 이격율 정비 요망. | `maintainability/improper-list-concat.yaml` |
| `insecure-file-permissions` | `WARNING` | 보안 옵션 누사 및 예방 단속 필요. | `security/audit/insecure-file-permissions.yaml` |
| `insecure-hash-algorithm-md5` | `WARNING` | 보안 옵션 누사 및 예방 단속 필요. | `security/insecure-hash-algorithms-md5.yaml` |
| `insecure-hash-algorithm-sha1` | `WARNING` | 보안 옵션 누사 및 예방 단속 필요. | `security/insecure-hash-algorithms.yaml` |
| `insecure-openerdirector-open` | `WARNING` | 보안 옵션 누사 및 예방 단속 필요. | `security/audit/insecure-transport/urllib/insecure-openerdirector-open.yaml` |
| `insecure-openerdirector-open-ftp` | `WARNING` | 보안 옵션 누사 및 예방 단속 필요. | `security/audit/insecure-transport/urllib/insecure-openerdirector-open-ftp.yaml` |
| `insecure-request-object` | `WARNING` | 보안 옵션 누사 및 예방 단속 필요. | `security/audit/insecure-transport/urllib/insecure-request-object.yaml` |
| `insecure-request-object-ftp` | `WARNING` | 보안 옵션 누사 및 예방 단속 필요. | `security/audit/insecure-transport/urllib/insecure-request-object-ftp.yaml` |
| `insecure-urlopen` | `WARNING` | 보안 옵션 누사 및 예방 단속 필요. | `security/audit/insecure-transport/urllib/insecure-urlopen.yaml` |
| `insecure-urlopen-ftp` | `WARNING` | 보안 옵션 누사 및 예방 단속 필요. | `security/audit/insecure-transport/urllib/insecure-urlopen-ftp.yaml` |
| `insecure-urlopener-open` | `WARNING` | 보안 옵션 누사 및 예방 단속 필요. | `security/audit/insecure-transport/urllib/insecure-urlopener-open.yaml` |
| `insecure-urlopener-open-ftp` | `WARNING` | 보안 옵션 누사 및 예방 단속 필요. | `security/audit/insecure-transport/urllib/insecure-urlopener-open-ftp.yaml` |
| `insecure-urlopener-retrieve` | `WARNING` | 보안 옵션 누사 및 예방 단속 필요. | `security/audit/insecure-transport/urllib/insecure-urlopener-retrieve.yaml` |
| `insecure-urlopener-retrieve-ftp` | `WARNING` | 보안 옵션 누사 및 예방 단속 필요. | `security/audit/insecure-transport/urllib/insecure-urlopener-retrieve-ftp.yaml` |
| `insecure-urlretrieve` | `WARNING` | 보안 옵션 누사 및 예방 단속 필요. | `security/audit/insecure-transport/urllib/insecure-urlretrieve.yaml` |
| `insecure-urlretrieve-ftp` | `WARNING` | 보안 옵션 누사 및 예방 단속 필요. | `security/audit/insecure-transport/urllib/insecure-urlretrieve-ftp.yaml` |
| `is-function-without-parentheses` | `WARNING` | is-function-without-parentheses 잠재적 결함 및 보안 이격율 정비 요망. | `maintainability/is-function-without-parentheses.yaml` |
| `is-not-is-not` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 is-not-is-not 전사 단속이 요구됩니다. | `correctness/common-mistakes/is-not-is-not.yaml` |
| `list-modify-while-iterate` | `ERROR` | for 루프 순회 중 원본 리스트를 가변 삭제/수정하여 오동작을 격발시키는 리스크 누출입니다. | `correctness/list-modify-iterating.yaml` |
| `listen-eval` | `WARNING` | listen-eval 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/logging/listeneval.yaml` |
| `logging-error-without-handling` | `WARNING` | logging-error-without-handling 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/logging-error-without-handling.yaml` |
| `mako-templates-detected` | `INFO` | mako-templates-detected 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/mako-templates-detected.yaml` |
| `manual-defaultdict-dict-create` | `WARNING` | manually creating a defaultdict - use collections.defaultdict(dict) | `best-practice/manual-collections-create.yaml` |
| `marshal-usage` | `WARNING` | marshal-usage 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/marshal.yaml` |
| `md5-used-as-password` | `WARNING` | md5-used-as-password 잠재적 결함 분기 정비 요망. | `security/audit/md5-used-as-password.yaml` |
| `missing-hash-with-eq` | `WARNING` | missing-hash-with-eq 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/missing-hash-with-eq.yaml` |
| `multiprocessing-recv` | `WARNING` | multiprocessing-recv 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/conn_recv.yaml` |
| `no-strings-as-booleans` | `ERROR` | 문자열 결합 시 연산 논리 혼선 국면을 저지합니다. | `correctness/useless-comparison.yaml` |
| `non-literal-import` | `WARNING` | non-literal-import 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/non-literal-import.yaml` |
| `open-never-closed` | `ERROR` | 디스크 서술자 닫기 연쇄가 빠졌습니다. | `best-practice/open-never-closed.yaml` |
| `paramiko-exec-command` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 paramiko-exec-command 전사 단속이 요구됩니다. | `security/audit/paramiko/paramiko-exec-command.yaml` |
| `paramiko-implicit-trust-host-key` | `WARNING` | paramiko-implicit-trust-host-key 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/paramiko-implicit-trust-host-key.yaml` |
| `pass-body-fn` | `WARNING` | `pass` is the body of function $X. Consider removing this or raise NotImplemente... | `best-practice/pass-body.yaml` |
| `pdb-remove` | `WARNING` | pdb-remove 잠재적 결함 및 보안 이격율 정비 요망. | `correctness/pdb.yaml` |
| `pg8000-sqli` | `WARNING` | 잠재적 SQL 인젝션 경로에 대한 검토가 필요합니다. | `security/audit/sqli/pg8000-sqli.yaml` |
| `psycopg-sqli` | `WARNING` | 잠재적 SQL 인젝션 경로에 대한 검토가 필요합니다. | `security/audit/sqli/psycopg-sqli.yaml` |
| `pytest-assert_match-after-path-patch` | `WARNING` | pytest-assert_match-after-path-patch 잠재적 결함 및 보안 이격율 정비 요망. | `correctness/pytest-assert_match-after-path-patch.yaml` |
| `python-debugger-found` | `WARNING` | python-debugger-found 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/pdb.yaml` |
| `python-logger-credential-disclosure` | `WARNING` | python-logger-credential-disclosure 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/logging/logger-credential-leak.yaml` |
| `python-reverse-shell` | `WARNING` | python-reverse-shell 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/python-reverse-shell.yaml` |
| `python36-compatibility-ssl` | `ERROR` | 해당 함수 및 문법은 해당 파이썬 버전 연산 지원 사양입니다. | `compatibility/python36.yaml` |
| `python37-compatibility-importlib` | `ERROR` | python37-compatibility-pdb 잠재적 결함 및 보안 이격율 정비 요망. | `compatibility/python37.yaml` |
| `raise-not-base-exception` | `ERROR` | raise-not-base-exception 보안 인젝션 및 런타임 버그 전사 예방 점검. | `correctness/exceptions/exceptions.yaml` |
| `regex_dos` | `WARNING` | regex_dos 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/regex-dos.yaml` |
| `sha224-hash` | `WARNING` | sha224-hash 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/sha224-hash.yaml` |
| `ssl-wrap-socket-is-deprecated` | `WARNING` | ssl-wrap-socket-is-deprecated 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/ssl-wrap-socket-is-deprecated.yaml` |
| `string-concat-in-list` | `WARNING` | string-concat-in-list 잠재적 결함 및 보안 이격율 정비 요망. | `correctness/common-mistakes/string-concat-in-list.yaml` |
| `subprocess-list-passed-as-string` | `WARNING` | 하위 프로세스 생성 드라이버 인젝션 피로도 점검. | `security/audit/subprocess-list-passed-as-string.yaml` |
| `subprocess-shell-true` | `ERROR` | shell=True 위험 옵션을 우회 처리하십시오. | `security/audit/subprocess-shell-true.yaml` |
| `sync-sleep-in-async-code` | `WARNING` | sync-sleep-in-async-code 잠재적 결함 및 보안 이격율 정비 요망. | `correctness/sync-sleep-in-async-code.yaml` |
| `system-wildcard-detected` | `WARNING` | system-wildcard-detected 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/system-wildcard-detected.yaml` |
| `telnetlib` | `WARNING` | telnetlib 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/telnetlib.yaml` |
| `tempfile-insecure` | `ERROR` | tempfile-insecure 보안 인젝션 및 런타임 버그 전사 예방 점검. | `correctness/tempfile/mktemp.yaml` |
| `tempfile-without-flush` | `ERROR` | tempfile-without-flush 보안 인젝션 및 런타임 버그 전사 예방 점검. | `correctness/tempfile/flush.yaml` |
| `test-is-missing-assert` | `WARNING` | test-is-missing-assert 잠재적 결함 및 보안 이격율 정비 요망. | `correctness/test-is-missing-assert.yaml` |
| `uncaught-executor-exceptions` | `WARNING` | uncaught-executor-exceptions 잠재적 결함 및 보안 이격율 정비 요망. | `correctness/concurrent.yaml` |
| `unchecked-subprocess-call` | `WARNING` | unchecked-subprocess-call 잠재적 결함 및 보안 이격율 정비 요망. | `correctness/unchecked-returns.yaml` |
| `unspecified-open-encoding` | `WARNING` | unspecified-open-encoding 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/unspecified-open-encoding.yaml` |
| `unverified-ssl-context` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 unverified-ssl-context 전사 단속이 요구됩니다. | `security/unverified-ssl-context.yaml` |
| `use-defused-xml` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 use-defused-xml 전사 단속이 요구됩니다. | `security/use-defused-xml.yaml` |
| `use-defused-xml-parse` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 use-defused-xml-parse 전사 단속이 요구됩니다. | `security/use-defused-xml-parse.yaml` |
| `use-defused-xmlrpc` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 use-defused-xmlrpc 전사 단속이 요구됩니다. | `security/use-defused-xmlrpc.yaml` |
| `use-defusedcsv` | `INFO` | use-defusedcsv 잠재적 결함 및 보안 이격율 정비 요망. | `security/use-defusedcsv.yaml` |
| `use-ftp-tls` | `INFO` | use-ftp-tls 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/insecure-transport/ftplib/use-ftp-tls.yaml` |
| `use-sys-exit` | `WARNING` | use-sys-exit 잠재적 결함 및 보안 이격율 정비 요망. | `correctness/exit.yaml` |
| `useless-assignment-keyed` | `INFO` | useless-assignment-keyed 잠재적 결함 및 보안 이격율 정비 요망. | `maintainability/useless-assign-keyed.yaml` |
| `useless-eqeq` | `INFO` | useless-eqeq 잠재적 결함 및 보안 이격율 정비 요망. | `correctness/useless-eqeq.yaml` |
| `useless-if-conditional` | `WARNING` | if block checks for the same condition on both branches (`$X`) | `maintainability/useless-ifelse.yaml` |
| `useless-inner-function` | `ERROR` | 내부 함수가 정의되었으나 사용 연동이 누락되었습니다. 코드 가독성을 위해 말소 대상 점검 하십시오. | `maintainability/useless-innerfunction.yaml` |
| `useless-literal` | `WARNING` | useless-literal 잠재적 결함 및 보안 이격율 정비 요망. | `maintainability/useless-literal.yaml` |
| `useless-literal-set` | `ERROR` | set 조립 단에 중복 할당 조각이 보입니다. | `maintainability/useless-literal-set.yaml` |
| `writing-to-file-in-read-mode` | `ERROR` | 읽기 전용으로 가동 중인 서술자에 쓰기(.write)를 가압하는 런타임 에러를 경보합니다. | `correctness/writing-to-file-in-read-mode.yaml` |
| `yield-in-init` | `ERROR` | __init__ 내부에 return문을 구동하여 버그를 조율시키는 극간 스탠스입니다. | `correctness/return-in-init.yaml` |

## PYCRYPTODOME

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `crypto-mode-without-authentication` | `ERROR` | 무결성 검증 없는 암호화 운영 모드가 사용되었습니다. GCM 등 AEAD 모드 사용을 권장합니다. | `security/mode-without-authentication.yaml` |
| `insecure-cipher-algorithm-blowfish` | `WARNING` | 보안 옵션 누사 및 예방 단속 필요. | `security/insecure-cipher-algorithm-blowfish.yaml` |
| `insecure-cipher-algorithm-des` | `WARNING` | 보안 옵션 누사 및 예방 단속 필요. | `security/insecure-cipher-algorithm-des.yaml` |
| `insecure-cipher-algorithm-rc2` | `WARNING` | 보안 옵션 누사 및 예방 단속 필요. | `security/insecure-cipher-algorithm-rc2.yaml` |
| `insecure-cipher-algorithm-rc4` | `WARNING` | 보안 옵션 누사 및 예방 단속 필요. | `security/insecure-cipher-algorithm-rc4.yaml` |
| `insecure-cipher-algorithm-xor` | `WARNING` | 보안 옵션 누사 및 예방 단속 필요. | `security/insecure-cipher-algorithm.yaml` |
| `insecure-hash-algorithm-md2` | `WARNING` | 보안 옵션 누사 및 예방 단속 필요. | `security/insecure-hash-algorithm-md2.yaml` |
| `insecure-hash-algorithm-md4` | `WARNING` | 보안 옵션 누사 및 예방 단속 필요. | `security/insecure-hash-algorithm-md4.yaml` |
| `insecure-hash-algorithm-md5` | `WARNING` | 보안 옵션 누사 및 예방 단속 필요. | `security/insecure-hash-algorithm-md5.yaml` |
| `insecure-hash-algorithm-sha1` | `WARNING` | 보안 옵션 누사 및 예방 단속 필요. | `security/insecure-hash-algorithm.yaml` |
| `insufficient-dsa-key-size` | `WARNING` | insufficient-dsa-key-size 잠재적 결함 및 보안 이격율 정비 요망. | `security/insufficient-dsa-key-size.yaml` |
| `insufficient-rsa-key-size` | `WARNING` | insufficient-rsa-key-size 잠재적 결함 및 보안 이격율 정비 요망. | `security/insufficient-rsa-key-size.yaml` |

## PYMONGO

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `mongo-client-bad-auth` | `WARNING` | mongo-client-bad-auth 잠재적 결함 및 보안 이격율 정비 요망. | `security/mongodb.yaml` |

## PYRAMID

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `pyramid-authtkt-cookie-httponly-unsafe-default` | `WARNING` | 쿠키 보안 속성(Secure/HttpOnly) 누출 우려 점검. | `audit/authtkt-cookie-httponly-unsafe-default.yaml` |
| `pyramid-authtkt-cookie-httponly-unsafe-value` | `WARNING` | 쿠키 보안 속성(Secure/HttpOnly) 누출 우려 점검. | `audit/authtkt-cookie-httponly-unsafe-value.yaml` |
| `pyramid-authtkt-cookie-samesite` | `WARNING` | 쿠키 보안 속성(Secure/HttpOnly) 누출 우려 점검. | `audit/authtkt-cookie-samesite.yaml` |
| `pyramid-authtkt-cookie-secure-unsafe-default` | `WARNING` | 쿠키 보안 속성(Secure/HttpOnly) 누출 우려 점검. | `audit/authtkt-cookie-secure-unsafe-default.yaml` |
| `pyramid-authtkt-cookie-secure-unsafe-value` | `WARNING` | 쿠키 보안 속성(Secure/HttpOnly) 누출 우려 점검. | `audit/authtkt-cookie-secure-unsafe-value.yaml` |
| `pyramid-csrf-check-disabled` | `WARNING` | pyramid-csrf-check-disabled 잠재적 결함 및 보안 이격율 정비 요망. | `audit/csrf-check-disabled.yaml` |
| `pyramid-csrf-check-disabled-globally` | `ERROR` | Pyramid 전역 CSRF 방어가 비활성화되었습니다. 뷰 보호를 위해 토크나이저를 구동하십시오. | `security/csrf-check-disabled-globally.yaml` |
| `pyramid-csrf-origin-check-disabled` | `WARNING` | pyramid-csrf-origin-check-disabled 잠재적 결함 및 보안 이격율 정비 요망. | `audit/csrf-origin-check-disabled.yaml` |
| `pyramid-csrf-origin-check-disabled-globally` | `ERROR` | Pyramid Referrer CSRF 검증 전역 누락 감지. Origin 체크 옵션을 활성화하십시오. | `audit/csrf-origin-check-disabled-globally.yaml` |
| `pyramid-direct-use-of-response` | `ERROR` | Response 객체를 렌더링 없이 날것으로 출력합니다. XSS 방어 레이어 우회 우려가 있습니다. | `security/direct-use-of-response.yaml` |
| `pyramid-set-cookie-httponly-unsafe-default` | `WARNING` | 쿠키 보안 속성(Secure/HttpOnly) 누출 우려 점검. | `audit/set-cookie-httponly-unsafe-default.yaml` |
| `pyramid-set-cookie-httponly-unsafe-value` | `WARNING` | 쿠키 보안 속성(Secure/HttpOnly) 누출 우려 점검. | `audit/set-cookie-httponly-unsafe-value.yaml` |
| `pyramid-set-cookie-samesite-unsafe-default` | `WARNING` | 쿠키 보안 속성(Secure/HttpOnly) 누출 우려 점검. | `audit/set-cookie-samesite-unsafe-default.yaml` |
| `pyramid-set-cookie-samesite-unsafe-value` | `WARNING` | 쿠키 보안 속성(Secure/HttpOnly) 누출 우려 점검. | `audit/set-cookie-samesite-unsafe-value.yaml` |
| `pyramid-set-cookie-secure-unsafe-default` | `WARNING` | 쿠키 보안 속성(Secure/HttpOnly) 누출 우려 점검. | `audit/set-cookie-secure-unsafe-default.yaml` |
| `pyramid-set-cookie-secure-unsafe-value` | `WARNING` | 쿠키 보안 속성(Secure/HttpOnly) 누출 우려 점검. | `audit/set-cookie-secure-unsafe-value.yaml` |
| `pyramid-sqlalchemy-sql-injection` | `ERROR` | distinct/having절 내 원시 SQL 인젝션 가동 현상 감지. bindparams 규격을 준행하세요. | `security/sqlalchemy-sql-injection.yaml` |

## REQUESTS

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `disabled-cert-validation` | `ERROR` | requests 가동 시 인증서 검증(verify=False) 탑재는 중간자 노출을 가동합니다. 재활성화 하세요. | `security/disabled-cert-validation.yaml` |
| `no-auth-over-http` | `ERROR` | HTTP 평문 채널을 통한 인증 전송이 포착되었습니다. 스니핑 격퇴를 위해 https:// 도약을 강제 하십시오. | `security/no-auth-over-http.yaml` |
| `python.requests.best-practice.use-request-json-shortcut` | `WARNING` | python.requests.best-practice.use-request-json-shortcut 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/use-request-json-shortcut.yaml` |
| `python.requests.best-practice.use-response-json-shortcut` | `WARNING` | python.requests.best-practice.use-response-json-shortcut 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/use-response-json-shortcut.yaml` |
| `use-raise-for-status` | `WARNING` | use-raise-for-status 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/use-raise-for-status.yaml` |
| `use-timeout` | `WARNING` | use-timeout 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/use-timeout.yaml` |

## SH

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `string-concat` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 string-concat 전사 단속이 요구됩니다. | `security/string-concat.yaml` |

## SQLALCHEMY

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `avoid-sqlalchemy-text` | `ERROR` | sqlalchemy.text() 구동 시 동적 스트링 합사 버그가 우려됩니다. ORM 규격 모델을 준행 하세요. | `security/audit/avoid-sqlalchemy-text.yaml` |
| `bad-operator-in-filter` | `WARNING` | bad-operator-in-filter 잠재적 결함 및 보안 이격율 정비 요망. | `correctness/bad-operator-in-filter.yaml` |
| `delete-where-no-execute` | `ERROR` | SQLAlchemy .delete() 연산 시 .where() 스킵 국면이 감지되었습니다. 전사 데이터 유실에 대비하십시오. | `correctness/delete-where.yaml` |
| `len-all-count` | `WARNING` | batch-import 잠재적 결함 분기 정비 요망. | `performance/performance-improvements.yaml` |
| `sqlalchemy-execute-raw-query` | `ERROR` | SQLAlchemy 원시 쿼리 동적 결합 감지. 인젝션 투하를 막으려면 Parameterized 선언을 장착 하십시오. | `security/sqlalchemy-execute-raw-query.yaml` |
| `sqlalchemy-sql-injection` | `WARNING` | sqlalchemy-sql-injection 잠재적 결함 및 보안 이격율 정비 요망. | `security/sqlalchemy-sql-injection.yaml` |

## TWILIO

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `twiml-injection` | `WARNING` | twiml-injection 잠재적 결함 분기 정비 요망. | `security/twiml-injection.yaml` |
