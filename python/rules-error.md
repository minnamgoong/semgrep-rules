# Python Semgrep Rules Summary

`python` 디렉토리 하위의 규칙 목록입니다. (테스트 파일 제외)

## AIRFLOW
\n| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `formatted-string-bashoperator` | `ERROR` | BashOperator 내부 가동 인자에 가변 합사가 포착되었습니다. 외부 주입 우려 노출을 전사 단속하십시오. | `security/audit/formatted-string-bashoperator.yaml` |
\n## AWS-LAMBDA
\n| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `dangerous-asyncio-create-exec` | `ERROR` | create_subprocess_exec 버퍼에 외부 데이터 합치기가 발견되었습니다. 인젝션 예방을 위해 필터링 하세요. | `security/dangerous-asyncio-create-exec.yaml` |
| `dangerous-asyncio-exec` | `ERROR` | subprocess_exec 가동 시 유저 리스트 오염 인자가 흐릅니다. 가변 탑재를 배제하십시오. | `security/dangerous-asyncio-exec.yaml` |
| `dangerous-asyncio-shell` | `ERROR` | asyncio 쉘 연산에 가변 인자가 합사되었습니다. 명령어 주입 우려가 있으니 shlex 세척을 권장합니다. | `security/dangerous-asyncio-shell.yaml` |
| `dangerous-spawn-process` | `ERROR` | os 바이너리 스폰 가동에 event 가변 오염이 흐릅니다. 쉘 명령어 덤프 RCE 차단을 위해 전사 단속하십시오. | `security/dangerous-spawn-process.yaml` |
| `dangerous-subprocess-use` | `ERROR` | subprocess 구동 시 shell=True 탑재 탑재로 보안 결함이 높습니다. 가변 인자 결합을 철회하십시오. | `security/dangerous-subprocess-use.yaml` |
| `dangerous-system-call` | `ERROR` | os 모듈 가동에 event 오염 인자가 유입됩니다. 인젝션 위험이 극에 달하므로 subprocess를 고용하세요. | `security/dangerous-system-call.yaml` |
| `dynamodb-filter-injection` | `ERROR` | DynamoDB 쿼리 필터에 $EVENT 유입 인자가 도주합니다. NoSQL 인젝션 예방을 위해 정적 할당 하십시오. | `security/dynamodb-filter-injection.yaml` |
| `tainted-sql-string` | `ERROR` | Lambda 가동 내 동적 SQL 조립이 탐지되었습니다. Parameterized Query를 사용하여 요인을 차단하십시오. | `security/tainted-sql-string.yaml` |
\n## CLICK
\n| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `use-click-secho` | `ERROR` | click.echo()와 style() 수동 배합 대신 click.secho() 연쇄 고용을 권장합니다. | `best-practice/echo-style.yaml` |
\n## CRYPTOGRAPHY
\n| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `crypto-mode-without-authentication` | `ERROR` | 무결성 검증 없는 암호화 운영 모드가 사용되었습니다. GCM 등 AEAD 모드로 교정하세요. | `security/mode-without-authentication.yaml` |
\n## DJANGO
\n| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `avoid-insecure-deserialization` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 avoid-insecure-deserialization 전사 단속이 요구됩니다. | `security/audit/avoid-insecure-deserialization.yaml` |
| `command-injection-os-system` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 command-injection-os-system 전사 단속이 요구됩니다. | `security/injection/command/command-injection-os-system.yaml` |
| `csv-writer-injection` | `ERROR` | CSV 가동 인자 인젝션 방어를 조율 하십시오. | `security/injection/csv-writer-injection.yaml` |
| `duplicate-path-assignment` | `ERROR` | 서로 다른 경로에 동일한 URL 이름(`$NAME`)이 중복 할당되어 있습니다. 이름 충돌을 방지하기 위해 각 경로에 고유한 이름을 지정해 주세요. | `maintainability/duplicate-path-assignment.yaml` |
| `globals-as-template-context` | `ERROR` | globals() 전역 인출 피칭 국면을 경보합니다. | `security/globals-as-template-context.yaml` |
| `hashids-with-django-secret` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 hashids-with-django-secret 전사 단속이 요구됩니다. | `security/hashids-with-django-secret.yaml` |
| `locals-as-template-context` | `ERROR` | locals() 직접 전사로 내부 탑재 변수가 외부에 탈주 폭주하는 위험 레이어를 점검합니다. | `security/locals-as-template-context.yaml` |
| `nan-injection` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 nan-injection 전사 단속이 요구됩니다. | `security/nan-injection.yaml` |
| `nontext-field-must-set-null-true` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 nontext-field-must-set-null-true 전사 단속이 요구됩니다. | `correctness/nontext-field-must-set-null-true.yaml` |
| `password-empty-string` | `ERROR` | 빈 문자열로 패스워드가 세팅되는 안티 무방비 보안 지점을 진압합니다. | `security/passwords/password-empty-string.yaml` |
| `ssrf-injection-requests` | `ERROR` | 서버 측 요청 위조(SSRF) 누출 피싱 주소 교정. | `security/injection/ssrf/ssrf-injection-requests.yaml` |
| `ssrf-injection-urllib` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 ssrf-injection-urllib 전사 단속이 요구됩니다. | `security/injection/ssrf/ssrf-injection-urllib.yaml` |
| `no-null-string-field` | `ERROR` | unique=True와 blank=True를 함께 선언하는 문자열 필드는 null=True도 반드시 설정해야 합니다. 그렇지 않으면 빈 값으로 여러 레코드를 저장할 때 고유 제약 조건 위반이 발생할 수 있습니다. | `correctness/string-field-null-checks.yaml` |
| `subprocess-injection` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 subprocess-injection 전사 단속이 요구됩니다. | `security/injection/command/subprocess-injection.yaml` |
| `tainted-sql-string` | `ERROR` | 동적 SQL 문자열 결합 유출이 포착되어 Parameterized 쿼리를 독촉합니다. | `security/injection/tainted-sql-string.yaml` |
| `use-count-method` | `ERROR` | .count() 헬퍼 가동으로 쿼리 집계 가속을 도모 하세요. | `performance/upsell-count.yaml` |
| `use-decimalfield-for-money` | `ERROR` | 금액 필드에 부동 소수점 오차를 막기 위해 DecimalField를 사수 하십시오. | `correctness/use-decimalfield-for-money.yaml` |
| `use-django-environ` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 use-django-environ 전사 단속이 요구됩니다. | `best-practice/upsell_django_environ.yaml` |
| `use-earliest-or-latest` | `ERROR` | use-earliest-or-latest 보안 인젝션 및 런타임 버그 전사 예방 점검. | `performance/upsell_earliest_latest.yaml` |
| `use-json-response` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 use-json-response 전사 단속이 요구됩니다. | `best-practice/json_response.yaml` |
| `use-none-for-password-default` | `ERROR` | 비밀번호 기본 데이터에 무효 인자 바인딩을 권장합니다. | `security/passwords/use-none-for-password-default.yaml` |
\n## FLASK
\n| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `csv-writer-injection` | `ERROR` | 내장 csv 모듈에 검증 실종 동동 데이터를 공급 중입니다. 매크로 주입 방어를 위해 특수 서식 이격을 거치세요. | `security/injection/csv-writer-injection.yaml` |
| `dangerous-template-string` | `ERROR` | 가변 스트링 합사를 통한 동적 템플릿 생산이 잡혔습니다. SSTI 예방을 위해 객체 렌더링 양식을 쓰세요. | `security/dangerous-template-string.yaml` |
| `eval-injection` | `ERROR` | eval() 연산 버퍼에 가변 사용자 동적 연산 입력이 관여합니다. 원격 코드 실행(RCE) 타격을 유발하므로 즉각 피하십시오. | `security/injection/user-eval.yaml` |
| `exec-injection` | `ERROR` | exec() 연산 버퍼에 가변 사용자 동적 인가 데이터가 합사됩니다. RCE 극심한 타격이 상존하니 중지하십시오. | `security/injection/user-exec.yaml` |
| `flask-api-method-string-format` | `ERROR` | 컨트롤러 연산에 유저 가변 문자열이 수동 가압됩니다. 인젝션 등 우회 타격 부재를 조심하십시오. | `security/flask-api-method-string-format.yaml` |
| `hashids-with-flask-secret` | `ERROR` | Flask SECRET_KEY를 HashIDs Salt로 오용했습니다. 해시 파싱 중 무력화 위협이 있으니 전용 값을 할당하세요. | `security/hashids-with-flask-secret.yaml` |
| `insecure-deserialization` | `ERROR` | 취약한 역직렬화 라이브러리가 감지되었습니다. RCE 공격 위험을 막기 위해 JSON 등 안전한 형태를 이용하세요. | `security/insecure-deserialization.yaml` |
| `nan-injection` | `ERROR` | 유저 입력이 typecast(float 등) 안으로 직접 유출됩니다. 데이터 연산 우회 조작이 발견될 수 있으니 검사하세요. | `security/injection/nan-injection.yaml` |
| `open-redirect` | `ERROR` | 외부 유입 주소 파라미터가 가공 없이 redirect()로 유출됩니다. 오픈 리디렉션 피싱 방지를 위해 사전 검출 검사하세요. | `security/open-redirect.yaml` |
| `os-system-injection` | `ERROR` | os.system() 가승 연산 버퍼에 동적 조합이 도칩니다. Command Injection 피싱 격량을 타개하기 위해 철회하십시오. | `security/injection/os-system-injection.yaml` |
| `path-traversal-open` | `ERROR` | open() 가동에 유저 노출 경로 데이터가 전사됩니다. 로컬 파일 시스템 탈취를 막고자 사전에 정적 이격 시키세요. | `security/injection/path-traversal-open.yaml` |
| `ssrf-requests` | `ERROR` | HTTP 발송 인자에 오염 입력이 통과 탑재됩니다. SSRF 탈취를 예방하기 위해 조율 주소를 엄밀하게 교정하세요. | `security/injection/ssrf-requests.yaml` |
| `subprocess-injection` | `ERROR` | subprocess 가동 인자에 가변 오염 입력이 포착되었습니다. 커맨드 인젝션 격퇴를 위해 파라미터 분할 배열형을 고수하십시오. | `security/injection/subprocess-injection.yaml` |
| `tainted-sql-string` | `ERROR` | 동적 SQL 문자열 결합이 포착되었습니다. SQL Injection 배후 차단을 위해 Parameterized Query를 사수하세요. | `security/injection/tainted-sql-string.yaml` |
| `use-jsonify` | `ERROR` | 수동 딕셔너리 연계 반환보다 flask.jsonify() 내장 헬퍼를 이용하여 안정성을 유치할 것을 권합합니다. | `best-practice/use-jsonify.yaml` |
\n## JWT
\n| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `jwt-python-exposed-credentials` | `ERROR` | JWT 토큰 페이로드에 기밀 정보가 노출되었습니다. 페이로드는 암호화되지 않으므로 유출 위험이 큽니다. | `security/jwt-exposed-credentials.yaml` |
| `jwt-python-hardcoded-secret` | `ERROR` | 하드코딩된 JWT 비밀키가 발견되었습니다. 보안 누출 예방을 위해 환경 변수나 보안 저장소로 이전하세요. | `security/jwt-hardcode.yaml` |
| `jwt-python-none-alg` | `ERROR` | JWT 서명 검증에서 none 알고리즘 사용이 감지되었습니다. 변조 토큰 우회를 피하기 위해 명시적 암호화를 지정하세요. | `security/jwt-none-alg.yaml` |
| `unverified-jwt-decode` | `ERROR` | JWT 디코딩 시 verify=False 플래그가 발견되었습니다. 무결성 검증을 위해 누출 옵션을 활성화하십시오. | `security/unverified-jwt-decode.yaml` |
\n## LANG
\n| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `arbitrary-sleep` | `ERROR` | 가동 루프 내 sleep 병목 지점을 확인하세요. | `best-practice/sleep.yaml` |
| `avoid-pyyaml-load` | `ERROR` | 취약한 PyYAML load() 가동이 식별되었습니다. RCE 예방을 위해 safe_load()로 대두 전개 처리 하십시오. | `security/deserialization/avoid-pyyaml-load.yaml` |
| `avoid-unsafe-ruamel` | `ERROR` | 동격의 Yaml 파서 인 안전하지 않은 로드 형태 포착. safe 로드 구성을 승인하세요. | `security/deserialization/avoid-unsafe-ruamel.yaml` |
| `dangerous-asyncio-create-exec-audit` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 dangerous-asyncio-create-exec-audit 전사 단속이 요구됩니다. | `security/audit/dangerous-asyncio-create-exec-audit.yaml` |
| `dangerous-asyncio-create-exec-tainted-env-args` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 dangerous-asyncio-create-exec-tainted-env-args 전사 단속이 요구됩니다. | `security/audit/dangerous-asyncio-create-exec-tainted-env-args.yaml` |
| `dangerous-asyncio-exec-audit` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 dangerous-asyncio-exec-audit 전사 단속이 요구됩니다. | `security/audit/dangerous-asyncio-exec-audit.yaml` |
| `dangerous-asyncio-exec-tainted-env-args` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 dangerous-asyncio-exec-tainted-env-args 전사 단속이 요구됩니다. | `security/audit/dangerous-asyncio-exec-tainted-env-args.yaml` |
| `dangerous-asyncio-shell-audit` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 dangerous-asyncio-shell-audit 전사 단속이 요구됩니다. | `security/audit/dangerous-asyncio-shell-audit.yaml` |
| `dangerous-asyncio-shell-tainted-env-args` | `ERROR` | 환경 변수 또는 외부 입력이 비동기 쉘 명령 실행에 직접 사용되고 있습니다. 커맨드 인젝션 취약점을 예방하려면 입력값을 엄격히 검증하거나 쉘을 사용하지 않는 방식으로 전환하세요. | `security/audit/dangerous-asyncio-shell-tainted-env-args.yaml` |
| `dangerous-os-exec` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 dangerous-os-exec 전사 단속이 요구됩니다. | `security/dangerous-os-exec.yaml` |
| `dangerous-os-exec-audit` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 dangerous-os-exec-audit 전사 단속이 요구됩니다. | `security/audit/dangerous-os-exec-audit.yaml` |
| `dangerous-os-exec-tainted-env-args` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 dangerous-os-exec-tainted-env-args 전사 단속이 요구됩니다. | `security/audit/dangerous-os-exec-tainted-env-args.yaml` |
| `dangerous-spawn-process` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 dangerous-spawn-process 전사 단속이 요구됩니다. | `security/dangerous-spawn-process.yaml` |
| `dangerous-spawn-process-audit` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 dangerous-spawn-process-audit 전사 단속이 요구됩니다. | `security/audit/dangerous-spawn-process-audit.yaml` |
| `dangerous-spawn-process-tainted-env-args` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 dangerous-spawn-process-tainted-env-args 전사 단속이 요구됩니다. | `security/audit/dangerous-spawn-process-tainted-env-args.yaml` |
| `dangerous-subprocess-use` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 dangerous-subprocess-use 전사 단속이 요구됩니다. | `security/dangerous-subprocess-use.yaml` |
| `dangerous-subprocess-use-audit` | `ERROR` | 하위 프로세스 생성 드라이버 인젝션 전담 점검. | `security/audit/dangerous-subprocess-use-audit.yaml` |
| `dangerous-subprocess-use-tainted-env-args` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 dangerous-subprocess-use-tainted-env-args 전사 단속이 요구됩니다. | `security/audit/dangerous-subprocess-use-tainted-env-args.yaml` |
| `dangerous-system-call` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 dangerous-system-call 전사 단속이 요구됩니다. | `security/dangerous-system-call.yaml` |
| `dangerous-system-call-audit` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 dangerous-system-call-audit 전사 단속이 요구됩니다. | `security/audit/dangerous-system-call-audit.yaml` |
| `dangerous-system-call-tainted-env-args` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 dangerous-system-call-tainted-env-args 전사 단속이 요구됩니다. | `security/audit/dangerous-system-call-tainted-env-args.yaml` |
| `default-mutable-dict` | `ERROR` | 가변 Dict를 함수 기본 인자로 탑재하여 전역 버퍼 오염을 유도하는 Pitfall을 경보합니다. None 분기가 요망됩니다. | `correctness/common-mistakes/default-mutable-dict.yaml` |
| `default-mutable-list` | `ERROR` | 가변 List 기본 인자 탑재로 인한 버퍼 공유 격량. None 매핑으로 필터 하세요. | `correctness/common-mistakes/default-mutable-list.yaml` |
| `disabled-cert-validation` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 disabled-cert-validation 전사 단속이 요구됩니다. | `security/audit/network/disabled-cert-validation.yaml` |
| `http-not-https-connection` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 http-not-https-connection 전사 단속이 요구됩니다. | `security/audit/network/http-not-https-connection.yaml` |
| `is-not-is-not` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 is-not-is-not 전사 단속이 요구됩니다. | `correctness/common-mistakes/is-not-is-not.yaml` |
| `list-modify-while-iterate` | `ERROR` | for 루프 순회 중 원본 리스트를 가변 삭제/수정하여 오동작을 격발시키는 리스크 누출입니다. | `correctness/list-modify-iterating.yaml` |
| `no-strings-as-booleans` | `ERROR` | 문자열 결합 시 연산 논리 혼선 국면을 저지합니다. | `correctness/useless-comparison.yaml` |
| `open-never-closed` | `ERROR` | 디스크 서술자 닫기 연쇄가 빠졌습니다. | `best-practice/open-never-closed.yaml` |
| `paramiko-exec-command` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 paramiko-exec-command 전사 단속이 요구됩니다. | `security/audit/paramiko/paramiko-exec-command.yaml` |
| `python36-compatibility-ssl` | `ERROR` | 해당 함수 및 문법은 해당 파이썬 버전 연산 지원 사양입니다. | `compatibility/python36.yaml` |
| `python37-compatibility-importlib` | `ERROR` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `compatibility/python37.yaml` |
| `raise-not-base-exception` | `ERROR` | raise-not-base-exception 보안 인젝션 및 런타임 버그 전사 예방 점검. | `correctness/exceptions/exceptions.yaml` |
| `identical-is-comparison` | `ERROR` | 문자열 동등 비교는 is가 아닌 == 연산자를 구동하여 안정성을 가두어야 합니다. | `correctness/common-mistakes/is-comparison-string.yaml` |
| `subprocess-shell-true` | `ERROR` | shell=True 위험 옵션을 우회 처리하십시오. | `security/audit/subprocess-shell-true.yaml` |
| `tempfile-insecure` | `ERROR` | tempfile-insecure 보안 인젝션 및 런타임 버그 전사 예방 점검. | `correctness/tempfile/mktemp.yaml` |
| `tempfile-without-flush` | `ERROR` | tempfile-without-flush 보안 인젝션 및 런타임 버그 전사 예방 점검. | `correctness/tempfile/flush.yaml` |
| `unverified-ssl-context` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 unverified-ssl-context 전사 단속이 요구됩니다. | `security/unverified-ssl-context.yaml` |
| `use-defused-xml` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 use-defused-xml 전사 단속이 요구됩니다. | `security/use-defused-xml.yaml` |
| `use-defused-xml-parse` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 use-defused-xml-parse 전사 단속이 요구됩니다. | `security/use-defused-xml-parse.yaml` |
| `use-defused-xmlrpc` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 use-defused-xmlrpc 전사 단속이 요구됩니다. | `security/use-defused-xmlrpc.yaml` |
| `useless-inner-function` | `ERROR` | 내부 함수가 정의되었으나 사용 연동이 누락되었습니다. 코드 가독성을 위해 말소 대상 점검 하십시오. | `maintainability/useless-innerfunction.yaml` |
| `useless-literal-set` | `ERROR` | set 조립 단에 중복 할당 조각이 보입니다. | `maintainability/useless-literal-set.yaml` |
| `writing-to-file-in-read-mode` | `ERROR` | 읽기 전용으로 가동 중인 서술자에 쓰기(.write)를 가압하는 런타임 에러를 경보합니다. | `correctness/writing-to-file-in-read-mode.yaml` |
| `return-in-init` | `ERROR` | __init__ 내부 yield 전사 금기 양식. | `correctness/return-in-init.yaml` |
\n## PYCRYPTODOME
\n| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `crypto-mode-without-authentication` | `ERROR` | 무결성 검증 없는 암호화 운영 모드가 사용되었습니다. GCM 등 AEAD 모드 사용을 권장합니다. | `security/mode-without-authentication.yaml` |
\n## PYRAMID
\n| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `pyramid-csrf-check-disabled-globally` | `ERROR` | Pyramid 전역 CSRF 방어가 비활성화되었습니다. 뷰 보호를 위해 토크나이저를 구동하십시오. | `security/csrf-check-disabled-globally.yaml` |
| `pyramid-csrf-origin-check-disabled-globally` | `ERROR` | Pyramid Referrer CSRF 검증 전역 누락 감지. Origin 체크 옵션을 활성화하십시오. | `audit/csrf-origin-check-disabled-globally.yaml` |
| `pyramid-direct-use-of-response` | `ERROR` | Response 객체를 렌더링 없이 날것으로 출력합니다. XSS 방어 레이어 우회 우려가 있습니다. | `security/direct-use-of-response.yaml` |
| `pyramid-sqlalchemy-sql-injection` | `ERROR` | distinct/having절 내 원시 SQL 인젝션 가동 현상 감지. bindparams 규격을 준행하세요. | `security/sqlalchemy-sql-injection.yaml` |
\n## REQUESTS
\n| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `disabled-cert-validation` | `ERROR` | requests 가동 시 인증서 검증(verify=False) 탑재는 중간자 노출을 가동합니다. 재활성화 하세요. | `security/disabled-cert-validation.yaml` |
| `no-auth-over-http` | `ERROR` | HTTP 평문 채널을 통한 인증 전송이 포착되었습니다. 스니핑 격퇴를 위해 https:// 도약을 강제 하십시오. | `security/no-auth-over-http.yaml` |
\n## SH
\n| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `string-concat` | `ERROR` | 인젝션 및 논리 에러 예방을 위한 string-concat 전사 단속이 요구됩니다. | `security/string-concat.yaml` |
\n## SQLALCHEMY
\n| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `avoid-sqlalchemy-text` | `ERROR` | sqlalchemy.text() 구동 시 동적 스트링 합사 버그가 우려됩니다. ORM 규격 모델을 준행 하세요. | `security/audit/avoid-sqlalchemy-text.yaml` |
| `delete-where-no-execute` | `ERROR` | SQLAlchemy .delete() 연산 시 .where() 스킵 국면이 감지되었습니다. 전사 데이터 유실에 대비하십시오. | `correctness/delete-where.yaml` |
| `sqlalchemy-execute-raw-query` | `ERROR` | SQLAlchemy 원시 쿼리 동적 결합 감지. 인젝션 투하를 막으려면 Parameterized 선언을 장착 하십시오. | `security/sqlalchemy-execute-raw-query.yaml` |
\n