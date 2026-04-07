# Java Semgrep Rules Summary

`java` 디렉토리 하위의 규칙 목록입니다. (테스트 파일 제외)

## ANDROID

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `exported_activity` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `android/security/exported_activity.yaml` |

## AWS-LAMBDA

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `tainted-sql-string` | `ERROR` | AWS Lambda 핸들러 등의 외부 사용자 입력이 직접 SQL 문자열 조립에 사용되었습니다. Parameterized Query를 사용하여 SQL 인젝션을 예방하세요. | `aws-lambda/security/tainted-sql-string.yaml` |
| `tainted-sqli` | `WARNING` | 잠재적 SQL 인젝션 취약점이 감지되었습니다. Parameterized Query나 ORM 모델을 준행하세요. | `aws-lambda/security/tainted-sqli.yaml` |

## JAVA-JWT

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `java-jwt-decode-without-verify` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `java-jwt/security/audit/jwt-decode-without-verify.yaml` |
| `java-jwt-hardcoded-secret` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `java-jwt/security/jwt-hardcode.yaml` |

## JAX-RS

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `default-resteasy-provider-abuse` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `jax-rs/security/insecure-resteasy.yaml` |
| `insecure-resteasy-deserialization` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `jax-rs/security/insecure-resteasy.yaml` |
| `jax-rs-path-traversal` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `jax-rs/security/jax-rs-path-traversal.yaml` |

## JBOSS

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `seam-log-injection` | `ERROR` | Seam Logging API에 외부 데이터가 그대로 주입되었습니다. 표현식 언어(EL)를 통해 로깅 시스템이 공격받을 수 있으므로 주입 전 엄격한 검증을 통과해야 합니다. | `jboss/security/seam-log-injection.yaml` |

## LANG

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `assignment-comparison` | `ERROR` | 조건식 내부에서 대입 연산자(=)가 사용되고 있습니다. 의도치 않게 할당이 일어나 비교가 고장날 우려가 있습니다. | `lang/correctness/assignment-comparison.yaml` |
| `autoescape-disabled` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `lang/security/audit/xss/jsf/autoescape-disabled.yaml` |
| `bad-hexa-conversion` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `lang/security/audit/bad-hexa-conversion.yaml` |
| `blowfish-insufficient-key-size` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `lang/security/audit/blowfish-insufficient-key-size.yaml` |
| `cbc-padding-oracle` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `lang/security/audit/cbc-padding-oracle.yaml` |
| `command-injection-formatted-runtime-call` | `ERROR` | Runtime.exec에 동적 조립 문자열(String.format 등)을 인자로 전달하여 커맨드 인젝션 위험이 있습니다. 안정성을 위해 인자 리스트(String[]) 형식으로 전달하세요. | `lang/security/audit/command-injection-formatted-runtime-call.yaml` |
| `command-injection-process-builder` | `ERROR` | ProcessBuilder를 이용한 명령어 가동 시 가변 포매터 및 동적 조립 문자열이 사용되었습니다. 리스트형 인자 전달 스타일로 변경하세요. | `lang/security/audit/command-injection-process-builder.yaml` |
| `cookie-missing-httponly` | `WARNING` | 쿠키에 보안 속성(Secure/HttpOnly)이 누락되어 세션 탈취(XSS/MitM)에 노출될 수 있습니다. | `lang/security/audit/cookie-missing-httponly.yaml` |
| `cookie-missing-secure-flag` | `WARNING` | 쿠키에 보안 속성(Secure/HttpOnly)이 누락되어 세션 탈취(XSS/MitM)에 노출될 수 있습니다. | `lang/security/audit/cookie-missing-secure-flag.yaml` |
| `crlf-injection-logs` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `lang/security/audit/crlf-injection-logs.yaml` |
| `dangerous-groovy-shell` | `WARNING` | Groovy Shell 직접 구동 파사드에 위험 요소 존재할 수 있습니다. | `lang/security/audit/dangerous-groovy-shell.yaml` |
| `defaulthttpclient-is-deprecated` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `lang/security/audit/crypto/ssl/defaulthttpclient-is-deprecated.yaml` |
| `desede-is-deprecated` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `lang/security/audit/crypto/desede-is-deprecated.yaml` |
| `do-privileged-use` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `lang/security/do-privileged-use.yaml` |
| `el-injection` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `lang/security/audit/el-injection.yaml` |
| `eqeq` | `ERROR` | $X == $X 또는 $X != $X 와 같이 본인 자신을 직접 비교하고 있습니다. 로직 실수이거나 무의미한 연산일 확률이 높습니다. | `lang/correctness/eqeq.yaml` |
| `formatted-sql-string` | `ERROR` | SQL 쿼리 내에서 Formatted String(서식 문자열)이 발견되었습니다. SQL 인젝션 요인을 막기 위해 PreparedStatement 스타일을 적용하세요. | `lang/security/audit/formatted-sql-string.yaml` |
| `gcm-detection` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `lang/security/audit/crypto/gcm-detection.yaml` |
| `gcm-nonce-reuse` | `ERROR` | GCM 모드 암호화 시 IV(Nonce) 값이 고정으로 재사용되고 있습니다. 암호화 보완성이 즉시 상실되므로 매번 랜덤하고 중복되지 않는 Nonce를 생성하여 주입하십시오. | `lang/security/audit/crypto/gcm-nonce-reuse.yaml` |
| `hardcoded-conditional` | `ERROR` | 조건문(if 등)의 조건식이 항상 true 또는 false로 고정되어 의미 없는 연산을 하거나 로직 버그일 가능성이 높습니다. | `lang/correctness/hardcoded-conditional.yaml` |
| `hibernate-sqli` | `WARNING` | 잠재적 SQL 인젝션 취약점이 감지되었습니다. Parameterized Query나 ORM 모델을 준행하세요. | `lang/security/audit/sqli/hibernate-sqli.yaml` |
| `http-response-splitting` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `lang/security/audit/http-response-splitting.yaml` |
| `httpservlet-path-traversal` | `ERROR` | 외부 입력값으로 직접 파일 시스템 경로를 구성해 처리. Relative path 제어 유출을 막기 위해 입력값에 대한 검증을 수행하세요. | `lang/security/httpservlet-path-traversal.yaml` |
| `insecure-hostname-verifier` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `lang/security/audit/crypto/ssl/insecure-hostname-verifier.yaml` |
| `insecure-jms-deserialization` | `WARNING` | 안전하지 않은 역직렬화 가동이 포착되었습니다. RCE 공격 차단을 위해 직렬화 파서를 격수하십시오. | `lang/security/insecure-jms-deserialization.yaml` |
| `insecure-smtp-connection` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `lang/security/audit/insecure-smtp-connection.yaml` |
| `jackson-unsafe-deserialization` | `WARNING` | 안전하지 않은 역직렬화 가동이 포착되었습니다. RCE 공격 차단을 위해 직렬화 파서를 격수하십시오. | `lang/security/jackson-unsafe-deserialization.yaml` |
| `java-pattern-from-string-parameter` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `lang/security/java-pattern-from-string-parameter.yaml` |
| `java-reverse-shell` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `lang/security/audit/java-reverse-shell.yaml` |
| `jdbc-sqli` | `WARNING` | 잠재적 SQL 인젝션 취약점이 감지되었습니다. Parameterized Query나 ORM 모델을 준행하세요. | `lang/security/audit/sqli/jdbc-sqli.yaml` |
| `jdo-sqli` | `WARNING` | 잠재적 SQL 인젝션 취약점이 감지되었습니다. Parameterized Query나 ORM 모델을 준행하세요. | `lang/security/audit/sqli/jdo-sqli.yaml` |
| `jpa-sqli` | `WARNING` | 잠재적 SQL 인젝션 취약점이 감지되었습니다. Parameterized Query나 ORM 모델을 준행하세요. | `lang/security/audit/sqli/jpa-sqli.yaml` |
| `ldap-entry-poisoning` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `lang/security/audit/ldap-entry-poisoning.yaml` |
| `ldap-injection` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `lang/security/audit/ldap-injection.yaml` |
| `md5-used-as-password` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `lang/security/audit/md5-used-as-password.yaml` |
| `no-static-initialization-vector` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `lang/security/audit/crypto/no-static-initialization-vector.yaml` |
| `no-string-eqeq` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `lang/correctness/no-string-eqeq.yaml` |
| `object-deserialization` | `WARNING` | 안전하지 않은 역직렬화 가동이 포착되었습니다. RCE 공격 차단을 위해 직렬화 파서를 격수하십시오. | `lang/security/audit/object-deserialization.yaml` |
| `ognl-injection` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `lang/security/audit/ognl-injection.yaml` |
| `overly-permissive-file-permission` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `lang/security/audit/overly-permissive-file-permission.yaml` |
| `rsa-no-padding` | `WARNING` | Padding 없는 RSA 암호화 기용 시 특정 공격에 무방비하게 노출될 수 있습니다. | `lang/security/audit/crypto/rsa-no-padding.yaml` |
| `script-engine-injection` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `lang/security/audit/script-engine-injection.yaml` |
| `tainted-cmd-from-http-request` | `ERROR` | HTTP 요청 데이터가 exec 또는 ProcessBuilder 명령 인자로 직주입되고 있습니다. 커맨드 인젝션을 격퇴하기 위해 외부 데이터 사용 시 사전에 구성된 인자형 맵 구조로 매핑하세요. | `lang/security/audit/tainted-cmd-from-http-request.yaml` |
| `tainted-env-from-http-request` | `ERROR` | HTTP 요청이 시스템 커맨드(`exec`)의 환경 변수로 직주입됩니다. 임의 명령 실행 공격을 예방하기 위해 조치하세요. | `lang/security/audit/tainted-env-from-http-request.yaml` |
| `tainted-ldapi-from-http-request` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `lang/security/audit/tainted-ldapi-from-http-request.yaml` |
| `tainted-session-from-http-request` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `lang/security/audit/tainted-session-from-http-request.yaml` |
| `tainted-sql-from-http-request` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `lang/security/audit/sqli/tainted-sql-from-http-request.yaml` |
| `tainted-xpath-from-http-request` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `lang/security/audit/tainted-xpath-from-http-request.yaml` |
| `turbine-sqli` | `WARNING` | 잠재적 SQL 인젝션 취약점이 감지되었습니다. Parameterized Query나 ORM 모델을 준행하세요. | `lang/security/audit/sqli/turbine-sqli.yaml` |
| `unencrypted-socket` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `lang/security/audit/crypto/unencrypted-socket.yaml` |
| `unsafe-reflection` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `lang/security/audit/unsafe-reflection.yaml` |
| `unvalidated-redirect` | `WARNING` | 오픈 리디렉션 피싱 가능성이 존재합니다. 도약 전 검증을 거치세요. | `lang/security/audit/unvalidated-redirect.yaml` |
| `url-rewriting` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `lang/security/audit/url-rewriting.yaml` |
| `use-of-md5-digest-utils` | `WARNING` | 취약한 해시 알고리즘(MD5) 사용이 식별되었습니다. 보안 무결성을 위해 SHA-256 이상을 고르세요. | `lang/security/audit/crypto/use-of-md5-digest-utils.yaml` |
| `use-of-md5` | `WARNING` | 취약한 해시 알고리즘(MD5) 사용이 식별되었습니다. 보안 무결성을 위해 SHA-256 이상을 고르세요. | `lang/security/audit/crypto/use-of-md5.yaml` |
| `use-of-sha1` | `WARNING` | 취약한 해시 알고리즘(SHA-1)이 포획되었습니다. 대체 보상 처리가 요구됩니다. | `lang/security/audit/crypto/use-of-sha1.yaml` |
| `use-of-sha224` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `lang/security/audit/crypto/use-of-sha224.yaml` |
| `use-of-weak-rsa-key` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `lang/security/audit/crypto/weak-rsa.yaml` |
| `use-snakeyaml-constructor` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `lang/security/use-snakeyaml-constructor.yaml` |
| `vertx-sqli` | `WARNING` | 잠재적 SQL 인젝션 취약점이 감지되었습니다. Parameterized Query나 ORM 모델을 준행하세요. | `lang/security/audit/sqli/vertx-sqli.yaml` |
| `weak-random` | `WARNING` | 예측 가능한 난수 생성기(Random) 사용 감지. 보안용으론 SecureRandom을 쓰세요. | `lang/security/audit/crypto/weak-random.yaml` |
| `weak-ssl-context` | `WARNING` | 취약하거나 검증되지 않은 SSL/TLS 컨텍스트가 감지되었습니다. 중간자 공격(MitM)을 조심하십시오. | `lang/security/audit/weak-ssl-context.yaml` |
| `xmlinputfactory-external-entities-enabled` | `ERROR` | XMLInputFactory에 외부 엔티티(External Entities)가 허용되어 있습니다. XML External Entity (XXE) 취약점 발생을 예방하기 위해 이를 비활성화하세요. | `lang/security/xmlinputfactory-external-entities-enabled.yaml` |
| `xmlinputfactory-possible-xxe` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `lang/security/xmlinputfactory-possible-xxe.yaml` |

## MONGODB

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `mongodb-nosqli` | `WARNING` | 잠재적 SQL 인젝션 취약점이 감지되었습니다. Parameterized Query나 ORM 모델을 준행하세요. | `mongodb/security/injection/audit/mongodb-nosqli.yaml` |

## RMI

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `server-dangerous-class-deserialization` | `WARNING` | 안전하지 않은 역직렬화 가동이 포착되었습니다. RCE 공격 차단을 위해 직렬화 파서를 격수하십시오. | `rmi/security/server-dangerous-class-deserialization.yaml` |
| `server-dangerous-object-deserialization` | `ERROR` | RMI 통신 시 임의 객체 수신으로 인한 안전하지 않은 역직렬화 취약점이 가중될 수 있습니다. 허용 클래스 필터링 등을 적용하세요. | `rmi/security/server-dangerous-object-deserialization.yaml` |

## SERVLETS

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `security-constraint-http-method` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `servlets/security/security-constraint-http-method.yaml` |

## SPRING

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `spel-injection` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `spring/security/audit/spel-injection.yaml` |
| `spring-actuator-fully-enabled-yaml` | `WARNING` | Spring Boot Actuator 엔드포인트가 과도하게 활성화되어 정보 누출 우려가 있습니다. | `spring/security/audit/spring-actuator-fully-enabled-yaml.yaml` |
| `spring-actuator-fully-enabled` | `ERROR` | Spring Boot Actuator의 모든 엔드포인트가 완전 개방되어 민감 정보가 노출될 수 있습니다. 필요한 엔티티만 인가하여 사용하세요. | `spring/security/audit/spring-actuator-fully-enabled.yaml` |
| `spring-csrf-disabled` | `WARNING` | Spring Security에서 CSRF 보안이 해제되었습니다. | `spring/security/audit/spring-csrf-disabled.yaml` |
| `spring-jsp-eval` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `spring/security/audit/spring-jsp-eval.yaml` |
| `spring-sqli` | `WARNING` | 잠재적 SQL 인젝션 취약점이 감지되었습니다. Parameterized Query나 ORM 모델을 준행하세요. | `spring/security/audit/spring-sqli.yaml` |
| `spring-unvalidated-redirect` | `WARNING` | 오픈 리디렉션 피싱 가능성이 존재합니다. 도약 전 검증을 거치세요. | `spring/security/audit/spring-unvalidated-redirect.yaml` |
| `tainted-file-path` | `ERROR` | 사용자 입력이 직접 파일 제어 경로 상수로 사용됩니다. Path Traversal 등 디렉토리 도약 시도를 검증하고 소거하세요. | `spring/security/injection/tainted-file-path.yaml` |
| `tainted-html-string` | `ERROR` | 동적 HTML 주입 연산 시 외부 오염 유입 데이터가 전달되었습니다. XSS 보호막 무력화를 예방하기 위해 사전 이스케이프해야 합니다. | `spring/security/injection/tainted-html-string.yaml` |
| `tainted-url-host` | `ERROR` | URL 동적 문자열 조립 시 외부 오염 테두리 호스트 값이 주입됩니다. Open Redirect나 SSRF 위험이 있으니 주소를 정적 고정하거나 검증하세요. | `spring/security/injection/tainted-url-host.yaml` |
| `unrestricted-request-mapping` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `spring/security/unrestricted-request-mapping.yaml` |
