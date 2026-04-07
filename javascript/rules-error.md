# JavaScript Semgrep Rules Summary

`javascript` 디렉토리 하위의 규칙 목록입니다. (테스트 파일 제외)

## ANGULAR
\n| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `detect-angular-open-redirect` | `ERROR` | $window.location.href 연산에 사용자 입력이 그대로 대입되어 오픈 리디렉션 위협이 도사립니다. 도메인 화이트리스트 검출 후 도약시키세요. | `security/detect-angular-open-redirect.yaml` |
| `detect-angular-sce-disabled` | `ERROR` | $sceProvider가 false로 설정되어 엄격한 컨텍스트 이스케이프가 비활성화되었습니다. XSS 공격 방어를 위해 SCE를 활성화해야 합니다. | `security/detect-angular-sce-disabled.yaml` |
\n## AWS-LAMBDA
\n| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `detect-child-process` | `ERROR` | child_process를 통한 하위 프로세스 생성 시 임의 인자가 탑재될 위험이 있습니다. 실행 코더와 인자를 고정 배열 스타일로 전달하세요. | `security/detect-child-process.yaml` |
| `dynamodb-request-object` | `ERROR` | DynamoDB 쿼리 매개변수 집계 시 $EVENT 유입 데이터가 소요됩니다. NoSQL 인젝션을 피하기 위해 입력 데이터를 정적 한정시키세요. | `security/dynamodb-request-object.yaml` |
| `tainted-sql-string` | `ERROR` | Lambda 가동 연산 스택에 유저 기반 SQL 문자열 조립이 탐지되었습니다. Parameterized Query를 사용하여 인젝션 요인을 차단하십시오. | `security/tainted-sql-string.yaml` |
| `vm-runincontext-injection` | `ERROR` | vm.runInContext() 호출에 외부 입력 데이터가 유입되어 샌드박스 우회 위험이 있습니다. 가변 코드 실행 연산을 중단하세요. | `security/vm-runincontext-injection.yaml` |
\n## BROWSER
\n| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `dom-based-xss` | `ERROR` | URL 쿼리나 해시 데이터가 이스케이프 없이 화면 렌더링에 전사됩니다. DOM 기반 XSS 예방을 위해 주입 전 스크립트 특문을 정적 필터링하세... | `security/dom-based-xss.yaml` |
| `insecure-document-method` | `ERROR` | document.write 또는 innerHTML 에 외부 오염 데이터가 탑재되어 DOM-XSS 위험이 보입니다. 안전한 DOM 트리 생성 메서드로 변경하세요. | `security/insecure-document-method.yaml` |
| `insecure-innerhtml` | `ERROR` | $EL.innerHTML에 사용자 제어 데이터가 대입되고 있습니다. XSS 취약점을 유발하는 안티 패턴이므로 textContent 대체 사용 등을 고려하세요. | `security/insecure-innerhtml.yaml` |
\n## DENO
\n| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `deno-dangerous-run` | `ERROR` | Deno.run() 호출 시 동적 문자열이 사용되었습니다. 명령어나 인자가 조작되어 커맨드 인젝션(Command Injection)이 발생할 수 있으므로 고정 배열 스타일을 적용하세요. | `security/audit/deno-dangerous-run.yaml` |
\n## EXPRESS
\n| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `express-expat-xxe` | `ERROR` | expat XML 파서 구동 시 외부 입력에 검증이 부실합니다. XML External Entity (XXE) 취약점 격출을 무마하기 위해 보안 옵션을 비활성화 처리하십시오. | `security/express-expat-xxe.yaml` |
| `express-libxml-noent` | `ERROR` | libxml 라이브러리 처리 시 noent(Entity expansion) 속성이 true 로 인가되었습니다. XXE 취약점에 전방 노출되므로 이를 비활성화 처리하세요. | `security/audit/express-libxml-noent.yaml` |
| `express-phantom-injection` | `ERROR` | phantom API 호출에 사용자 통제 입력 데이터가 결합되었습니다. SSRF 및 인젝션 예방을 위해 사전에 검증된 정적 화이트리스트 맵을 구비하세요. | `security/express-phantom-injection.yaml` |
| `express-puppeteer-injection` | `ERROR` | puppeteer 인스턴스 메서드 구동 영역에 외부 동적 데이터가 도출됩니다. SSRF 유도 및 원격 클라이언트 브라우저 구동 조작을 차단하십시오. | `security/express-puppeteer-injection.yaml` |
| `express-sandbox-code-injection` | `ERROR` | sandbox 관련 호출에 사용자 입력 데이터가 도달했습니다. 샌드박스 내부에서 임의 코드가 실행될 수 있으므로 동적 조립을 배제하세요. | `security/express-sandbox-injection.yaml` |
| `express-vm-injection` | `ERROR` | Node.js vm 모듈 스크립트 실행 스택 등에 동적 사용자 오염 테두리가 가압되는 피로도를 잡습니다. 샌드박스 우회를 우려해 사전에 분리 차단하세요. | `security/express-vm-injection.yaml` |
| `express-wkhtmltoimage-injection` | `ERROR` | wkhtmltopdf 변환 연산 스택에 동적 오염 인자가 포진했습니다. SSRF와 파괴 인자 인젝션 예방을 위해 입력 주소를 필터링하십시오. | `security/express-wkhtml-injection.yaml` |
| `express-wkhtmltoimage-injection` | `ERROR` | wkhtmltopdf 변환 연산 스택에 동적 오염 인자가 포진했습니다. SSRF와 파괴 인자 인젝션 예방을 위해 입력 주소를 필터링하십시오. | `security/express-wkhtml-injection.yaml` |
| `express-xml2json-xxe` | `ERROR` | XML Parser로 입력되는 데이터 가공 시 외부 사용자 입력이 유출됩니다. XXE(XML External Entity) 공격 취약점을 유발하므로 파서에 DTD 로딩 및 외부 엔티티 호출을 차단하세요. | `security/express-xml2json-xxe.yaml` |
| `remote-property-injection` | `ERROR` | 대괄호 표기법([])에 사용자 입력이 반영되어 객체 속성에 접근하고 있습니다. 프로퍼티 인젝션 및 프로토타입 오염 위험이 있으니 입력값을 사전에 검증하세요. | `security/audit/remote-property-injection.yaml` |
| `require-request` | `ERROR` | require() 인자 위치에 동적 외부 입력이 발견되었습니다. 예상치 못한 스크립트/모듈 로딩 예방을 위해 정적 모듈 경로로 고정하십시오. | `security/require-request.yaml` |
| `tainted-sql-string` | `ERROR` | 동적 SQL 문자열 결합이 탐지되었습니다. SQL Injection 예방을 위해 객체 모델 바인딩 및 Parameterized Query 기법을 사용하세요. | `security/injection/tainted-sql-string.yaml` |
\n## GRPC
\n| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `grpc-nodejs-insecure-connection` | `ERROR` | gRPC 연결 생성 시 암호화되지 않은 안전하지 않은 채널(createInsecure())이 사용되었습니다. 중간자 공격(MitM) 등에 무방비하므로 SSL/TLS 보완책을 적용하십시오. | `security/grpc-nodejs-insecure-connection.yaml` |
\n## JOSE
\n| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `jwt-none-alg` | `ERROR` | jose 라이브러리 연산에서 서명 해제용 none 알고리즘 가압이 포착되었습니다. 변조 토큰 패싱을 예방하기 위해 보안 고정 알고리즘을 사용하십시오. | `security/jwt-none-alg.yaml` |
\n## JSONWEBTOKEN
\n| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `jwt-none-alg` | `ERROR` | jsonwebtoken 서명 알고리즘에 검증 해제용 none 알고리즘 가압이 포착되었습니다. 변조 토큰 인용을 방지하기 위해 확실한 암호화 알고리즘만 허용하도록 고정하세요. | `security/jwt-none-alg.yaml` |
\n## JWT-SIMPLE
\n| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `jwt-simple-noverify` | `ERROR` | jwt-simple 디코딩 수동 호출 시 서명 검증(verify) 단계가 누락되었습니다. 변조 토큰 우회를 막기 위해 반드시 검증 옵션을 활성화하세요. | `security/jwt-simple-noverify.yaml` |
\n## LANG
\n| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `code-string-concat` | `ERROR` | 요청 데이터를 eval() 또는 Function() 실행 인자로 직접 연산 합사합니다. 원격 코드 실행(RCE) 타격을 유발하므로 동적 코드 실행을 금지하십시오. | `security/audit/code-string-concat.yaml` |
| `dangerous-spawn-shell` | `ERROR` | 비 리터럴 문자열을 실행 명령 매개체로 탑재하는 위험 spawn 구조를 감지했습니다. 명령 실행의 안정성을 위해 정적 리스트를 적용하세요. | `security/audit/dangerous-spawn-shell.yaml` |
| `detect-child-process` | `ERROR` | child_process 범용 호출 시 유입 인자의 정적 분기가 누락되었습니다. 커맨드 스페이스 조작에 의한 인젝션 방지를 위해 규격 배열을 고수하세요. | `security/detect-child-process.yaml` |
| `detect-insecure-websocket` | `ERROR` | 보안되지 않은 WebSocket(ws://) 연결이 감지되었습니다. 스니핑 공격을 예방하기 위해 암호화된 wss:// 연결을 사용하세요. | `security/detect-insecure-websocket.yaml` |
| `spawn-git-clone` | `ERROR` | git clone 실행 인자에 사용자 오염 가변 데이터가 유입되었습니다. 인자 인젝션 위험이 있으므로 주소를 고정하거나 정적 세탁하세요. | `security/spawn-git-clone.yaml` |
| `spawn-shell-true` | `ERROR` | spawn 구동 시 {shell: true} 옵션이 사용되었습니다. 인자 하이재킹에 취약하므로 옵션을 철회하고 배열형 인자를 명시하세요. | `security/audit/spawn-shell-true.yaml` |
\n## NODE-CRYPTO
\n| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `aead-no-final` | `ERROR` | AEAD 암호 해독 객체의 final() 호출이 빠졌습니다. 인증 태그(Tag) 검증이 스킵되어 위조 데이터 분별이 안되므로 필수 호출하세요. | `security/aead-no-final.yaml` |
| `create-de-cipher-no-iv` | `ERROR` | 지원 중단된 createCipher 기용이 잡혔습니다. 암호화 해독 위험이 크므로 createCipheriv 로 고유 IV를 주입하여 보강하세요. | `security/create-de-cipher-no-iv.yaml` |
| `gcm-no-tag-length` | `ERROR` | GCM 모드 구동 시 createDecipheriv 에 인증 태그(Tag) 탑재 확인 옵션이 누락되었습니다. 데이터 무결성 검증을 위해 반드시 활성화하세요. | `security/gcm-no-tag-length.yaml` |
\n## REACT
\n| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `calling-set-state-on-current-state` | `ERROR` | React Hooks에서 현재 상태(state) 값을 그대로 다시 setState에 주입하는 무의미한 연산이 감지되었습니다. 로직 실수를 검토하세요. | `correctness/hooks/set-state-no-op.yaml` |
\n## SEQUELIZE
\n| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `express-sequelize-injection` | `ERROR` | Sequelize 바인딩 스택에 인화성 가변 파라미터가 유입됩니다. SQL Injection 방어를 위해 ORM 규격 바인딩(replacements)을 쓰세요. | `security/audit/sequelize-injection-express.yaml` |
| `sequelize-tls-disabled-cert-validation` | `ERROR` | Sequelize 설정 중 인증서 검증을 우회(rejectUnauthorized: false)하는 상태가 감지되었습니다. 중간자 공격에 도출되므로 프로덕션 배포 시 철회하십시오. | `security/audit/sequelize-tls-disabled-cert-validation.yaml` |
\n## SHELLJS
\n| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `shelljs-exec-injection` | `ERROR` | shelljs.exec() 호출 연산에 외부 사용자 오염 가변 데이터가 주입되었습니다. RCE(원격코드실행) 위협이 가중되므로 인자 분할 형식으로 전환하십시오. | `security/shelljs-exec-injection.yaml` |
\n