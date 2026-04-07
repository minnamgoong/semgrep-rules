# Java Semgrep Rules Summary

`java` 디렉토리 하위의 규칙 목록입니다. (테스트 파일 제외)

## AWS-LAMBDA
\n| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `tainted-sql-string` | `ERROR` | AWS Lambda 핸들러 등의 외부 사용자 입력이 직접 SQL 문자열 조립에 사용되었습니다. Parameterized Query를 사용하여 SQL 인젝션을 예방하세요. | `aws-lambda/security/tainted-sql-string.yaml` |
\n## JBOSS
\n| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `seam-log-injection` | `ERROR` | Seam Logging API에 외부 데이터가 그대로 주입되었습니다. 표현식 언어(EL)를 통해 로깅 시스템이 공격받을 수 있으므로 주입 전 엄격한 검증을 통과해야 합니다. | `jboss/security/seam-log-injection.yaml` |
\n## LANG
\n| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `assignment-comparison` | `ERROR` | 조건식 내부에서 대입 연산자(=)가 사용되고 있습니다. 의도치 않게 할당이 일어나 비교가 고장날 우려가 있습니다. | `lang/correctness/assignment-comparison.yaml` |
| `command-injection-formatted-runtime-call` | `ERROR` | Runtime.exec에 동적 조립 문자열(String.format 등)을 인자로 전달하여 커맨드 인젝션 위험이 있습니다. 안정성을 위해 인자 리스트(String[]) 형식으로 전달하세요. | `lang/security/audit/command-injection-formatted-runtime-call.yaml` |
| `command-injection-process-builder` | `ERROR` | ProcessBuilder를 이용한 명령어 가동 시 가변 포매터 및 동적 조립 문자열이 사용되었습니다. 리스트형 인자 전달 스타일로 변경하세요. | `lang/security/audit/command-injection-process-builder.yaml` |
| `eqeq` | `ERROR` | $X == $X 또는 $X != $X 와 같이 본인 자신을 직접 비교하고 있습니다. 로직 실수이거나 무의미한 연산일 확률이 높습니다. | `lang/correctness/eqeq.yaml` |
| `formatted-sql-string` | `ERROR` | SQL 쿼리 내에서 Formatted String(서식 문자열)이 발견되었습니다. SQL 인젝션 요인을 막기 위해 PreparedStatement 스타일을 적용하세요. | `lang/security/audit/formatted-sql-string.yaml` |
| `gcm-nonce-reuse` | `ERROR` | GCM 모드 암호화 시 IV(Nonce) 값이 고정으로 재사용되고 있습니다. 암호화 보완성이 즉시 상실되므로 매번 랜덤하고 중복되지 않는 Nonce를 생성하여 주입하십시오. | `lang/security/audit/crypto/gcm-nonce-reuse.yaml` |
| `hardcoded-conditional` | `ERROR` | 조건문(if 등)의 조건식이 항상 true 또는 false로 고정되어 의미 없는 연산을 하거나 로직 버그일 가능성이 높습니다. | `lang/correctness/hardcoded-conditional.yaml` |
| `httpservlet-path-traversal` | `ERROR` | 외부 입력값으로 직접 파일 시스템 경로를 구성해 처리. Relative path 제어 유출을 막기 위해 입력값에 대한 검증을 수행하세요. | `lang/security/httpservlet-path-traversal.yaml` |
| `tainted-cmd-from-http-request` | `ERROR` | HTTP 요청 데이터가 exec 또는 ProcessBuilder 명령 인자로 직주입되고 있습니다. 커맨드 인젝션을 격퇴하기 위해 외부 데이터 사용 시 사전에 구성된 인자형 맵 구조로 매핑하세요. | `lang/security/audit/tainted-cmd-from-http-request.yaml` |
| `tainted-env-from-http-request` | `ERROR` | HTTP 요청이 시스템 커맨드(`exec`)의 환경 변수로 직주입됩니다. 임의 명령 실행 공격을 예방하기 위해 조치하세요. | `lang/security/audit/tainted-env-from-http-request.yaml` |
| `xmlinputfactory-external-entities-enabled` | `ERROR` | XMLInputFactory에 외부 엔티티(External Entities)가 허용되어 있습니다. XML External Entity (XXE) 취약점 발생을 예방하기 위해 이를 비활성화하세요. | `lang/security/xmlinputfactory-external-entities-enabled.yaml` |
\n## RMI
\n| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `server-dangerous-object-deserialization` | `ERROR` | RMI 통신 시 임의 객체 수신으로 인한 안전하지 않은 역직렬화 취약점이 가중될 수 있습니다. 허용 클래스 필터링 등을 적용하세요. | `rmi/security/server-dangerous-object-deserialization.yaml` |
\n## SPRING
\n| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `spring-actuator-fully-enabled` | `ERROR` | Spring Boot Actuator의 모든 엔드포인트가 완전 개방되어 민감 정보가 노출될 수 있습니다. 필요한 엔티티만 인가하여 사용하세요. | `spring/security/audit/spring-actuator-fully-enabled.yaml` |
| `tainted-file-path` | `ERROR` | 사용자 입력이 직접 파일 제어 경로 상수로 사용됩니다. Path Traversal 등 디렉토리 도약 시도를 검증하고 소거하세요. | `spring/security/injection/tainted-file-path.yaml` |
| `tainted-html-string` | `ERROR` | 동적 HTML 주입 연산 시 외부 오염 유입 데이터가 전달되었습니다. XSS 보호막 무력화를 예방하기 위해 사전 이스케이프해야 합니다. | `spring/security/injection/tainted-html-string.yaml` |
| `tainted-url-host` | `ERROR` | URL 동적 문자열 조립 시 외부 오염 테두리 호스트 값이 주입됩니다. Open Redirect나 SSRF 위험이 있으니 주소를 정적 고정하거나 검증하세요. | `spring/security/injection/tainted-url-host.yaml` |
