# Java Semgrep Rules Summary

`java` 디렉토리 하위의 규칙 목록입니다. (테스트 파일 제외)

## ANDROID

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `exported="false"` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/exported_activity.yaml` |
| `manifest-usesCleartextTraffic-true` | `INFO` | 평문 트래픽(Cleartext) 전송 옵션이 활성화되었습니다. 스니핑 격퇴를 위해 HTTPS 강제를 요합니다. | `best-practice/manifest-security-features.yaml` |
| `nsc-allows-plaintext-traffic` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/network-security-config.yml` |

## AWS-LAMBDA

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `tainted-sql-string` | `ERROR` | AWS Lambda 핸들러 등의 외부 사용자 입력이 직접 SQL 문자열 조립에 사용되었습니다. Parameterized Query를 사용하여 S... | `security/tainted-sql-string.yaml` |
| `tainted-sqli` | `WARNING` | 잠재적 SQL 인젝션 취약점이 감지되었습니다. Parameterized Query나 ORM 모델을 준행하세요. | `security/tainted-sqli.yaml` |

## JAVA-JWT

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `java-jwt-decode-without-verify` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/jwt-decode-without-verify.yaml` |
| `java-jwt-hardcoded-secret` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/jwt-hardcode.yaml` |
| `java-jwt-none-alg` | `ERROR` | JWT 토큰 서명 및 디코드 검증 누락 여부 점검. | `security/jwt-none-alg.yaml` |

## JAX-RS

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `insecure-resteasy-deserialization` | `WARNING` | 안전하지 않은 역직렬화 가동이 포착되었습니다. RCE 공격 차단을 위해 직렬화 파서를 격수하십시오. | `security/insecure-resteasy.yaml` |
| `jax-rs-path-traversal` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/jax-rs-path-traversal.yaml` |

## JBOSS

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `find-sql-string-concatenation` | `ERROR` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/session_sqli.yaml` |
| `seam-log-injection` | `ERROR` | Seam Logging API에 외부 데이터가 그대로 주입되었습니다. 표현식 언어(EL)를 통해 로깅 시스템이 공격받을 수 있으므로 주입 전 엄... | `security/seam-log-injection.yaml` |

## JJWT

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `jjwt-none-alg` | `ERROR` | JWT 토큰 서명 및 디코드 검증 누락 여부 점검. | `security/jwt-none-alg.yaml` |

## LANG

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `14.4.8` | `WARNING` | CORS 정책이 와일드카드(*) 등으로 과도하게 허용되어 브라우저 데이터 유출 우려가 있습니다. | `security/audit/permissive-cors.yaml` |
| `3.4.1` | `WARNING` | 쿠키에 보안 속성(Secure/HttpOnly)이 누락되어 세션 탈취(XSS/MitM)에 노출될 수 있습니다. | `security/audit/cookie-missing-secure-flag.yaml` |
| `3.4.2` | `WARNING` | 쿠키에 보안 속성(Secure/HttpOnly)이 누락되어 세션 탈취(XSS/MitM)에 노출될 수 있습니다. | `security/audit/cookie-missing-httponly.yaml` |
| `5.1.5` | `WARNING` | 오픈 리디렉션 피싱 가능성이 존재합니다. 도약 전 검증을 거치세요. | `security/audit/unvalidated-redirect.yaml` |
| `5.3.5` | `ERROR` | SQL 쿼리 내에서 Formatted String(서식 문자열)이 발견되었습니다. SQL 인젝션 요인을 막기 위해 PreparedStatemen... | `security/audit/formatted-sql-string.yaml` |
| `5.3.5` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/jdbc-sql-formatted-string.yaml` |
| `5.3.5` | `WARNING` | 잠재적 SQL 인젝션 취약점이 감지되었습니다. Parameterized Query나 ORM 모델을 준행하세요. | `security/audit/sqli/hibernate-sqli.yaml` |
| `5.3.7` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/ldap-entry-poisoning.yaml` |
| `5.3.7` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/ldap-injection.yaml` |
| `5.5.2` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/xmlinputfactory-possible-xxe.yaml` |
| `5.5.2` | `ERROR` | XMLInputFactory에 외부 엔티티(External Entities)가 허용되어 있습니다. XML External Entity (XXE)... | `security/xmlinputfactory-external-entities-enabled.yaml` |
| `5.5.2` | `ERROR` | DocumentBuilderFactory에서 일반 외부 엔티티 호출이 허용되어 XXE 공격에 취약합니다. 가용 가능한 setFeature로 해당... | `security/audit/xxe/documentbuilderfactory-external-general-entities-true.yaml` |
| `5.5.2` | `ERROR` | TransformerFactory에서 DTD 문서 선언 금지 설정이 누락되어 XXE 위험에 노출됩니다. 안전한 XML 가공을 위해 ACCESS_... | `security/audit/xxe/transformerfactory-dtds-not-disabled.yaml` |
| `5.5.2` | `ERROR` | DocumentBuilderFactory 초기화 시 DISALLOW_DOCTYPE_DECL 선언이 누락되었습니다. XXE 및 DTD 부하 공격을... | `security/audit/xxe/documentbuilderfactory-disallow-doctype-decl-missing.yaml` |
| `5.5.2` | `ERROR` | SAXParserFactory 초기화 시 disallow-doctype-decl 선언 설정이 누락되었습니다. XXE 공격 창구를 원천 차단하기 ... | `security/audit/xxe/saxparserfactory-disallow-doctype-decl-missing.yaml` |
| `5.5.2` | `ERROR` | DocumentBuilderFactory에서 disallow-doctype-decl 속성이 false로 설정되어 있습니다. XML 파싱 공격(X... | `security/audit/xxe/documentbuilderfactory-disallow-doctype-decl-false.yaml` |
| `5.5.2` | `ERROR` | DocumentBuilderFactory에서 파라미터형 외부 엔티티 전개 허용이 감지되었습니다. XXE 정보 탈취 피해를 막기 위해 해당 파라미... | `security/audit/xxe/documentbuilderfactory-external-parameter-entities-true.yaml` |
| `5.5.3` | `WARNING` | 안전하지 않은 역직렬화 가동이 포착되었습니다. RCE 공격 차단을 위해 직렬화 파서를 격수하십시오. | `security/insecure-jms-deserialization.yaml` |
| `6.2.2` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/crypto/ssl/avoid-implementing-custom-digests.yaml` |
| `6.2.5` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/blowfish-insufficient-key-size.yaml` |
| `6.2.5` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/crypto/unencrypted-socket.yaml` |
| `6.2.5` | `WARNING` | 취약한 해시 알고리즘(SHA-1)이 포획되었습니다. 대체 보상 처리가 요구됩니다. | `security/audit/crypto/use-of-sha1.yaml` |
| `6.2.5` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/crypto/no-static-initialization-vector.yaml` |
| `6.2.5` | `WARNING` | Padding 없는 RSA 암호화 기용 시 특정 공격에 무방비하게 노출될 수 있습니다. | `security/audit/crypto/rsa-no-padding.yaml` |
| `6.2.5` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/crypto/des-is-deprecated.yaml` |
| `6.2.5` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/crypto/use-of-sha224.yaml` |
| `6.2.5` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/crypto/no-null-cipher.yaml` |
| `9.1.3` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/crypto/ssl/defaulthttpclient-is-deprecated.yaml` |
| `9.2.1` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/crypto/ssl/insecure-hostname-verifier.yaml` |
| `9.2.1` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/crypto/ssl/insecure-trust-manager.yaml` |
| `anonymous-ldap-bind` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/anonymous-ldap-bind.yaml` |
| `assignment-comparison` | `ERROR` | 조건식 내부에서 대입 연산자(=)가 사용되고 있습니다. 의도치 않게 할당이 일어나 비교가 고장날 우려가 있습니다. | `correctness/assignment-comparison.yaml` |
| `autoescape-disabled` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/xss/jsf/autoescape-disabled.yaml` |
| `bad-hexa-conversion` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/bad-hexa-conversion.yaml` |
| `cbc-padding-oracle` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/cbc-padding-oracle.yaml` |
| `command-injection-formatted-runtime-call` | `ERROR` | Runtime.exec에 동적 조립 문자열(String.format 등)을 인자로 전달하여 커맨드 인젝션 위험이 있습니다. 안정성을 위해 인자 ... | `security/audit/command-injection-formatted-runtime-call.yaml` |
| `command-injection-process-builder` | `ERROR` | ProcessBuilder를 이용한 명령어 가동 시 가변 포매터 및 동적 조립 문자열이 사용되었습니다. 리스트형 인자 전달 스타일로 변경하세요. | `security/audit/command-injection-process-builder.yaml` |
| `crlf-injection-logs` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/crlf-injection-logs.yaml` |
| `dangerous-groovy-shell` | `WARNING` | Groovy Shell 직접 구동 파사드에 위험 요소 존재할 수 있습니다. | `security/audit/dangerous-groovy-shell.yaml` |
| `desede-is-deprecated` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/crypto/desede-is-deprecated.yaml` |
| `do-privileged-use` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/do-privileged-use.yaml` |
| `ecb-cipher` | `WARNING` | 취약한 블록 암호화 운영 모드(ECB) 사용 감지. 패턴 노출 방지를 위해 CBC/GCM 모드로 전향하세요. | `security/audit/crypto/ecb-cipher.yaml` |
| `el-injection` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/el-injection.yaml` |
| `eqeq` | `ERROR` | $X == $X 또는 $X != $X 와 같이 본인 자신을 직접 비교하고 있습니다. 로직 실수이거나 무의미한 연산일 확률이 높습니다. | `correctness/eqeq.yaml` |
| `gcm-detection` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/crypto/gcm-detection.yaml` |
| `gcm-nonce-reuse` | `ERROR` | GCM 모드 암호화 시 IV(Nonce) 값이 고정으로 재사용되고 있습니다. 암호화 보완성이 즉시 상실되므로 매번 랜덤하고 중복되지 않는 Non... | `security/audit/crypto/gcm-nonce-reuse.yaml` |
| `hardcoded-conditional` | `ERROR` | 조건문(if 등)의 조건식이 항상 true 또는 false로 고정되어 의미 없는 연산을 하거나 로직 버그일 가능성이 높습니다. | `correctness/hardcoded-conditional.yaml` |
| `http-response-splitting` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/http-response-splitting.yaml` |
| `httpservlet-path-traversal` | `ERROR` | 외부 입력값으로 직접 파일 시스템 경로를 구성해 처리. Relative path 제어 유출을 막기 위해 입력값에 대한 검증을 수행하세요. | `security/httpservlet-path-traversal.yaml` |
| `insecure-smtp-connection` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/insecure-smtp-connection.yaml` |
| `jackson-unsafe-deserialization` | `WARNING` | 안전하지 않은 역직렬화 가동이 포착되었습니다. RCE 공격 차단을 위해 직렬화 파서를 격수하십시오. | `security/jackson-unsafe-deserialization.yaml` |
| `java-pattern-from-string-parameter` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/java-pattern-from-string-parameter.yaml` |
| `java-reverse-shell` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/java-reverse-shell.yaml` |
| `jdbc-sqli` | `WARNING` | 잠재적 SQL 인젝션 취약점이 감지되었습니다. Parameterized Query나 ORM 모델을 준행하세요. | `security/audit/sqli/jdbc-sqli.yaml` |
| `jdo-sqli` | `WARNING` | 잠재적 SQL 인젝션 취약점이 감지되었습니다. Parameterized Query나 ORM 모델을 준행하세요. | `security/audit/sqli/jdo-sqli.yaml` |
| `jpa-sqli` | `WARNING` | 잠재적 SQL 인젝션 취약점이 감지되었습니다. Parameterized Query나 ORM 모델을 준행하세요. | `security/audit/sqli/jpa-sqli.yaml` |
| `md5-used-as-password` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/md5-used-as-password.yaml` |
| `no-direct-response-writer` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/xss/no-direct-response-writer.yaml` |
| `no-scriptlets` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/xss/jsp/no-scriptlets.yaml` |
| `no-string-eqeq` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `correctness/no-string-eqeq.yaml` |
| `object-deserialization` | `WARNING` | 안전하지 않은 역직렬화 가동이 포착되었습니다. RCE 공격 차단을 위해 직렬화 파서를 격수하십시오. | `security/audit/object-deserialization.yaml` |
| `ognl-injection` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/ognl-injection.yaml` |
| `overly-permissive-file-permission` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/overly-permissive-file-permission.yaml` |
| `script-engine-injection` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/script-engine-injection.yaml` |
| `servletresponse-writer-xss` | `ERROR` | HttpServletResponse writer에 사용자 입력이 그대로 출력돼 XSS가 우려됩니다. 출력 전 HTML 인코딩을 적용하거나 보안 ... | `security/servletresponse-writer-xss.yaml` |
| `tainted-cmd-from-http-request` | `ERROR` | HTTP 요청 데이터가 exec 또는 ProcessBuilder 명령 인자로 직주입되고 있습니다. 커맨드 인젝션을 격퇴하기 위해 외부 데이터 사... | `security/audit/tainted-cmd-from-http-request.yaml` |
| `tainted-env-from-http-request` | `ERROR` | HTTP 요청이 시스템 커맨드(`exec`)의 환경 변수로 직주입됩니다. 임의 명령 실행 공격을 예방하기 위해 조치하세요. | `security/audit/tainted-env-from-http-request.yaml` |
| `tainted-ldapi-from-http-request` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/tainted-ldapi-from-http-request.yaml` |
| `tainted-session-from-http-request` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/tainted-session-from-http-request.yaml` |
| `tainted-sql-from-http-request` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/sqli/tainted-sql-from-http-request.yaml` |
| `tainted-xpath-from-http-request` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/tainted-xpath-from-http-request.yaml` |
| `turbine-sqli` | `WARNING` | 잠재적 SQL 인젝션 취약점이 감지되었습니다. Parameterized Query나 ORM 모델을 준행하세요. | `security/audit/sqli/turbine-sqli.yaml` |
| `unsafe-reflection` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/unsafe-reflection.yaml` |
| `url-rewriting` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/url-rewriting.yaml` |
| `use-escapexml` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/xss/jsp/use-escapexml.yaml` |
| `use-jstl-escaping` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/xss/jsp/use-jstl-escaping.yaml` |
| `use-of-aes-ecb` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/crypto/use-of-aes-ecb.yaml` |
| `use-of-blowfish` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/crypto/use-of-blowfish.yaml` |
| `use-of-default-aes` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/crypto/use-of-default-aes.yaml` |
| `use-of-md5` | `WARNING` | 취약한 해시 알고리즘(MD5) 사용이 식별되었습니다. 보안 무결성을 위해 SHA-256 이상을 고르세요. | `security/audit/crypto/use-of-md5.yaml` |
| `use-of-md5-digest-utils` | `WARNING` | 취약한 해시 알고리즘(MD5) 사용이 식별되었습니다. 보안 무결성을 위해 SHA-256 이상을 고르세요. | `security/audit/crypto/use-of-md5-digest-utils.yaml` |
| `use-of-rc2` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/crypto/use-of-rc2.yaml` |
| `use-of-rc4` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/crypto/use-of-rc4.yaml` |
| `use-of-weak-rsa-key` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/crypto/weak-rsa.yaml` |
| `use-snakeyaml-constructor` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/use-snakeyaml-constructor.yaml` |
| `vertx-sqli` | `WARNING` | 잠재적 SQL 인젝션 취약점이 감지되었습니다. Parameterized Query나 ORM 모델을 준행하세요. | `security/audit/sqli/vertx-sqli.yaml` |
| `weak-random` | `WARNING` | 예측 가능한 난수 생성기(Random) 사용 감지. 보안용으론 SecureRandom을 쓰세요. | `security/audit/crypto/weak-random.yaml` |
| `weak-ssl-context` | `WARNING` | 취약하거나 검증되지 않은 SSL/TLS 컨텍스트가 감지되었습니다. 중간자 공격(MitM)을 조심하십시오. | `security/audit/weak-ssl-context.yaml` |
| `xml-decoder` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/xml-decoder.yaml` |
| `xssrequestwrapper-is-insecure` | `WARNING` | 크로스 사이트 스크립팅(XSS) 주입 취약점 우려을 점검하세요. | `security/audit/xssrequestwrapper-is-insecure.yaml` |

## MONGODB

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `5.3.4` | `WARNING` | 잠재적 SQL 인젝션 취약점이 감지되었습니다. Parameterized Query나 ORM 모델을 준행하세요. | `security/injection/audit/mongodb-nosqli.yaml` |

## RMI

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `server-dangerous-class-deserialization` | `WARNING` | 안전하지 않은 역직렬화 가동이 포착되었습니다. RCE 공격 차단을 위해 직렬화 파서를 격수하십시오. | `security/server-dangerous-class-deserialization.yaml` |
| `server-dangerous-object-deserialization` | `ERROR` | RMI 통신 시 임의 객체 수신으로 인한 안전하지 않은 역직렬화 취약점이 가중될 수 있습니다. 허용 클래스 필터링 등을 적용하세요. | `security/server-dangerous-object-deserialization.yaml` |

## SERVLETS

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `cookie-issecure-false` | `WARNING` | 쿠키에 보안 속성(Secure/HttpOnly)이 누락되어 세션 탈취(XSS/MitM)에 노출될 수 있습니다. | `security/cookie-issecure-false.yaml` |
| `cookie-setSecure` | `WARNING` | 쿠키에 보안 속성(Secure/HttpOnly)이 누락되어 세션 탈취(XSS/MitM)에 노출될 수 있습니다. | `security/cookie-setSecure.yaml` |
| `security-constraint-http-method` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/security-constraint-http-method.yaml` |

## SPRING

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `4.2.2` | `WARNING` | Spring Security에서 CSRF 보안이 해제되었습니다. | `security/audit/spring-csrf-disabled.yaml` |
| `spel-injection` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/spel-injection.yaml` |
| `spring-actuator-dangerous-endpoints-enabled` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/spring-actuator-non-health-enabled.yaml` |
| `spring-actuator-dangerous-endpoints-enabled-yaml` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/spring-actuator-non-health-enabled-yaml.yaml` |
| `spring-actuator-fully-enabled` | `ERROR` | Spring Boot Actuator의 모든 엔드포인트가 완전 개방되어 민감 정보가 노출될 수 있습니다. 필요한 엔티티만 인가하여 사용하세요. | `security/audit/spring-actuator-fully-enabled.yaml` |
| `spring-actuator-fully-enabled-yaml` | `WARNING` | Spring Boot Actuator 엔드포인트가 과도하게 활성화되어 정보 누출 우려가 있습니다. | `security/audit/spring-actuator-fully-enabled-yaml.yaml` |
| `spring-jsp-eval` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/spring-jsp-eval.yaml` |
| `spring-sqli` | `WARNING` | 잠재적 SQL 인젝션 취약점이 감지되었습니다. Parameterized Query나 ORM 모델을 준행하세요. | `security/audit/spring-sqli.yaml` |
| `spring-unvalidated-redirect` | `WARNING` | 오픈 리디렉션 피싱 가능성이 존재합니다. 도약 전 검증을 거치세요. | `security/audit/spring-unvalidated-redirect.yaml` |
| `tainted-file-path` | `ERROR` | 사용자 입력이 직접 파일 제어 경로 상수로 사용됩니다. Path Traversal 등 디렉토리 도약 시도를 검증하고 소거하세요. | `security/injection/tainted-file-path.yaml` |
| `tainted-html-string` | `ERROR` | 동적 HTML 주입 연산 시 외부 오염 유입 데이터가 전달되었습니다. XSS 보호막 무력화를 예방하기 위해 사전 이스케이프해야 합니다. | `security/injection/tainted-html-string.yaml` |
| `tainted-sql-string` | `ERROR` | 외부 유입 오염 데이터가 직접 SQL 문자열 조립에 사용되었습니다. SQL 인젝션을 막기 위해 검증된 파라미터형 바인딩 양식을 도출하세요. | `security/injection/tainted-sql-string.yaml` |
| `tainted-system-command` | `ERROR` | 메소드 동적 입력이 직접 시스템 커맨드 실행 인자로 탑재되었습니다. Command Injection의 주요 창구이므로 인자 구조를 엄격히 분격하... | `security/injection/tainted-system-command.yaml` |
| `tainted-url-host` | `ERROR` | URL 동적 문자열 조립 시 외부 오염 테두리 호스트 값이 주입됩니다. Open Redirect나 SSRF 위험이 있으니 주소를 정적 고정하거나... | `security/injection/tainted-url-host.yaml` |
| `unrestricted-request-mapping` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/unrestricted-request-mapping.yaml` |
