# Global Semgrep ERROR Rules Summary

# Language: DOCKERFILE

## CORRECTNESS

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `invalid-port` | `ERROR` | Dockerfile 연쇄 점검: invalid-port 준행 오류 국면 감지. | `dockerfile/invalid-port.yaml` |
| `multiple-entrypoint-instructions` | `ERROR` | ENTRYPOINT 명령어 다수 사용 시 충돌 국면 점검. | `dockerfile/multiple-entrypoint-instructions.yaml` |

## SECURITY

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `dockerfile-dockerd-socket-mount` | `ERROR` | Dockerfile 연쇄 점검: dockerfile-dockerd-socket-mount 준행 오류 국면 감지. | `dockerfile/dockerd-socket-mount.yaml` |
| `last-user-is-root` | `ERROR` | 마지막 실행 컨텍스트가 root로 전사 탑재 되었습니다. | `dockerfile/last-user-is-root.yaml` |
| `missing-user` | `ERROR` | Dockerfile에 USER 명령어가 부재하여 root 권한 폭주 우려가 있습니다. | `dockerfile/missing-user.yaml` |
| `missing-user-entrypoint` | `ERROR` | USER 명령어 누사로 인한 컨테이너 root 실행 위험 지점입니다. | `dockerfile/missing-user-entrypoint.yaml` |

# Language: GENERIC

## CI

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `bash_reverse_shell` | `ERROR` | bash_reverse_shell 보안 인젝션 및 런타임 버그 전사 예방 점검. | `generic/security/bash-reverse-shell.yaml` |

## DOCKERFILE

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `alias-must-be-unique` | `ERROR` | Alias 식별자 고유율을 수하 하세요. | `generic/correctness/alias-must-be-unique.yaml` |
| `copy-from-own-alias` | `ERROR` | 자기 자신의 스테이지 레이어를 출처(from)로 명명하는 순환 구성을 경보합니다. | `generic/correctness/copy-from-own-alias.yaml` |
| `multiple-cmd-instructions` | `ERROR` | Dockerfile 내 `CMD` 절 중복 가압 금지. 마지막 절만 효력을 발휘합니다. | `generic/correctness/multiple-cmd-instructions.yaml` |

## NGINX

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `header-injection` | `ERROR` | Nginx 헤더 가압 버퍼 오염 위험 경고. | `generic/security/header-injection.yaml` |

## SECRETS

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `detected-amazon-mws-auth-token` | `ERROR` | 보안 기밀/인증 문자열(Secret) 노출이 감지되었습니다. 보안 저장소로 대두 전담 하세요. | `generic/security/detected-amazon-mws-auth-token.yaml` |
| `detected-artifactory-password` | `ERROR` | 보안 기밀/인증 문자열(Secret) 노출이 감지되었습니다. 보안 저장소로 대두 전담 하세요. | `generic/security/detected-artifactory-password.yaml` |
| `detected-artifactory-token` | `ERROR` | 보안 기밀/인증 문자열(Secret) 노출이 감지되었습니다. 보안 저장소로 대두 전담 하세요. | `generic/security/detected-artifactory-token.yaml` |
| `detected-aws-access-key-id-value` | `ERROR` | AWS Access/Secret 자격증명이 노출되었습니다. | `generic/security/detected-aws-access-key-id-value.yaml` |
| `detected-aws-appsync-graphql-key` | `ERROR` | AWS Access/Secret 자격증명이 노출되었습니다. | `generic/security/detected-aws-appsync-graphql-key.yaml` |
| `detected-aws-secret-access-key` | `ERROR` | AWS Access/Secret 자격증명이 노출되었습니다. | `generic/security/detected-aws-secret-access-key.yaml` |
| `detected-aws-session-token` | `ERROR` | AWS Access/Secret 자격증명이 노출되었습니다. | `generic/security/detected-aws-session-token.yaml` |
| `detected-bcrypt-hash` | `ERROR` | 보안 기밀/인증 문자열(Secret) 노출이 감지되었습니다. 보안 저장소로 대두 전담 하세요. | `generic/security/detected-bcrypt-hash.yaml` |
| `detected-codeclimate` | `ERROR` | 보안 기밀/인증 문자열(Secret) 노출이 감지되었습니다. 보안 저장소로 대두 전담 하세요. | `generic/security/detected-codeclimate.yaml` |
| `detected-etc-shadow` | `ERROR` | 보안 기밀/인증 문자열(Secret) 노출이 감지되었습니다. 보안 저장소로 대두 전담 하세요. | `generic/security/detected-etc-shadow.yaml` |
| `detected-facebook-access-token` | `ERROR` | Facebook 인증 토큰이 노출되었습니다. | `generic/security/detected-facebook-access-token.yaml` |
| `detected-facebook-oauth` | `ERROR` | Facebook 인증 토큰이 노출되었습니다. | `generic/security/detected-facebook-oauth.yaml` |
| `detected-generic-api-key` | `ERROR` | 보안 기밀/인증 문자열(Secret) 노출이 감지되었습니다. 보안 저장소로 대두 전담 하세요. | `generic/security/detected-generic-api-key.yaml` |
| `detected-generic-secret` | `ERROR` | 보안 기밀/인증 문자열(Secret) 노출이 감지되었습니다. 보안 저장소로 대두 전담 하세요. | `generic/security/detected-generic-secret.yaml` |
| `detected-github-token` | `ERROR` | GitHub 토큰 자격증명이 노출되었습니다. | `generic/security/detected-github-token.yaml` |
| `detected-google-api-key` | `ERROR` | Google API/OAuth 자격증명이 노출되었습니다. | `generic/security/detected-google-api-key.yaml` |
| `detected-google-cloud-api-key` | `ERROR` | Google API/OAuth 자격증명이 노출되었습니다. | `generic/security/detected-google-cloud-api-key.yaml` |
| `detected-google-gcm-service-account` | `ERROR` | Google API/OAuth 자격증명이 노출되었습니다. | `generic/security/detected-google-gcm-service-account.yaml` |
| `detected-google-oauth-access-token` | `ERROR` | Google API/OAuth 자격증명이 노출되었습니다. | `generic/security/detected-google-oauth-access-token.yaml` |
| `detected-google-oauth-url` | `ERROR` | Google API/OAuth 자격증명이 노출되었습니다. | `generic/security/detected-google-oauth.yaml` |
| `detected-heroku-api-key` | `ERROR` | 보안 기밀/인증 문자열(Secret) 노출이 감지되었습니다. 보안 저장소로 대두 전담 하세요. | `generic/security/detected-heroku-api-key.yaml` |
| `detected-hockeyapp` | `ERROR` | 보안 기밀/인증 문자열(Secret) 노출이 감지되었습니다. 보안 저장소로 대두 전담 하세요. | `generic/security/detected-hockeyapp.yaml` |
| `detected-jwt-token` | `ERROR` | 보안 기밀/인증 문자열(Secret) 노출이 감지되었습니다. 보안 저장소로 대두 전담 하세요. | `generic/security/detected-jwt-token.yaml` |
| `detected-kolide-api-key` | `ERROR` | 보안 기밀/인증 문자열(Secret) 노출이 감지되었습니다. 보안 저장소로 대두 전담 하세요. | `generic/security/detected-kolide-api-key.yaml` |
| `detected-mailchimp-api-key` | `ERROR` | 보안 기밀/인증 문자열(Secret) 노출이 감지되었습니다. 보안 저장소로 대두 전담 하세요. | `generic/security/detected-mailchimp-api-key.yaml` |
| `detected-mailgun-api-key` | `ERROR` | 보안 기밀/인증 문자열(Secret) 노출이 감지되었습니다. 보안 저장소로 대두 전담 하세요. | `generic/security/detected-mailgun-api-key.yaml` |
| `detected-npm-registry-auth-token` | `ERROR` | 보안 기밀/인증 문자열(Secret) 노출이 감지되었습니다. 보안 저장소로 대두 전담 하세요. | `generic/security/detected-npm-registry-auth-token.yaml` |
| `detected-onfido-live-api-token` | `ERROR` | 보안 기밀/인증 문자열(Secret) 노출이 감지되었습니다. 보안 저장소로 대두 전담 하세요. | `generic/security/detected-onfido-live-api-token.yaml` |
| `detected-outlook-team` | `ERROR` | 보안 기밀/인증 문자열(Secret) 노출이 감지되었습니다. 보안 저장소로 대두 전담 하세요. | `generic/security/detected-outlook-team.yaml` |
| `detected-paypal-braintree-access-token` | `ERROR` | 보안 기밀/인증 문자열(Secret) 노출이 감지되었습니다. 보안 저장소로 대두 전담 하세요. | `generic/security/detected-paypal-braintree-access-token.yaml` |
| `detected-pgp-private-key-block` | `ERROR` | 보안 기밀/인증 문자열(Secret) 노출이 감지되었습니다. 보안 저장소로 대두 전담 하세요. | `generic/security/detected-pgp-private-key-block.yaml` |
| `detected-picatic-api-key` | `ERROR` | 보안 기밀/인증 문자열(Secret) 노출이 감지되었습니다. 보안 저장소로 대두 전담 하세요. | `generic/security/detected-picatic-api-key.yaml` |
| `detected-private-key` | `ERROR` | 보안 기밀/인증 문자열(Secret) 노출이 감지되었습니다. 보안 저장소로 대두 전담 하세요. | `generic/security/detected-private-key.yaml` |
| `detected-sauce-token` | `ERROR` | 보안 기밀/인증 문자열(Secret) 노출이 감지되었습니다. 보안 저장소로 대두 전담 하세요. | `generic/security/detected-sauce-token.yaml` |
| `detected-sendgrid-api-key` | `ERROR` | 보안 기밀/인증 문자열(Secret) 노출이 감지되었습니다. 보안 저장소로 대두 전담 하세요. | `generic/security/detected-sendgrid-api-key.yaml` |
| `detected-slack-token` | `ERROR` | Slack 토큰 자격증명이 노출되었습니다. | `generic/security/detected-slack-token.yaml` |
| `detected-slack-webhook` | `ERROR` | Slack 토큰 자격증명이 노출되었습니다. | `generic/security/detected-slack-webhook.yaml` |
| `detected-snyk-api-key` | `ERROR` | 보안 기밀/인증 문자열(Secret) 노출이 감지되었습니다. 보안 저장소로 대두 전담 하세요. | `generic/security/detected-snyk-api-key.yaml` |
| `detected-softlayer-api-key` | `ERROR` | 보안 기밀/인증 문자열(Secret) 노출이 감지되었습니다. 보안 저장소로 대두 전담 하세요. | `generic/security/detected-softlayer-api-key.yaml` |
| `detected-sonarqube-docs-api-key` | `ERROR` | 보안 기밀/인증 문자열(Secret) 노출이 감지되었습니다. 보안 저장소로 대두 전담 하세요. | `generic/security/detected-sonarqube-docs-api-key.yaml` |
| `detected-square-access-token` | `ERROR` | 보안 기밀/인증 문자열(Secret) 노출이 감지되었습니다. 보안 저장소로 대두 전담 하세요. | `generic/security/detected-square-access-token.yaml` |
| `detected-square-oauth-secret` | `ERROR` | 보안 기밀/인증 문자열(Secret) 노출이 감지되었습니다. 보안 저장소로 대두 전담 하세요. | `generic/security/detected-square-oauth-secret.yaml` |
| `detected-ssh-password` | `ERROR` | 보안 기밀/인증 문자열(Secret) 노출이 감지되었습니다. 보안 저장소로 대두 전담 하세요. | `generic/security/detected-ssh-password.yaml` |
| `detected-stripe-api-key` | `ERROR` | 보안 기밀/인증 문자열(Secret) 노출이 감지되었습니다. 보안 저장소로 대두 전담 하세요. | `generic/security/detected-stripe-api-key.yaml` |
| `detected-stripe-restricted-api-key` | `ERROR` | 보안 기밀/인증 문자열(Secret) 노출이 감지되었습니다. 보안 저장소로 대두 전담 하세요. | `generic/security/detected-stripe-restricted-api-key.yaml` |
| `detected-telegram-bot-api-key` | `ERROR` | 보안 기밀/인증 문자열(Secret) 노출이 감지되었습니다. 보안 저장소로 대두 전담 하세요. | `generic/security/detected-telegram-bot-api-key.yaml` |
| `detected-twilio-api-key` | `ERROR` | 보안 기밀/인증 문자열(Secret) 노출이 감지되었습니다. 보안 저장소로 대두 전담 하세요. | `generic/security/detected-twilio-api-key.yaml` |
| `detected-username-and-password-in-uri` | `ERROR` | 보안 기밀/인증 문자열(Secret) 노출이 감지되었습니다. 보안 저장소로 대두 전담 하세요. | `generic/security/detected-username-and-password-in-uri.yaml` |

## VISUALFORCE

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `xss-from-unescaped-url-param` | `ERROR` | xss-from-unescaped-url-param 보안 인젝션 및 런타임 버그 전사 예방 점검. | `generic/security/ncino/vf/XSSFromUnescapedURLParam.yaml` |

# Language: GO

## AWS-LAMBDA

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `tainted-sql-string` | `ERROR` | Go 보안 및 무결성 관리: tainted-sql-string 점검 처리 하세요. | `go/security/tainted-sql-string.yaml` |

## GRPC

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `grpc-client-insecure-connection` | `ERROR` | Go 보안 및 무결성 관리: grpc-client-insecure-connection 점검 처리 하세요. | `go/security/grpc-client-insecure-connection.yaml` |
| `grpc-server-insecure-connection` | `ERROR` | Go 보안 및 무결성 관리: grpc-server-insecure-connection 점검 처리 하세요. | `go/security/grpc-server-insecure-connection.yaml` |

## JWT-GO

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `jwt-go-none-algorithm` | `ERROR` | Go 보안 및 무결성 관리: jwt-go-none-algorithm 점검 처리 하세요. | `go/security/jwt-none-alg.yaml` |

## LANG

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `dangerous-command-write` | `ERROR` | Go 보안 및 무결성 관리: dangerous-command-write 점검 처리 하세요. | `go/security/audit/dangerous-command-write.yaml` |
| `dangerous-exec-cmd` | `ERROR` | Go 보안 및 무결성 관리: dangerous-exec-cmd 점검 처리 하세요. | `go/security/audit/dangerous-exec-cmd.yaml` |
| `dangerous-exec-command` | `ERROR` | Go 보안 및 무결성 관리: dangerous-exec-command 점검 처리 하세요. | `go/security/audit/dangerous-exec-command.yaml` |
| `dangerous-syscall-exec` | `ERROR` | Go 보안 및 무결성 관리: dangerous-syscall-exec 점검 처리 하세요. | `go/security/audit/dangerous-syscall-exec.yaml` |
| `filepath-clean-misuse` | `ERROR` | Go 보안 및 무결성 관리: filepath-clean-misuse 점검 처리 하세요. | `go/security/filepath-clean-misuse.yaml` |
| `gosql-sqli` | `ERROR` | Go Lang 다이렉트 SQL 쿼리 가압 단의 인젝션 우려 탑승. | `go/security/audit/sqli/gosql-sqli.yaml` |
| `pg-orm-sqli` | `ERROR` | Go Lang 다이렉트 SQL 쿼리 가압 단의 인젝션 우려 탑승. | `go/security/audit/sqli/pg-orm-sqli.yaml` |
| `pg-sqli` | `ERROR` | Go Lang 다이렉트 SQL 쿼리 가압 단의 인젝션 우려 탑승. | `go/security/audit/sqli/pg-sqli.yaml` |
| `pgx-sqli` | `ERROR` | Go Lang 다이렉트 SQL 쿼리 가압 단의 인젝션 우려 탑승. | `go/security/audit/sqli/pgx-sqli.yaml` |
| `reflect-makefunc` | `ERROR` | Go 보안 및 무결성 관리: reflect-makefunc 점검 처리 하세요. | `go/security/audit/reflect-makefunc.yaml` |
| `tainted-sql-string` | `ERROR` | Go 보안 및 무결성 관리: tainted-sql-string 점검 처리 하세요. | `go/security/injection/tainted-sql-string.yaml` |

## OTTO

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `dangerous-execution` | `ERROR` | Go 보안 및 무결성 관리: dangerous-execution 점검 처리 하세요. | `go/security/audit/dangerous-execution.yaml` |

## TEMPLATE

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `go-ssti` | `ERROR` | Go 보안 및 무결성 관리: go-ssti 점검 처리 하세요. | `go/security/ssti.yaml` |

# Language: HTML

## CORRECTNESS

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `https-equiv` | `ERROR` | HTTPS 꼬리표 결여 및 메타 데이터 누출 경하 점검. | `html/https-equiv.yaml` |

# Language: JAVA

## AWS-LAMBDA

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `tainted-sql-string` | `ERROR` | AWS Lambda 핸들러 등의 외부 사용자 입력이 직접 SQL 문자열 조립에 사용되었습니다. Parameterized Query를 사용하여 SQL 인젝션을 예방하세요. | `java/aws-lambda/security/tainted-sql-string.yaml` |

## JBOSS

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `seam-log-injection` | `ERROR` | Seam Logging API에 외부 데이터가 그대로 주입되었습니다. 표현식 언어(EL)를 통해 로깅 시스템이 공격받을 수 있으므로 주입 전 엄격한 검증을 통과해야 합니다. | `java/jboss/security/seam-log-injection.yaml` |

## LANG

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `assignment-comparison` | `ERROR` | 조건식 내부에서 대입 연산자(=)가 사용되고 있습니다. 의도치 않게 할당이 일어나 비교가 고장날 우려가 있습니다. | `java/lang/correctness/assignment-comparison.yaml` |
| `command-injection-formatted-runtime-call` | `ERROR` | Runtime.exec에 동적 조립 문자열(String.format 등)을 인자로 전달하여 커맨드 인젝션 위험이 있습니다. 안정성을 위해 인자 리스트(String[]) 형식으로 전달하세요. | `java/lang/security/audit/command-injection-formatted-runtime-call.yaml` |
| `command-injection-process-builder` | `ERROR` | ProcessBuilder를 이용한 명령어 가동 시 가변 포매터 및 동적 조립 문자열이 사용되었습니다. 리스트형 인자 전달 스타일로 변경하세요. | `java/lang/security/audit/command-injection-process-builder.yaml` |
| `eqeq` | `ERROR` | $X == $X 또는 $X != $X 와 같이 본인 자신을 직접 비교하고 있습니다. 로직 실수이거나 무의미한 연산일 확률이 높습니다. | `java/lang/correctness/eqeq.yaml` |
| `formatted-sql-string` | `ERROR` | SQL 쿼리 내에서 Formatted String(서식 문자열)이 발견되었습니다. SQL 인젝션 요인을 막기 위해 PreparedStatement 스타일을 적용하세요. | `java/lang/security/audit/formatted-sql-string.yaml` |
| `gcm-nonce-reuse` | `ERROR` | GCM 모드 암호화 시 IV(Nonce) 값이 고정으로 재사용되고 있습니다. 암호화 보완성이 즉시 상실되므로 매번 랜덤하고 중복되지 않는 Nonce를 생성하여 주입하십시오. | `java/lang/security/audit/crypto/gcm-nonce-reuse.yaml` |
| `hardcoded-conditional` | `ERROR` | 조건문(if 등)의 조건식이 항상 true 또는 false로 고정되어 의미 없는 연산을 하거나 로직 버그일 가능성이 높습니다. | `java/lang/correctness/hardcoded-conditional.yaml` |
| `httpservlet-path-traversal` | `ERROR` | 외부 입력값으로 직접 파일 시스템 경로를 구성해 처리. Relative path 제어 유출을 막기 위해 입력값에 대한 검증을 수행하세요. | `java/lang/security/httpservlet-path-traversal.yaml` |
| `tainted-cmd-from-http-request` | `ERROR` | HTTP 요청 데이터가 exec 또는 ProcessBuilder 명령 인자로 직주입되고 있습니다. 커맨드 인젝션을 격퇴하기 위해 외부 데이터 사용 시 사전에 구성된 인자형 맵 구조로 매핑하세요. | `java/lang/security/audit/tainted-cmd-from-http-request.yaml` |
| `tainted-env-from-http-request` | `ERROR` | HTTP 요청이 시스템 커맨드(`exec`)의 환경 변수로 직주입됩니다. 임의 명령 실행 공격을 예방하기 위해 조치하세요. | `java/lang/security/audit/tainted-env-from-http-request.yaml` |
| `xmlinputfactory-external-entities-enabled` | `ERROR` | XMLInputFactory에 외부 엔티티(External Entities)가 허용되어 있습니다. XML External Entity (XXE) 취약점 발생을 예방하기 위해 이를 비활성화하세요. | `java/lang/security/xmlinputfactory-external-entities-enabled.yaml` |

## RMI

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `server-dangerous-object-deserialization` | `ERROR` | RMI 통신 시 임의 객체 수신으로 인한 안전하지 않은 역직렬화 취약점이 가중될 수 있습니다. 허용 클래스 필터링 등을 적용하세요. | `java/rmi/security/server-dangerous-object-deserialization.yaml` |

## SPRING

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `spring-actuator-fully-enabled` | `ERROR` | Spring Boot Actuator의 모든 엔드포인트가 완전 개방되어 민감 정보가 노출될 수 있습니다. 필요한 엔티티만 인가하여 사용하세요. | `java/spring/security/audit/spring-actuator-fully-enabled.yaml` |
| `tainted-file-path` | `ERROR` | 사용자 입력이 직접 파일 제어 경로 상수로 사용됩니다. Path Traversal 등 디렉토리 도약 시도를 검증하고 소거하세요. | `java/spring/security/injection/tainted-file-path.yaml` |
| `tainted-html-string` | `ERROR` | 동적 HTML 주입 연산 시 외부 오염 유입 데이터가 전달되었습니다. XSS 보호막 무력화를 예방하기 위해 사전 이스케이프해야 합니다. | `java/spring/security/injection/tainted-html-string.yaml` |
| `tainted-url-host` | `ERROR` | URL 동적 문자열 조립 시 외부 오염 테두리 호스트 값이 주입됩니다. Open Redirect나 SSRF 위험이 있으니 주소를 정적 고정하거나 검증하세요. | `java/spring/security/injection/tainted-url-host.yaml` |

# Language: JAVASCRIPT

## ANGULAR

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `detect-angular-open-redirect` | `ERROR` | $window.location.href 연산에 사용자 입력이 그대로 대입되어 오픈 리디렉션 위협이 도사립니다. 도메인 화이트리스트 검출 후 도약시키세요. | `javascript/security/detect-angular-open-redirect.yaml` |
| `detect-angular-sce-disabled` | `ERROR` | $sceProvider가 false로 설정되어 엄격한 컨텍스트 이스케이프가 비활성화되었습니다. XSS 공격 방어를 위해 SCE를 활성화해야 합니다. | `javascript/security/detect-angular-sce-disabled.yaml` |

## AWS-LAMBDA

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `detect-child-process` | `ERROR` | child_process를 통한 하위 프로세스 생성 시 임의 인자가 탑재될 위험이 있습니다. 실행 코더와 인자를 고정 배열 스타일로 전달하세요. | `javascript/security/detect-child-process.yaml` |
| `dynamodb-request-object` | `ERROR` | DynamoDB 쿼리 매개변수 집계 시 $EVENT 유입 데이터가 소요됩니다. NoSQL 인젝션을 피하기 위해 입력 데이터를 정적 한정시키세요. | `javascript/security/dynamodb-request-object.yaml` |
| `tainted-sql-string` | `ERROR` | Lambda 가동 연산 스택에 유저 기반 SQL 문자열 조립이 탐지되었습니다. Parameterized Query를 사용하여 인젝션 요인을 차단하십시오. | `javascript/security/tainted-sql-string.yaml` |
| `vm-runincontext-injection` | `ERROR` | vm.runInContext() 호출에 외부 입력 데이터가 유입되어 샌드박스 우회 위험이 있습니다. 가변 코드 실행 연산을 중단하세요. | `javascript/security/vm-runincontext-injection.yaml` |

## BROWSER

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `dom-based-xss` | `ERROR` | URL 쿼리나 해시 데이터가 이스케이프 없이 화면 렌더링에 전사됩니다. DOM 기반 XSS 예방을 위해 주입 전 스크립트 특문을 정적 필터링하세... | `javascript/security/dom-based-xss.yaml` |
| `insecure-document-method` | `ERROR` | document.write 또는 innerHTML 에 외부 오염 데이터가 탑재되어 DOM-XSS 위험이 보입니다. 안전한 DOM 트리 생성 메서드로 변경하세요. | `javascript/security/insecure-document-method.yaml` |
| `insecure-innerhtml` | `ERROR` | $EL.innerHTML에 사용자 제어 데이터가 대입되고 있습니다. XSS 취약점을 유발하는 안티 패턴이므로 textContent 대체 사용 등을 고려하세요. | `javascript/security/insecure-innerhtml.yaml` |

## DENO

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `deno-dangerous-run` | `ERROR` | Deno.run() 호출 시 동적 문자열이 사용되었습니다. 명령어나 인자가 조작되어 커맨드 인젝션(Command Injection)이 발생할 수 있으므로 고정 배열 스타일을 적용하세요. | `javascript/security/audit/deno-dangerous-run.yaml` |

## EXPRESS

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `express-expat-xxe` | `ERROR` | expat XML 파서 구동 시 외부 입력에 검증이 부실합니다. XML External Entity (XXE) 취약점 격출을 무마하기 위해 보안 옵션을 비활성화 처리하십시오. | `javascript/security/express-expat-xxe.yaml` |
| `express-libxml-noent` | `ERROR` | libxml 라이브러리 처리 시 noent(Entity expansion) 속성이 true 로 인가되었습니다. XXE 취약점에 전방 노출되므로 이를 비활성화 처리하세요. | `javascript/security/audit/express-libxml-noent.yaml` |
| `express-phantom-injection` | `ERROR` | phantom API 호출에 사용자 통제 입력 데이터가 결합되었습니다. SSRF 및 인젝션 예방을 위해 사전에 검증된 정적 화이트리스트 맵을 구비하세요. | `javascript/security/express-phantom-injection.yaml` |
| `express-puppeteer-injection` | `ERROR` | puppeteer 인스턴스 메서드 구동 영역에 외부 동적 데이터가 도출됩니다. SSRF 유도 및 원격 클라이언트 브라우저 구동 조작을 차단하십시오. | `javascript/security/express-puppeteer-injection.yaml` |
| `express-sandbox-code-injection` | `ERROR` | sandbox 관련 호출에 사용자 입력 데이터가 도달했습니다. 샌드박스 내부에서 임의 코드가 실행될 수 있으므로 동적 조립을 배제하세요. | `javascript/security/express-sandbox-injection.yaml` |
| `express-vm-injection` | `ERROR` | Node.js vm 모듈 스크립트 실행 스택 등에 동적 사용자 오염 테두리가 가압되는 피로도를 잡습니다. 샌드박스 우회를 우려해 사전에 분리 차단하세요. | `javascript/security/express-vm-injection.yaml` |
| `express-wkhtmltoimage-injection` | `ERROR` | wkhtmltopdf 변환 연산 스택에 동적 오염 인자가 포진했습니다. SSRF와 파괴 인자 인젝션 예방을 위해 입력 주소를 필터링하십시오. | `javascript/security/express-wkhtml-injection.yaml` |
| `express-wkhtmltoimage-injection` | `ERROR` | wkhtmltopdf 변환 연산 스택에 동적 오염 인자가 포진했습니다. SSRF와 파괴 인자 인젝션 예방을 위해 입력 주소를 필터링하십시오. | `javascript/security/express-wkhtml-injection.yaml` |
| `express-xml2json-xxe` | `ERROR` | XML Parser로 입력되는 데이터 가공 시 외부 사용자 입력이 유출됩니다. XXE(XML External Entity) 공격 취약점을 유발하므로 파서에 DTD 로딩 및 외부 엔티티 호출을 차단하세요. | `javascript/security/express-xml2json-xxe.yaml` |
| `remote-property-injection` | `ERROR` | 대괄호 표기법([])에 사용자 입력이 반영되어 객체 속성에 접근하고 있습니다. 프로퍼티 인젝션 및 프로토타입 오염 위험이 있으니 입력값을 사전에 검증하세요. | `javascript/security/audit/remote-property-injection.yaml` |
| `require-request` | `ERROR` | require() 인자 위치에 동적 외부 입력이 발견되었습니다. 예상치 못한 스크립트/모듈 로딩 예방을 위해 정적 모듈 경로로 고정하십시오. | `javascript/security/require-request.yaml` |
| `tainted-sql-string` | `ERROR` | 동적 SQL 문자열 결합이 탐지되었습니다. SQL Injection 예방을 위해 객체 모델 바인딩 및 Parameterized Query 기법을 사용하세요. | `javascript/security/injection/tainted-sql-string.yaml` |

## GRPC

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `grpc-nodejs-insecure-connection` | `ERROR` | gRPC 연결 생성 시 암호화되지 않은 안전하지 않은 채널(createInsecure())이 사용되었습니다. 중간자 공격(MitM) 등에 무방비하므로 SSL/TLS 보완책을 적용하십시오. | `javascript/security/grpc-nodejs-insecure-connection.yaml` |

## JOSE

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `jwt-none-alg` | `ERROR` | jose 라이브러리 연산에서 서명 해제용 none 알고리즘 가압이 포착되었습니다. 변조 토큰 패싱을 예방하기 위해 보안 고정 알고리즘을 사용하십시오. | `javascript/security/jwt-none-alg.yaml` |

## JSONWEBTOKEN

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `jwt-none-alg` | `ERROR` | jsonwebtoken 서명 알고리즘에 검증 해제용 none 알고리즘 가압이 포착되었습니다. 변조 토큰 인용을 방지하기 위해 확실한 암호화 알고리즘만 허용하도록 고정하세요. | `javascript/security/jwt-none-alg.yaml` |

## JWT-SIMPLE

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `jwt-simple-noverify` | `ERROR` | jwt-simple 디코딩 수동 호출 시 서명 검증(verify) 단계가 누락되었습니다. 변조 토큰 우회를 막기 위해 반드시 검증 옵션을 활성화하세요. | `javascript/security/jwt-simple-noverify.yaml` |

## LANG

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `code-string-concat` | `ERROR` | 요청 데이터를 eval() 또는 Function() 실행 인자로 직접 연산 합사합니다. 원격 코드 실행(RCE) 타격을 유발하므로 동적 코드 실행을 금지하십시오. | `javascript/security/audit/code-string-concat.yaml` |
| `dangerous-spawn-shell` | `ERROR` | 비 리터럴 문자열을 실행 명령 매개체로 탑재하는 위험 spawn 구조를 감지했습니다. 명령 실행의 안정성을 위해 정적 리스트를 적용하세요. | `javascript/security/audit/dangerous-spawn-shell.yaml` |
| `detect-child-process` | `ERROR` | child_process 범용 호출 시 유입 인자의 정적 분기가 누락되었습니다. 커맨드 스페이스 조작에 의한 인젝션 방지를 위해 규격 배열을 고수하세요. | `javascript/security/detect-child-process.yaml` |
| `detect-insecure-websocket` | `ERROR` | 보안되지 않은 WebSocket(ws://) 연결이 감지되었습니다. 스니핑 공격을 예방하기 위해 암호화된 wss:// 연결을 사용하세요. | `javascript/security/detect-insecure-websocket.yaml` |
| `spawn-git-clone` | `ERROR` | git clone 실행 인자에 사용자 오염 가변 데이터가 유입되었습니다. 인자 인젝션 위험이 있으므로 주소를 고정하거나 정적 세탁하세요. | `javascript/security/spawn-git-clone.yaml` |
| `spawn-shell-true` | `ERROR` | spawn 구동 시 {shell: true} 옵션이 사용되었습니다. 인자 하이재킹에 취약하므로 옵션을 철회하고 배열형 인자를 명시하세요. | `javascript/security/audit/spawn-shell-true.yaml` |

## NODE-CRYPTO

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `aead-no-final` | `ERROR` | AEAD 암호 해독 객체의 final() 호출이 빠졌습니다. 인증 태그(Tag) 검증이 스킵되어 위조 데이터 분별이 안되므로 필수 호출하세요. | `javascript/security/aead-no-final.yaml` |
| `create-de-cipher-no-iv` | `ERROR` | 지원 중단된 createCipher 기용이 잡혔습니다. 암호화 해독 위험이 크므로 createCipheriv 로 고유 IV를 주입하여 보강하세요. | `javascript/security/create-de-cipher-no-iv.yaml` |
| `gcm-no-tag-length` | `ERROR` | GCM 모드 구동 시 createDecipheriv 에 인증 태그(Tag) 탑재 확인 옵션이 누락되었습니다. 데이터 무결성 검증을 위해 반드시 활성화하세요. | `javascript/security/gcm-no-tag-length.yaml` |

## REACT

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `calling-set-state-on-current-state` | `ERROR` | React Hooks에서 현재 상태(state) 값을 그대로 다시 setState에 주입하는 무의미한 연산이 감지되었습니다. 로직 실수를 검토하세요. | `javascript/correctness/hooks/set-state-no-op.yaml` |

## SEQUELIZE

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `express-sequelize-injection` | `ERROR` | Sequelize 바인딩 스택에 인화성 가변 파라미터가 유입됩니다. SQL Injection 방어를 위해 ORM 규격 바인딩(replacements)을 쓰세요. | `javascript/security/audit/sequelize-injection-express.yaml` |
| `sequelize-tls-disabled-cert-validation` | `ERROR` | Sequelize 설정 중 인증서 검증을 우회(rejectUnauthorized: false)하는 상태가 감지되었습니다. 중간자 공격에 도출되므로 프로덕션 배포 시 철회하십시오. | `javascript/security/audit/sequelize-tls-disabled-cert-validation.yaml` |

## SHELLJS

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `shelljs-exec-injection` | `ERROR` | shelljs.exec() 호출 연산에 외부 사용자 오염 가변 데이터가 주입되었습니다. RCE(원격코드실행) 위협이 가중되므로 인자 분할 형식으로 전환하십시오. | `javascript/security/shelljs-exec-injection.yaml` |

# Language: JSON

## AWS

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `wildcard-assume-role` | `ERROR` | wildcard-assume-role 보안 인젝션 및 런타임 버그 전사 예방 점검. | `json/security/wildcard-assume-role.yaml` |

# Language: KOTLIN

## LANG

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `command-injection-formatted-runtime-call` | `ERROR` | java.lang.Runtime 호출 인자에 가변 포맷 또는 동적 합산 문자열이 감지되었습니다. 외부 입력 탑재 시 명령어 주입(Command Injection) 위협이 가중되므로 정적 분할 전달이나 세척을 거치십시오. | `kotlin/security/command-injection-formatted-runtime-call.yaml` |

# Language: PYTHON

## AIRFLOW

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `formatted-string-bashoperator` | `ERROR` | BashOperator 내부 가동 인자에 가변 합사가 포착되었습니다. 외부 주입 우려 노출을 전사 단속하십시오. | `python/security/audit/formatted-string-bashoperator.yaml` |

## AWS-LAMBDA

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `dangerous-asyncio-create-exec` | `ERROR` | create_subprocess_exec 버퍼에 외부 데이터 합치기가 발견되었습니다. 인젝션 예방을 위해 필터링 하세요. | `python/security/dangerous-asyncio-create-exec.yaml` |
| `dangerous-asyncio-exec` | `ERROR` | subprocess_exec 가동 시 유저 리스트 오염 인자가 흐릅니다. 가변 탑재를 배제하십시오. | `python/security/dangerous-asyncio-exec.yaml` |
| `dangerous-asyncio-shell` | `ERROR` | asyncio 쉘 연산에 가변 인자가 합사되었습니다. 명령어 주입 우려가 있으니 shlex 세척을 권장합니다. | `python/security/dangerous-asyncio-shell.yaml` |
| `dangerous-spawn-process` | `ERROR` | os 바이너리 스폰 가동에 event 가변 오염이 흐릅니다. 쉘 명령어 덤프 RCE 차단을 위해 전사 단속하십시오. | `python/security/dangerous-spawn-process.yaml` |
| `dangerous-subprocess-use` | `ERROR` | subprocess 구동 시 shell=True 탑재 탑재로 보안 결함이 높습니다. 가변 인자 결합을 철회하십시오. | `python/security/dangerous-subprocess-use.yaml` |
| `dangerous-system-call` | `ERROR` | os 모듈 가동에 event 오염 인자가 유입됩니다. 인젝션 위험이 극에 달하므로 subprocess를 고용하세요. | `python/security/dangerous-system-call.yaml` |
| `dynamodb-filter-injection` | `ERROR` | DynamoDB 쿼리 필터에 $EVENT 유입 인자가 도주합니다. NoSQL 인젝션 예방을 위해 정적 할당 하십시오. | `python/security/dynamodb-filter-injection.yaml` |
| `tainted-sql-string` | `ERROR` | Lambda 가동 내 동적 SQL 조립이 탐지되었습니다. Parameterized Query를 사용하여 요인을 차단하십시오. | `python/security/tainted-sql-string.yaml` |

## CLICK

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `use-click-secho` | `ERROR` | click.echo()와 style() 수동 배합 대신 click.secho() 연쇄 고용을 권장합니다. | `python/best-practice/echo-style.yaml` |

## CRYPTOGRAPHY

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `crypto-mode-without-authentication` | `ERROR` | 무결성 검증 없는 암호화 운영 모드가 사용되었습니다. GCM 등 AEAD 모드로 교정하세요. | `python/security/mode-without-authentication.yaml` |

## DJANGO

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `avoid-insecure-deserialization` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 avoid-insecure-deserialization 전사 단속이 요구됩니다. | `python/security/audit/avoid-insecure-deserialization.yaml` |
| `command-injection-os-system` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 command-injection-os-system 전사 단속이 요구됩니다. | `python/security/injection/command/command-injection-os-system.yaml` |
| `csv-writer-injection` | `ERROR` | CSV 가동 인자 인젝션 방어를 조율 하십시오. | `python/security/injection/csv-writer-injection.yaml` |
| `duplicate-path-assignment` | `ERROR` | 서로 다른 경로에 동일한 URL 이름(`$NAME`)이 중복 할당되어 있습니다. 이름 충돌을 방지하기 위해 각 경로에 고유한 이름을 지정해 주세요. | `python/maintainability/duplicate-path-assignment.yaml` |
| `globals-as-template-context` | `ERROR` | globals() 전역 인출 피칭 국면을 경보합니다. | `python/security/globals-as-template-context.yaml` |
| `hashids-with-django-secret` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 hashids-with-django-secret 전사 단속이 요구됩니다. | `python/security/hashids-with-django-secret.yaml` |
| `locals-as-template-context` | `ERROR` | locals() 직접 전사로 내부 탑재 변수가 외부에 탈주 폭주하는 위험 레이어를 점검합니다. | `python/security/locals-as-template-context.yaml` |
| `nan-injection` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 nan-injection 전사 단속이 요구됩니다. | `python/security/nan-injection.yaml` |
| `nontext-field-must-set-null-true` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 nontext-field-must-set-null-true 전사 단속이 요구됩니다. | `python/correctness/nontext-field-must-set-null-true.yaml` |
| `password-empty-string` | `ERROR` | 빈 문자열로 패스워드가 세팅되는 안티 무방비 보안 지점을 진압합니다. | `python/security/passwords/password-empty-string.yaml` |
| `ssrf-injection-requests` | `ERROR` | 서버 측 요청 위조(SSRF) 누출 피싱 주소 교정. | `python/security/injection/ssrf/ssrf-injection-requests.yaml` |
| `ssrf-injection-urllib` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 ssrf-injection-urllib 전사 단속이 요구됩니다. | `python/security/injection/ssrf/ssrf-injection-urllib.yaml` |
| `no-null-string-field` | `ERROR` | unique=True와 blank=True를 함께 선언하는 문자열 필드는 null=True도 반드시 설정해야 합니다. 그렇지 않으면 빈 값으로 여러 레코드를 저장할 때 고유 제약 조건 위반이 발생할 수 있습니다. | `python/correctness/string-field-null-checks.yaml` |
| `subprocess-injection` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 subprocess-injection 전사 단속이 요구됩니다. | `python/security/injection/command/subprocess-injection.yaml` |
| `tainted-sql-string` | `ERROR` | 동적 SQL 문자열 결합 유출이 포착되어 Parameterized 쿼리를 독촉합니다. | `python/security/injection/tainted-sql-string.yaml` |
| `use-count-method` | `ERROR` | .count() 헬퍼 가동으로 쿼리 집계 가속을 도모 하세요. | `python/performance/upsell-count.yaml` |
| `use-decimalfield-for-money` | `ERROR` | 금액 필드에 부동 소수점 오차를 막기 위해 DecimalField를 사수 하십시오. | `python/correctness/use-decimalfield-for-money.yaml` |
| `use-django-environ` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 use-django-environ 전사 단속이 요구됩니다. | `python/best-practice/upsell_django_environ.yaml` |
| `use-earliest-or-latest` | `ERROR` | use-earliest-or-latest 보안 인젝션 및 런타임 버그 전사 예방 점검. | `python/performance/upsell_earliest_latest.yaml` |
| `use-json-response` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 use-json-response 전사 단속이 요구됩니다. | `python/best-practice/json_response.yaml` |
| `use-none-for-password-default` | `ERROR` | 비밀번호 기본 데이터에 무효 인자 바인딩을 권장합니다. | `python/security/passwords/use-none-for-password-default.yaml` |

## FLASK

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `csv-writer-injection` | `ERROR` | 내장 csv 모듈에 검증 실종 동동 데이터를 공급 중입니다. 매크로 주입 방어를 위해 특수 서식 이격을 거치세요. | `python/security/injection/csv-writer-injection.yaml` |
| `dangerous-template-string` | `ERROR` | 가변 스트링 합사를 통한 동적 템플릿 생산이 잡혔습니다. SSTI 예방을 위해 객체 렌더링 양식을 쓰세요. | `python/security/dangerous-template-string.yaml` |
| `eval-injection` | `ERROR` | eval() 연산 버퍼에 가변 사용자 동적 연산 입력이 관여합니다. 원격 코드 실행(RCE) 타격을 유발하므로 즉각 피하십시오. | `python/security/injection/user-eval.yaml` |
| `exec-injection` | `ERROR` | exec() 연산 버퍼에 가변 사용자 동적 인가 데이터가 합사됩니다. RCE 극심한 타격이 상존하니 중지하십시오. | `python/security/injection/user-exec.yaml` |
| `flask-api-method-string-format` | `ERROR` | 컨트롤러 연산에 유저 가변 문자열이 수동 가압됩니다. 인젝션 등 우회 타격 부재를 조심하십시오. | `python/security/flask-api-method-string-format.yaml` |
| `hashids-with-flask-secret` | `ERROR` | Flask SECRET_KEY를 HashIDs Salt로 오용했습니다. 해시 파싱 중 무력화 위협이 있으니 전용 값을 할당하세요. | `python/security/hashids-with-flask-secret.yaml` |
| `insecure-deserialization` | `ERROR` | 취약한 역직렬화 라이브러리가 감지되었습니다. RCE 공격 위험을 막기 위해 JSON 등 안전한 형태를 이용하세요. | `python/security/insecure-deserialization.yaml` |
| `nan-injection` | `ERROR` | 유저 입력이 typecast(float 등) 안으로 직접 유출됩니다. 데이터 연산 우회 조작이 발견될 수 있으니 검사하세요. | `python/security/injection/nan-injection.yaml` |
| `open-redirect` | `ERROR` | 외부 유입 주소 파라미터가 가공 없이 redirect()로 유출됩니다. 오픈 리디렉션 피싱 방지를 위해 사전 검출 검사하세요. | `python/security/open-redirect.yaml` |
| `os-system-injection` | `ERROR` | os.system() 가승 연산 버퍼에 동적 조합이 도칩니다. Command Injection 피싱 격량을 타개하기 위해 철회하십시오. | `python/security/injection/os-system-injection.yaml` |
| `path-traversal-open` | `ERROR` | open() 가동에 유저 노출 경로 데이터가 전사됩니다. 로컬 파일 시스템 탈취를 막고자 사전에 정적 이격 시키세요. | `python/security/injection/path-traversal-open.yaml` |
| `ssrf-requests` | `ERROR` | HTTP 발송 인자에 오염 입력이 통과 탑재됩니다. SSRF 탈취를 예방하기 위해 조율 주소를 엄밀하게 교정하세요. | `python/security/injection/ssrf-requests.yaml` |
| `subprocess-injection` | `ERROR` | subprocess 가동 인자에 가변 오염 입력이 포착되었습니다. 커맨드 인젝션 격퇴를 위해 파라미터 분할 배열형을 고수하십시오. | `python/security/injection/subprocess-injection.yaml` |
| `tainted-sql-string` | `ERROR` | 동적 SQL 문자열 결합이 포착되었습니다. SQL Injection 배후 차단을 위해 Parameterized Query를 사수하세요. | `python/security/injection/tainted-sql-string.yaml` |
| `use-jsonify` | `ERROR` | 수동 딕셔너리 연계 반환보다 flask.jsonify() 내장 헬퍼를 이용하여 안정성을 유치할 것을 권합합니다. | `python/best-practice/use-jsonify.yaml` |

## JWT

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `jwt-python-exposed-credentials` | `ERROR` | JWT 토큰 페이로드에 기밀 정보가 노출되었습니다. 페이로드는 암호화되지 않으므로 유출 위험이 큽니다. | `python/security/jwt-exposed-credentials.yaml` |
| `jwt-python-hardcoded-secret` | `ERROR` | 하드코딩된 JWT 비밀키가 발견되었습니다. 보안 누출 예방을 위해 환경 변수나 보안 저장소로 이전하세요. | `python/security/jwt-hardcode.yaml` |
| `jwt-python-none-alg` | `ERROR` | JWT 서명 검증에서 none 알고리즘 사용이 감지되었습니다. 변조 토큰 우회를 피하기 위해 명시적 암호화를 지정하세요. | `python/security/jwt-none-alg.yaml` |
| `unverified-jwt-decode` | `ERROR` | JWT 디코딩 시 verify=False 플래그가 발견되었습니다. 무결성 검증을 위해 누출 옵션을 활성화하십시오. | `python/security/unverified-jwt-decode.yaml` |

## LANG

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `arbitrary-sleep` | `ERROR` | 가동 루프 내 sleep 병목 지점을 확인하세요. | `python/best-practice/sleep.yaml` |
| `avoid-pyyaml-load` | `ERROR` | 취약한 PyYAML load() 가동이 식별되었습니다. RCE 예방을 위해 safe_load()로 대두 전개 처리 하십시오. | `python/security/deserialization/avoid-pyyaml-load.yaml` |
| `avoid-unsafe-ruamel` | `ERROR` | 동격의 Yaml 파서 인 안전하지 않은 로드 형태 포착. safe 로드 구성을 승인하세요. | `python/security/deserialization/avoid-unsafe-ruamel.yaml` |
| `dangerous-asyncio-create-exec-audit` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 dangerous-asyncio-create-exec-audit 전사 단속이 요구됩니다. | `python/security/audit/dangerous-asyncio-create-exec-audit.yaml` |
| `dangerous-asyncio-create-exec-tainted-env-args` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 dangerous-asyncio-create-exec-tainted-env-args 전사 단속이 요구됩니다. | `python/security/audit/dangerous-asyncio-create-exec-tainted-env-args.yaml` |
| `dangerous-asyncio-exec-audit` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 dangerous-asyncio-exec-audit 전사 단속이 요구됩니다. | `python/security/audit/dangerous-asyncio-exec-audit.yaml` |
| `dangerous-asyncio-exec-tainted-env-args` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 dangerous-asyncio-exec-tainted-env-args 전사 단속이 요구됩니다. | `python/security/audit/dangerous-asyncio-exec-tainted-env-args.yaml` |
| `dangerous-asyncio-shell-audit` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 dangerous-asyncio-shell-audit 전사 단속이 요구됩니다. | `python/security/audit/dangerous-asyncio-shell-audit.yaml` |
| `dangerous-asyncio-shell-tainted-env-args` | `ERROR` | 환경 변수 또는 외부 입력이 비동기 쉘 명령 실행에 직접 사용되고 있습니다. 커맨드 인젝션 취약점을 예방하려면 입력값을 엄격히 검증하거나 쉘을 사용하지 않는 방식으로 전환하세요. | `python/security/audit/dangerous-asyncio-shell-tainted-env-args.yaml` |
| `dangerous-os-exec` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 dangerous-os-exec 전사 단속이 요구됩니다. | `python/security/dangerous-os-exec.yaml` |
| `dangerous-os-exec-audit` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 dangerous-os-exec-audit 전사 단속이 요구됩니다. | `python/security/audit/dangerous-os-exec-audit.yaml` |
| `dangerous-os-exec-tainted-env-args` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 dangerous-os-exec-tainted-env-args 전사 단속이 요구됩니다. | `python/security/audit/dangerous-os-exec-tainted-env-args.yaml` |
| `dangerous-spawn-process` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 dangerous-spawn-process 전사 단속이 요구됩니다. | `python/security/dangerous-spawn-process.yaml` |
| `dangerous-spawn-process-audit` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 dangerous-spawn-process-audit 전사 단속이 요구됩니다. | `python/security/audit/dangerous-spawn-process-audit.yaml` |
| `dangerous-spawn-process-tainted-env-args` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 dangerous-spawn-process-tainted-env-args 전사 단속이 요구됩니다. | `python/security/audit/dangerous-spawn-process-tainted-env-args.yaml` |
| `dangerous-subprocess-use` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 dangerous-subprocess-use 전사 단속이 요구됩니다. | `python/security/dangerous-subprocess-use.yaml` |
| `dangerous-subprocess-use-audit` | `ERROR` | 하위 프로세스 생성 드라이버 인젝션 전담 점검. | `python/security/audit/dangerous-subprocess-use-audit.yaml` |
| `dangerous-subprocess-use-tainted-env-args` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 dangerous-subprocess-use-tainted-env-args 전사 단속이 요구됩니다. | `python/security/audit/dangerous-subprocess-use-tainted-env-args.yaml` |
| `dangerous-system-call` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 dangerous-system-call 전사 단속이 요구됩니다. | `python/security/dangerous-system-call.yaml` |
| `dangerous-system-call-audit` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 dangerous-system-call-audit 전사 단속이 요구됩니다. | `python/security/audit/dangerous-system-call-audit.yaml` |
| `dangerous-system-call-tainted-env-args` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 dangerous-system-call-tainted-env-args 전사 단속이 요구됩니다. | `python/security/audit/dangerous-system-call-tainted-env-args.yaml` |
| `default-mutable-dict` | `ERROR` | 가변 Dict를 함수 기본 인자로 탑재하여 전역 버퍼 오염을 유도하는 Pitfall을 경보합니다. None 분기가 요망됩니다. | `python/correctness/common-mistakes/default-mutable-dict.yaml` |
| `default-mutable-list` | `ERROR` | 가변 List 기본 인자 탑재로 인한 버퍼 공유 격량. None 매핑으로 필터 하세요. | `python/correctness/common-mistakes/default-mutable-list.yaml` |
| `disabled-cert-validation` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 disabled-cert-validation 전사 단속이 요구됩니다. | `python/security/audit/network/disabled-cert-validation.yaml` |
| `http-not-https-connection` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 http-not-https-connection 전사 단속이 요구됩니다. | `python/security/audit/network/http-not-https-connection.yaml` |
| `is-not-is-not` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 is-not-is-not 전사 단속이 요구됩니다. | `python/correctness/common-mistakes/is-not-is-not.yaml` |
| `list-modify-while-iterate` | `ERROR` | for 루프 순회 중 원본 리스트를 가변 삭제/수정하여 오동작을 격발시키는 리스크 누출입니다. | `python/correctness/list-modify-iterating.yaml` |
| `no-strings-as-booleans` | `ERROR` | 문자열 결합 시 연산 논리 혼선 국면을 저지합니다. | `python/correctness/useless-comparison.yaml` |
| `open-never-closed` | `ERROR` | 디스크 서술자 닫기 연쇄가 빠졌습니다. | `python/best-practice/open-never-closed.yaml` |
| `paramiko-exec-command` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 paramiko-exec-command 전사 단속이 요구됩니다. | `python/security/audit/paramiko/paramiko-exec-command.yaml` |
| `python36-compatibility-ssl` | `ERROR` | 해당 함수 및 문법은 해당 파이썬 버전 연산 지원 사양입니다. | `python/compatibility/python36.yaml` |
| `python37-compatibility-importlib` | `ERROR` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `python/compatibility/python37.yaml` |
| `raise-not-base-exception` | `ERROR` | raise-not-base-exception 보안 인젝션 및 런타임 버그 전사 예방 점검. | `python/correctness/exceptions/exceptions.yaml` |
| `identical-is-comparison` | `ERROR` | 문자열 동등 비교는 is가 아닌 == 연산자를 구동하여 안정성을 가두어야 합니다. | `python/correctness/common-mistakes/is-comparison-string.yaml` |
| `subprocess-shell-true` | `ERROR` | shell=True 위험 옵션을 우회 처리하십시오. | `python/security/audit/subprocess-shell-true.yaml` |
| `tempfile-insecure` | `ERROR` | tempfile-insecure 보안 인젝션 및 런타임 버그 전사 예방 점검. | `python/correctness/tempfile/mktemp.yaml` |
| `tempfile-without-flush` | `ERROR` | tempfile-without-flush 보안 인젝션 및 런타임 버그 전사 예방 점검. | `python/correctness/tempfile/flush.yaml` |
| `unverified-ssl-context` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 unverified-ssl-context 전사 단속이 요구됩니다. | `python/security/unverified-ssl-context.yaml` |
| `use-defused-xml` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 use-defused-xml 전사 단속이 요구됩니다. | `python/security/use-defused-xml.yaml` |
| `use-defused-xml-parse` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 use-defused-xml-parse 전사 단속이 요구됩니다. | `python/security/use-defused-xml-parse.yaml` |
| `use-defused-xmlrpc` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 use-defused-xmlrpc 전사 단속이 요구됩니다. | `python/security/use-defused-xmlrpc.yaml` |
| `useless-inner-function` | `ERROR` | 내부 함수가 정의되었으나 사용 연동이 누락되었습니다. 코드 가독성을 위해 말소 대상 점검 하십시오. | `python/maintainability/useless-innerfunction.yaml` |
| `useless-literal-set` | `ERROR` | set 조립 단에 중복 할당 조각이 보입니다. | `python/maintainability/useless-literal-set.yaml` |
| `writing-to-file-in-read-mode` | `ERROR` | 읽기 전용으로 가동 중인 서술자에 쓰기(.write)를 가압하는 런타임 에러를 경보합니다. | `python/correctness/writing-to-file-in-read-mode.yaml` |
| `return-in-init` | `ERROR` | __init__ 내부 yield 전사 금기 양식. | `python/correctness/return-in-init.yaml` |

## PYCRYPTODOME

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `crypto-mode-without-authentication` | `ERROR` | 무결성 검증 없는 암호화 운영 모드가 사용되었습니다. GCM 등 AEAD 모드 사용을 권장합니다. | `python/security/mode-without-authentication.yaml` |

## PYRAMID

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `pyramid-csrf-check-disabled-globally` | `ERROR` | Pyramid 전역 CSRF 방어가 비활성화되었습니다. 뷰 보호를 위해 토크나이저를 구동하십시오. | `python/security/csrf-check-disabled-globally.yaml` |
| `pyramid-csrf-origin-check-disabled-globally` | `ERROR` | Pyramid Referrer CSRF 검증 전역 누락 감지. Origin 체크 옵션을 활성화하십시오. | `python/audit/csrf-origin-check-disabled-globally.yaml` |
| `pyramid-direct-use-of-response` | `ERROR` | Response 객체를 렌더링 없이 날것으로 출력합니다. XSS 방어 레이어 우회 우려가 있습니다. | `python/security/direct-use-of-response.yaml` |
| `pyramid-sqlalchemy-sql-injection` | `ERROR` | distinct/having절 내 원시 SQL 인젝션 가동 현상 감지. bindparams 규격을 준행하세요. | `python/security/sqlalchemy-sql-injection.yaml` |

## REQUESTS

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `disabled-cert-validation` | `ERROR` | requests 가동 시 인증서 검증(verify=False) 탑재는 중간자 노출을 가동합니다. 재활성화 하세요. | `python/security/disabled-cert-validation.yaml` |
| `no-auth-over-http` | `ERROR` | HTTP 평문 채널을 통한 인증 전송이 포착되었습니다. 스니핑 격퇴를 위해 https:// 도약을 강제 하십시오. | `python/security/no-auth-over-http.yaml` |

## SH

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `string-concat` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 string-concat 전사 단속이 요구됩니다. | `python/security/string-concat.yaml` |

## SQLALCHEMY

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `avoid-sqlalchemy-text` | `ERROR` | sqlalchemy.text() 구동 시 동적 스트링 합사 버그가 우려됩니다. ORM 규격 모델을 준행 하세요. | `python/security/audit/avoid-sqlalchemy-text.yaml` |
| `delete-where-no-execute` | `ERROR` | SQLAlchemy .delete() 연산 시 .where() 스킵 국면이 감지되었습니다. 전사 데이터 유실에 대비하십시오. | `python/correctness/delete-where.yaml` |
| `sqlalchemy-execute-raw-query` | `ERROR` | SQLAlchemy 원시 쿼리 동적 결합 감지. 인젝션 투하를 막으려면 Parameterized 선언을 장착 하십시오. | `python/security/sqlalchemy-execute-raw-query.yaml` |

# Language: TERRAFORM

## AWS

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `aws-glacier-vault-any-principal` | `ERROR` | IaC 보안 옵션 누락 경보: aws-glacier-vault-any-principal 설정율을 적용해 주십시오. | `terraform/security/aws-glacier-vault-any-principal.yaml` |
| `aws-iam-admin-policy` | `ERROR` | IaC 보안 옵션 누락 경보: aws-iam-admin-policy 설정율을 적용해 주십시오. | `terraform/security/aws-iam-admin-policy.yaml` |
| `aws-iam-admin-policy-ssoadmin` | `ERROR` | IaC 보안 옵션 누락 경보: aws-iam-admin-policy-ssoadmin 설정율을 적용해 주십시오. | `terraform/security/aws-iam-admin-policy-ssoadmin.yaml` |
| `aws-kms-key-wildcard-principal` | `ERROR` | Terraform 구성 중 와일드카드(*) 권한 과잉 부여가 식별되었습니다. | `terraform/security/aws-kms-key-wildcard-principal.yaml` |
| `aws-lambda-environment-credentials` | `ERROR` | IaC 보안 옵션 누락 경보: aws-lambda-environment-credentials 설정율을 적용해 주십시오. | `terraform/security/aws-lambda-environment-credentials.yaml` |
| `aws-lambda-permission-unrestricted-source-arn` | `ERROR` | IaC 보안 옵션 누락 경보: aws-lambda-permission-unrestricted-source-arn 설정율을 적용해 주십시오. | `terraform/security/aws-lambda-permission-unrestricted-source-arn.yaml` |
| `aws-sqs-queue-policy-wildcard-principal` | `ERROR` | Terraform 구성 중 와일드카드(*) 권한 과잉 부여가 식별되었습니다. | `terraform/security/aws-sqs-queue-policy-wildcard-principal.yaml` |
| `wildcard-assume-role` | `ERROR` | Terraform 구성 중 와일드카드(*) 권한 과잉 부여가 식별되었습니다. | `terraform/security/wildcard-assume-role.yaml` |

## AZURE

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `appservice-authentication-enabled` | `ERROR` | IaC 보안 옵션 누락 경보: appservice-authentication-enabled 설정율을 적용해 주십시오. | `terraform/security/appservice/appservice-authentication-enabled.yaml` |
| `appservice-enable-https-only` | `ERROR` | IaC 보안 옵션 누락 경보: appservice-enable-https-only 설정율을 적용해 주십시오. | `terraform/security/appservice/appservice-enable-https-only.yaml` |
| `appservice-use-secure-tls-policy` | `ERROR` | IaC 보안 옵션 누락 경보: appservice-use-secure-tls-policy 설정율을 적용해 주십시오. | `terraform/security/appservice/appservice-use-secure-tls-policy.yaml` |
| `keyvault-specify-network-acl` | `ERROR` | IaC 보안 옵션 누락 경보: keyvault-specify-network-acl 설정율을 적용해 주십시오. | `terraform/security/keyvault/keyvault-specify-network-acl.yaml` |
| `storage-default-action-deny` | `ERROR` | IaC 보안 옵션 누락 경보: storage-default-action-deny 설정율을 적용해 주십시오. | `terraform/security/storage/storage-default-action-deny.yaml` |
| `storage-use-secure-tls-policy` | `ERROR` | IaC 보안 옵션 누락 경보: storage-use-secure-tls-policy 설정율을 적용해 주십시오. | `terraform/security/storage/storage-use-secure-tls-policy.yaml` |

## LANG

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `ec2-imdsv1-optional` | `ERROR` | IaC 보안 옵션 누락 경보: ec2-imdsv1-optional 설정율을 적용해 주십시오. | `terraform/security/ec2-imdsv1-optional.yaml` |
| `s3-public-rw-bucket` | `ERROR` | IaC 보안 옵션 누락 경보: s3-public-rw-bucket 설정율을 적용해 주십시오. | `terraform/security/s3-public-rw-bucket.yaml` |

# Language: TYPESCRIPT

## AWS-CDK

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `aws-cdk-bucket-enforcessl` | `ERROR` | S3 버킷에 전송 중 암호화(SSL/TLS) 강제화 옵션이 누락되었습니다. 데이터 전송 기밀성을 위해 해당 옵션을 활성화하십시오. | `typescript/security/audit/awscdk-bucket-enforcessl.yml` |
| `awscdk-bucket-encryption` | `ERROR` | AWS CDK S3 버킷 생성 시 기본 암호화(KMS_MANAGED 등) 설정이 누락되었습니다. 데이터 보안을 위해 암호화 모드를 지정하세요. | `typescript/security/audit/awscdk-bucket-encryption.yml` |

## LANG

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `useless-ternary` | `ERROR` | 불필요한 삼항 연산자(a ? true : false 등) 사용이 감지되었습니다. 논리 직관성을 위해 단순 불리언 캐스팅 등으로 대체하세요. | `typescript/correctness/useless-ternary.yaml` |

## REACT

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `react-insecure-request` | `ERROR` | React 애플리케이션에서 암호화되지 않은 HTTP 요청이 감지되었습니다. 스니핑 공격에 노출되므로 https:// 사용을 권장합니다. | `typescript/security/react-insecure-request.yaml` |

# Language: YAML

## ARGO

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `argo-workflow-parameter-command-injection` | `ERROR` | Argo 워크플로우 매개변수 가동 중 원격 명령어 주입(Command Injection) 우려가 수렴됩니다. | `yaml/security/argo-workflow-parameter-command-injection.yaml` |

## GITHUB-ACTIONS

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `curl-eval` | `ERROR` | curl-eval 보안 인젝션 및 런타임 버그 전사 예방 점검. | `yaml/security/curl-eval.yaml` |
| `detect-shai-hulud-backdoor` | `ERROR` | detect-shai-hulud-backdoor 보안 인젝션 및 런타임 버그 전사 예방 점검. | `yaml/security/detect-shai-hulud-backdoor.yaml` |
| `github-script-injection` | `ERROR` | github-script-injection 보안 인젝션 및 런타임 버그 전사 예방 점검. | `yaml/security/github-script-injection.yaml` |
| `run-shell-injection` | `ERROR` | run-shell-injection 보안 인젝션 및 런타임 버그 전사 예방 점검. | `yaml/security/run-shell-injection.yaml` |

## OPENAPI

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `use-of-basic-authentication` | `ERROR` | use-of-basic-authentication 보안 인젝션 및 런타임 버그 전사 예방 점검. | `yaml/security/use-of-basic-authentication.yaml` |

## SEMGREP

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `- id: duplicate-id` | `ERROR` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `yaml/duplicate-id.yaml` |
| `duplicate-pattern` | `ERROR` | Semgrep 규칙 저작 메타 데이터 정합성 점검: duplicate-pattern 누락 경보. | `yaml/duplicate-pattern.yaml` |
| `metadata-cwe` | `ERROR` | Semgrep 규칙 저작 메타 데이터 정합성 점검: metadata-cwe 누락 경보. | `yaml/metadata-cwe.yaml` |
| `metadata-cwe-prohibited-or-discouraged` | `ERROR` | Semgrep 규칙 저작 메타 데이터 정합성 점검: metadata-cwe-prohibited-or-discouraged 누락 경보. | `yaml/metadata-cwe-prohibited-or-discouraged.yaml` |
| `metadata-license` | `ERROR` | Semgrep 규칙 저작 메타 데이터 정합성 점검: metadata-license 누락 경보. | `yaml/metadata-license.yaml` |
| `metadata-owasp` | `ERROR` | Semgrep 규칙 저작 메타 데이터 정합성 점검: metadata-owasp 누락 경보. | `yaml/metadata-owasp.yaml` |
| `metadata-references` | `ERROR` | Semgrep 규칙 저작 메타 데이터 정합성 점검: metadata-references 누락 경보. | `yaml/metadata-references.yaml` |
| `unsatisfiable-rule` | `ERROR` | Semgrep 규칙 저작 메타 데이터 정합성 점검: unsatisfiable-rule 누락 경보. | `yaml/unsatisfiable.yaml` |

