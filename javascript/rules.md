# JavaScript Semgrep Rules Summary

`javascript` 디렉토리 하위의 규칙 목록입니다. (테스트 파일 제외)

## AJV

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `ajv-allerrors-true` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/ajv-allerrors-true.yaml` |

## ANGULAR

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `detect-angular-element-methods` | `INFO` | Angular 프론트엔드 결함 주사 점검. | `security/detect-angular-element-methods.yaml` |
| `detect-angular-element-taint` | `WARNING` | Angular 프론트엔드 결함 주사 점검. | `security/detect-angular-element-taint.yaml` |
| `detect-angular-open-redirect` | `ERROR` | $window.location.href 연산에 사용자 입력이 그대로 대입되어 오픈 리디렉션 위협이 도사립니다. 도메인 화이트리스트 검출 후 도약... | `security/detect-angular-open-redirect.yaml` |
| `detect-angular-resource-loading` | `WARNING` | Angular 프론트엔드 결함 주사 점검. | `security/detect-angular-resource-loading.yaml` |
| `detect-angular-sce-disabled` | `ERROR` | $sceProvider가 false로 설정되어 엄격한 컨텍스트 이스케이프가 비활성화되었습니다. XSS 공격 방어를 위해 SCE를 활성화해야 합니... | `security/detect-angular-sce-disabled.yaml` |
| `detect-angular-translateprovider-translations-method` | `WARNING` | Angular 프론트엔드 결함 주사 점검. | `security/detect-third-party-angular-translate.yaml` |
| `detect-angular-trust-as-css-method` | `WARNING` | Angular 프론트엔드 결함 주사 점검. | `security/detect-angular-trust-as-css.yaml` |
| `detect-angular-trust-as-html-method` | `WARNING` | Angular 프론트엔드 결함 주사 점검. | `security/detect-angular-trust-as-html-method.yaml` |
| `detect-angular-trust-as-js-method` | `WARNING` | Angular 프론트엔드 결함 주사 점검. | `security/detect-angular-trust-as-js-method.yaml` |
| `detect-angular-trust-as-method` | `WARNING` | Angular 프론트엔드 결함 주사 점검. | `security/detect-angular-trust-as-method.yaml` |
| `detect-angular-trust-as-resourceurl-method` | `WARNING` | Angular 프론트엔드 결함 주사 점검. | `security/detect-angular-trust-as-resourceurl-method.yaml` |
| `detect-angular-trust-as-url-method` | `WARNING` | Angular 프론트엔드 결함 주사 점검. | `security/detect-angular-trust-as-url-method.yaml` |

## APOLLO

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `apollo-axios-ssrf` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/apollo-axios-ssrf.yaml` |

## ARGON2

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `unsafe-argon2-config` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/unsafe-argon2-config.yaml` |

## AUDIT

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `detect-replaceall-sanitization` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `detect-replaceall-sanitization.yaml` |

## AWS-LAMBDA

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `detect-child-process` | `ERROR` | child_process를 통한 하위 프로세스 생성 시 임의 인자가 탑재될 위험이 있습니다. 실행 코더와 인자를 고정 배열 스타일로 전달하세요. | `security/detect-child-process.yaml` |
| `dynamodb-request-object` | `ERROR` | DynamoDB 쿼리 매개변수 집계 시 $EVENT 유입 데이터가 소요됩니다. NoSQL 인젝션을 피하기 위해 입력 데이터를 정적 한정시키세요. | `security/dynamodb-request-object.yaml` |
| `knex-sqli` | `WARNING` | 잠재적 SQL 인젝션 경로에 대한 검토가 필요합니다. | `security/knex-sqli.yaml` |
| `mysql-sqli` | `WARNING` | 잠재적 SQL 인젝션 경로에 대한 검토가 필요합니다. | `security/mysql-sqli.yaml` |
| `pg-sqli` | `WARNING` | 잠재적 SQL 인젝션 경로에 대한 검토가 필요합니다. | `security/pg-sqli.yaml` |
| `sequelize-sqli` | `WARNING` | 잠재적 SQL 인젝션 경로에 대한 검토가 필요합니다. | `security/sequelize-sqli.yaml` |
| `tainted-eval` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/tainted-eval.yaml` |
| `tainted-html-response` | `WARNING` | HTML 템플릿 가속 피싱 대응. | `security/tainted-html-response.yaml` |
| `tainted-html-string` | `WARNING` | HTML 템플릿 가속 피싱 대응. | `security/tainted-html-string.yaml` |
| `tainted-sql-string` | `ERROR` | Lambda 가동 연산 스택에 유저 기반 SQL 문자열 조립이 탐지되었습니다. Parameterized Query를 사용하여 인젝션 요인을 차단... | `security/tainted-sql-string.yaml` |
| `vm-runincontext-injection` | `ERROR` | vm.runInContext() 호출에 외부 입력 데이터가 유입되어 샌드박스 우회 위험이 있습니다. 가변 코드 실행 연산을 중단하세요. | `security/vm-runincontext-injection.yaml` |

## BLUEBIRD

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `tofastproperties-code-execution` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/tofastproperties-code-execution.yaml` |

## BROWSER

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `dom-based-xss` | `ERROR` | URL 쿼리나 해시 데이터가 이스케이프 없이 화면 렌더링에 전사됩니다. DOM 기반 XSS 예방을 위해 주입 전 스크립트 특문을 정적 필터링하세... | `security/dom-based-xss.yaml` |
| `eval-detected` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/eval-detected.yaml` |
| `insecure-document-method` | `ERROR` | document.write 또는 innerHTML 에 외부 오염 데이터가 탑재되어 DOM-XSS 위험이 보입니다. 안전한 DOM 트리 생성 메서... | `security/insecure-document-method.yaml` |
| `insecure-innerhtml` | `ERROR` | $EL.innerHTML에 사용자 제어 데이터가 대입되고 있습니다. XSS 취약점을 유발하는 안티 패턴이므로 textContent 대체 사용 등... | `security/insecure-innerhtml.yaml` |
| `insufficient-postmessage-origin-validation` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/insufficient-postmessage-origin-validation.yaml` |
| `js-open-redirect` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/open-redirect.yaml` |
| `js-open-redirect-from-function` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/open-redirect-from-function.yaml` |
| `raw-html-concat` | `WARNING` | HTML 템플릿 가속 피싱 대응. | `security/raw-html-concat.yaml` |
| `raw-html-join` | `WARNING` | HTML 템플릿 가속 피싱 대응. | `security/raw-html-join.yaml` |
| `wildcard-postmessage-configuration` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/wildcard-postmessage-configuration.yaml` |

## CHROME-REMOTE-INTERFACE

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `chrome-remote-interface-compilescript-injection` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/chrome-remote-interface-compilescript-injection.yaml` |

## DENO

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `deno-dangerous-run` | `ERROR` | Deno.run() 호출 시 동적 문자열이 사용되었습니다. 명령어나 인자가 조작되어 커맨드 인젝션(Command Injection)이 발생할 수... | `security/audit/deno-dangerous-run.yaml` |

## EXPRESS

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `cors-misconfiguration` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/cors-misconfiguration.yaml` |
| `direct-response-write` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/xss/direct-response-write.yaml` |
| `escape-function-overwrite` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/xss/mustache/escape-function-overwrite.yaml` |
| `express-check-csurf-middleware-usage` | `INFO` | Express 프레임워크 라우팅 및 리디렉션 보안 수사. | `security/audit/express-check-csurf-middleware-usage.yaml` |
| `express-check-directory-listing` | `WARNING` | Express 프레임워크 라우팅 및 리디렉션 보안 수사. | `security/audit/express-check-directory-listing.yaml` |
| `express-cookie-session-default-name` | `WARNING` | Don’t use the default session cookie name Using the default session cookie name ... | `security/audit/express-cookie-settings.yaml` |
| `express-cookie-session-no-domain` | `WARNING` | 쿠키 보안 속성(Secure/HttpOnly) 누출 우려가 있습니다. | `security/audit/express-cookie-settings.yaml` |
| `express-cookie-session-no-expires` | `WARNING` | 쿠키 보안 속성(Secure/HttpOnly) 누출 우려가 있습니다. | `security/audit/express-cookie-settings.yaml` |
| `express-cookie-session-no-httponly` | `WARNING` | 쿠키 보안 속성(Secure/HttpOnly) 누출 우려가 있습니다. | `security/audit/express-cookie-settings.yaml` |
| `express-cookie-session-no-path` | `WARNING` | 쿠키 보안 속성(Secure/HttpOnly) 누출 우려가 있습니다. | `security/audit/express-cookie-settings.yaml` |
| `express-cookie-session-no-secure` | `WARNING` | 쿠키 보안 속성(Secure/HttpOnly) 누출 우려가 있습니다. | `security/audit/express-cookie-settings.yaml` |
| `express-data-exfiltration` | `WARNING` | Express 프레임워크 라우팅 및 리디렉션 보안 수사. | `security/express-data-exfiltration.yaml` |
| `express-detect-notevil-usage` | `WARNING` | Express 프레임워크 라우팅 및 리디렉션 보안 수사. | `security/audit/express-detect-notevil-usage.yaml` |
| `express-expat-xxe` | `ERROR` | expat XML 파서 구동 시 외부 입력에 검증이 부실합니다. XML External Entity (XXE) 취약점 격출을 무마하기 위해 보안... | `security/express-expat-xxe.yaml` |
| `express-insecure-template-usage` | `WARNING` | Express 프레임워크 라우팅 및 리디렉션 보안 수사. | `security/express-insecure-template-usage.yaml` |
| `express-jwt-hardcoded-secret` | `WARNING` | JWT 토큰 서명 및 디코드 검증 누락 여부 점검. | `security/express-jwt-hardcoded-secret.yaml` |
| `express-jwt-not-revoked` | `WARNING` | JWT 토큰 서명 및 디코드 검증 누락 여부 점검. | `security/audit/express-jwt-not-revoked.yaml` |
| `express-libxml-noent` | `ERROR` | libxml 라이브러리 처리 시 noent(Entity expansion) 속성이 true 로 인가되었습니다. XXE 취약점에 전방 노출되므로 ... | `security/audit/express-libxml-noent.yaml` |
| `express-libxml-vm-noent` | `WARNING` | Express 프레임워크 라우팅 및 리디렉션 보안 수사. | `security/audit/express-libxml-vm-noent.yaml` |
| `express-open-redirect` | `WARNING` | Express 프레임워크 라우팅 및 리디렉션 보안 수사. | `security/audit/express-open-redirect.yaml` |
| `express-path-join-resolve-traversal` | `WARNING` | Express 프레임워크 라우팅 및 리디렉션 보안 수사. | `security/audit/express-path-join-resolve-traversal.yaml` |
| `express-phantom-injection` | `ERROR` | phantom API 호출에 사용자 통제 입력 데이터가 결합되었습니다. SSRF 및 인젝션 예방을 위해 사전에 검증된 정적 화이트리스트 맵을 구... | `security/express-phantom-injection.yaml` |
| `express-puppeteer-injection` | `ERROR` | puppeteer 인스턴스 메서드 구동 영역에 외부 동적 데이터가 도출됩니다. SSRF 유도 및 원격 클라이언트 브라우저 구동 조작을 차단하십시... | `security/express-puppeteer-injection.yaml` |
| `express-res-sendfile` | `WARNING` | Express 프레임워크 라우팅 및 리디렉션 보안 수사. | `security/audit/express-res-sendfile.yaml` |
| `express-sandbox-code-injection` | `ERROR` | sandbox 관련 호출에 사용자 입력 데이터가 도달했습니다. 샌드박스 내부에서 임의 코드가 실행될 수 있으므로 동적 조립을 배제하세요. | `security/express-sandbox-injection.yaml` |
| `express-session-hardcoded-secret` | `WARNING` | Express 프레임워크 라우팅 및 리디렉션 보안 수사. | `security/audit/express-session-hardcoded-secret.yaml` |
| `express-ssrf` | `WARNING` | Express 프레임워크 라우팅 및 리디렉션 보안 수사. | `security/audit/express-ssrf.yaml` |
| `express-third-party-object-deserialization` | `WARNING` | Express 프레임워크 라우팅 및 리디렉션 보안 수사. | `security/audit/express-third-party-object-deserialization.yaml` |
| `express-vm-injection` | `ERROR` | Node.js vm 모듈 스크립트 실행 스택 등에 동적 사용자 오염 테두리가 가압되는 피로도를 잡습니다. 샌드박스 우회를 우려해 사전에 분리 차... | `security/express-vm-injection.yaml` |
| `express-vm2-injection` | `WARNING` | Express 프레임워크 라우팅 및 리디렉션 보안 수사. | `security/express-vm2-injection.yaml` |
| `express-wkhtmltoimage-injection` | `ERROR` | wkhtmltoimage 변환 연산 스택에 동적 오염 인자가 포진했습니다. SSRF와 파괴 인자 인젝션 예방을 위해 입력 주소를 교정하세요. | `security/express-wkhtml-injection.yaml` |
| `express-wkhtmltopdf-injection` | `ERROR` | wkhtmltopdf 변환 연산 스택에 동적 오염 인자가 포진했습니다. SSRF와 파괴 인자 인젝션 예방을 위해 입력 주소를 필터링하십시오. | `security/express-wkhtml-injection.yaml` |
| `express-xml2json-xxe` | `ERROR` | XML Parser로 입력되는 데이터 가공 시 외부 사용자 입력이 유출됩니다. XXE(XML External Entity) 공격 취약점을 유발하... | `security/express-xml2json-xxe.yaml` |
| `express-xml2json-xxe-event` | `WARNING` | Express 프레임워크 라우팅 및 리디렉션 보안 수사. | `security/audit/express-xml2json-xxe-event.yaml` |
| `raw-html-format` | `WARNING` | HTML 템플릿 가속 피싱 대응. | `security/injection/raw-html-format.yaml` |
| `remote-property-injection` | `ERROR` | 대괄호 표기법([])에 사용자 입력이 반영되어 객체 속성에 접근하고 있습니다. 프로퍼티 인젝션 및 프로토타입 오염 위험이 있으니 입력값을 사전에... | `security/audit/remote-property-injection.yaml` |
| `require-request` | `ERROR` | require() 인자 위치에 동적 외부 입력이 발견되었습니다. 예상치 못한 스크립트/모듈 로딩 예방을 위해 정적 모듈 경로로 고정하십시오. | `security/require-request.yaml` |
| `res-render-injection` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/res-render-injection.yaml` |
| `tainted-sql-string` | `ERROR` | 동적 SQL 문자열 결합이 탐지되었습니다. SQL Injection 예방을 위해 객체 모델 바인딩 및 Parameterized Query 기법을... | `security/injection/tainted-sql-string.yaml` |
| `template-and-attributes` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/xss/pug/and-attributes.yaml` |
| `template-explicit-unescape` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/xss/pug/explicit-unescape.yaml` |
| `template-explicit-unescape` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/xss/ejs/explicit-unescape.yaml` |
| `template-explicit-unescape` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/xss/mustache/explicit-unescape.yaml` |
| `unknown-value-in-redirect` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/possible-user-input-redirect.yaml` |
| `var-in-href` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/xss/pug/var-in-href.yaml` |
| `var-in-href` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/xss/ejs/var-in-href.yaml` |
| `var-in-script-src` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/xss/ejs/var-in-script-src.yaml` |
| `var-in-script-tag` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/xss/pug/var-in-script-tag.yaml` |
| `var-in-script-tag` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/xss/ejs/var-in-script-tag.yaml` |
| `var-in-script-tag` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/xss/mustache/var-in-script-tag.yaml` |
| `x-frame-options-misconfiguration` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/x-frame-options-misconfiguration.yaml` |

## FBJS

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `insecure-createnodesfrommarkup` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/insecure-createnodesfrommarkup.yaml` |

## GRPC

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `grpc-nodejs-insecure-connection` | `ERROR` | gRPC 연결 생성 시 암호화되지 않은 안전하지 않은 채널(createInsecure())이 사용되었습니다. 중간자 공격(MitM) 등에 무방비... | `security/grpc-nodejs-insecure-connection.yaml` |

## INTERCOM

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `intercom-settings-user-identifier-without-user-hash` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/intercom-settings-user-identifier-without-user-hash.yaml` |

## JOSE

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `hardcoded-jwt-secret` | `WARNING` | JWT 토큰 서명 및 디코드 검증 누락 여부 점검. | `security/jwt-hardcode.yaml` |
| `jose-exposed-data` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/jose-exposed-data.yaml` |
| `jwt-none-alg` | `ERROR` | jose 라이브러리 연산에서 서명 해제용 none 알고리즘 가압이 포착되었습니다. 변조 토큰 패싱을 예방하기 위해 보안 고정 알고리즘을 사용하십... | `security/jwt-none-alg.yaml` |

## JQUERY

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `jquery-insecure-method` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/jquery-insecure-method.yaml` |
| `jquery-insecure-selector` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/jquery-insecure-selector.yaml` |
| `prohibit-jquery-html` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/prohibit-jquery-html.yaml` |

## JSONWEBTOKEN

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `hardcoded-jwt-secret` | `WARNING` | JWT 토큰 서명 및 디코드 검증 누락 여부 점검. | `security/jwt-hardcode.yaml` |
| `jwt-decode-without-verify` | `WARNING` | JWT 토큰 서명 및 디코드 검증 누락 여부 점검. | `security/audit/jwt-decode-without-verify.yaml` |
| `jwt-exposed-data` | `WARNING` | JWT 토큰 서명 및 디코드 검증 누락 여부 점검. | `security/audit/jwt-exposed-data.yaml` |
| `jwt-none-alg` | `ERROR` | jsonwebtoken 서명 알고리즘에 검증 해제용 none 알고리즘 가압이 포착되었습니다. 변조 토큰 인용을 방지하기 위해 확실한 암호화 알고... | `security/jwt-none-alg.yaml` |

## JWT-SIMPLE

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `jwt-simple-noverify` | `ERROR` | jwt-simple 디코딩 수동 호출 시 서명 검증(verify) 단계가 누락되었습니다. 변조 토큰 우회를 막기 위해 반드시 검증 옵션을 활성화... | `security/jwt-simple-noverify.yaml` |

## LANG

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `assigned-undefined` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/assigned-undefined.yaml` |
| `code-string-concat` | `ERROR` | 요청 데이터를 eval() 또는 Function() 실행 인자로 직접 연산 합사합니다. 원격 코드 실행(RCE) 타격을 유발하므로 동적 코드 실... | `security/audit/code-string-concat.yaml` |
| `dangerous-spawn-shell` | `ERROR` | 비 리터럴 문자열을 실행 명령 매개체로 탑재하는 위험 spawn 구조를 감지했습니다. 명령 실행의 안정성을 위해 정적 리스트를 적용하세요. | `security/audit/dangerous-spawn-shell.yaml` |
| `detect-buffer-noassert` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/detect-buffer-noassert.yaml` |
| `detect-child-process` | `ERROR` | child_process 범용 호출 시 유입 인자의 정적 분기가 누락되었습니다. 커맨드 스페이스 조작에 의한 인젝션 방지를 위해 규격 배열을 고... | `security/detect-child-process.yaml` |
| `detect-disable-mustache-escape` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/detect-disable-mustache-escape.yaml` |
| `detect-eval-with-expression` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/detect-eval-with-expression.yaml` |
| `detect-insecure-websocket` | `ERROR` | 보안되지 않은 WebSocket(ws://) 연결이 감지되었습니다. 스니핑 공격을 예방하기 위해 암호화된 wss:// 연결을 사용하세요. | `security/detect-insecure-websocket.yaml` |
| `detect-no-csrf-before-method-override` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/detect-no-csrf-before-method-override.yaml` |
| `detect-non-literal-fs-filename` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/detect-non-literal-fs-filename.yaml` |
| `detect-non-literal-regexp` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/detect-non-literal-regexp.yaml` |
| `detect-non-literal-require` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/detect-non-literal-require.yaml` |
| `detect-pseudoRandomBytes` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/detect-pseudoRandomBytes.yaml` |
| `detect-redos` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/detect-redos.yaml` |
| `eqeq-is-bad` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `correctness/useless-eqeq.yaml` |
| `hardcoded-hmac-key` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/hardcoded-hmac-key.yaml` |
| `html-in-template-string` | `WARNING` | HTML 템플릿 가속 피싱 대응. | `security/html-in-template-string.yaml` |
| `incomplete-sanitization` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/incomplete-sanitization.yaml` |
| `insecure-object-assign` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/insecure-object-assign.yaml` |
| `javascript-alert` | `WARNING` | found alert() call; should this be in production code? | `best-practice/leftover_debugging.yaml` |
| `javascript-confirm` | `WARNING` | 프로덕션 코드에 `confirm()` 호출이 남아있습니다. 배포 전 반드시 제거해 주세요. | `best-practice/leftover_debugging.yaml` |
| `javascript-debugger` | `WARNING` | 프로덕션 코드에 `debugger` 구문이 남아있습니다. 배포 전 반드시 제거해 주세요. | `best-practice/leftover_debugging.yaml` |
| `javascript-prompt` | `WARNING` | 프로덕션 코드에 `prompt()` 호출이 남아있습니다. 배포 전 반드시 제거해 주세요. | `best-practice/leftover_debugging.yaml` |
| `lazy-load-module` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/lazy-load-module.yaml` |
| `md5-used-as-password` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/md5-used-as-password.yaml` |
| `missing-template-string-indicator` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `correctness/missing-template-string-indicator.yaml` |
| `no-replaceall` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `correctness/no-replaceall.yaml` |
| `no-stringify-keys` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `correctness/no-stringify-keys.yaml` |
| `node-knex-sqli` | `WARNING` | 잠재적 SQL 인젝션 경로에 대한 검토가 필요합니다. | `security/audit/sqli/node-knex-sqli.yaml` |
| `node-mssql-sqli` | `WARNING` | 잠재적 SQL 인젝션 경로에 대한 검토가 필요합니다. | `security/audit/sqli/node-mssql-sqli.yaml` |
| `node-mysql-sqli` | `WARNING` | 잠재적 SQL 인젝션 경로에 대한 검토가 필요합니다. | `security/audit/sqli/node-mysql-sqli.yaml` |
| `node-postgres-sqli` | `WARNING` | 잠재적 SQL 인젝션 경로에 대한 검토가 필요합니다. | `security/audit/sqli/node-postgres-sqli.yaml` |
| `path-join-resolve-traversal` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/path-traversal/path-join-resolve-traversal.yaml` |
| `prototype-pollution-assignment` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/prototype-pollution/prototype-pollution-assignment.yaml` |
| `prototype-pollution-loop` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/prototype-pollution/prototype-pollution-loop.yaml` |
| `spawn-git-clone` | `ERROR` | git clone 실행 인자에 사용자 오염 가변 데이터가 유입되었습니다. 인자 인젝션 위험이 있으므로 주소를 고정하거나 정적 세탁하세요. | `security/spawn-git-clone.yaml` |
| `spawn-shell-true` | `ERROR` | spawn 구동 시 {shell: true} 옵션이 사용되었습니다. 인자 하이재킹에 취약하므로 옵션을 철회하고 배열형 인자를 명시하세요. | `security/audit/spawn-shell-true.yaml` |
| `unknown-value-with-script-tag` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/unknown-value-with-script-tag.yaml` |
| `unsafe-dynamic-method` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/unsafe-dynamic-method.yaml` |
| `unsafe-formatstring` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/unsafe-formatstring.yaml` |
| `useless-assignment` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `correctness/useless-assign.yaml` |
| `zlib-async-loop` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/zlib-async-loop.yaml` |

## MONACO-EDITOR

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `monaco-hover-htmlsupport` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/monaco-hover-htmlsupport.yaml` |

## NODE-CRYPTO

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `aead-no-final` | `ERROR` | AEAD 암호 해독 객체의 final() 호출이 빠졌습니다. 인증 태그(Tag) 검증이 스킵되어 위조 데이터 분별이 안되므로 필수 호출하세요. | `security/aead-no-final.yaml` |
| `create-de-cipher-no-iv` | `ERROR` | 지원 중단된 createCipher 기용이 잡혔습니다. 암호화 해독 위험이 크므로 createCipheriv 로 고유 IV를 주입하여 보강하세요... | `security/create-de-cipher-no-iv.yaml` |
| `gcm-no-tag-length` | `ERROR` | GCM 모드 구동 시 createDecipheriv 에 인증 태그(Tag) 탑재 확인 옵션이 누락되었습니다. 데이터 무결성 검증을 위해 반드시 ... | `security/gcm-no-tag-length.yaml` |

## NODE-EXPAT

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `expat-xxe` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/expat-xxe.yaml` |

## PASSPORT-JWT

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `hardcoded-passport-secret` | `WARNING` | 자격증명/보안 기밀 문자열 누락 여부 점검. | `security/passport-hardcode.yaml` |

## PHANTOM

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `phantom-injection` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/phantom-injection.yaml` |

## PLAYWRIGHT

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `playwright-addinitscript-code-injection` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/playwright-addinitscript-code-injection.yaml` |
| `playwright-evaluate-arg-injection` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/playwright-evaluate-arg-injection.yaml` |
| `playwright-evaluate-code-injection` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/playwright-evaluate-code-injection.yaml` |
| `playwright-exposed-chrome-devtools` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/playwright-exposed-chrome-devtools.yaml` |
| `playwright-goto-injection` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/playwright-goto-injection.yaml` |
| `playwright-setcontent-injection` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/playwright-setcontent-injection.yaml` |

## PUPPETEER

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `puppeteer-evaluate-arg-injection` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/puppeteer-evaluate-arg-injection.yaml` |
| `puppeteer-evaluate-code-injection` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/puppeteer-evaluate-code-injection.yaml` |
| `puppeteer-exposed-chrome-devtools` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/puppeteer-exposed-chrome-devtools.yaml` |
| `puppeteer-goto-injection` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/puppeteer-goto-injection.yaml` |
| `puppeteer-setcontent-injection` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/puppeteer-setcontent-injection.yaml` |

## REACT

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `calling-set-state-on-current-state` | `ERROR` | React Hooks에서 현재 상태(state) 값을 그대로 다시 setState에 주입하는 무의미한 연산이 감지되었습니다. 로직 실수를 검토하... | `correctness/hooks/set-state-no-op.yaml` |

## SANDBOX

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `sandbox-code-injection` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/sandbox-code-injection.yaml` |

## SAX

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `sax-xxe` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/sax-xxe.yaml` |

## SEQUELIZE

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `express-sequelize-injection` | `ERROR` | Sequelize 바인딩 스택에 인화성 가변 파라미터가 유입됩니다. SQL Injection 방어를 위해 ORM 규격 바인딩(replacemen... | `security/audit/sequelize-injection-express.yaml` |
| `sequelize-enforce-tls` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/sequelize-enforce-tls.yaml` |
| `sequelize-raw-query` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/sequelize-raw-query.yaml` |
| `sequelize-tls-disabled-cert-validation` | `ERROR` | Sequelize 설정 중 인증서 검증을 우회(rejectUnauthorized: false)하는 상태가 감지되었습니다. 중간자 공격에 도출되므... | `security/audit/sequelize-tls-disabled-cert-validation.yaml` |
| `sequelize-weak-tls-version` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/sequelize-weak-tls-version.yaml` |

## SERIALIZE-JAVASCRIPT

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `unsafe-serialize-javascript` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/unsafe-serialize-javascript.yaml` |

## SHELLJS

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `shelljs-exec-injection` | `ERROR` | shelljs.exec() 호출 연산에 외부 사용자 오염 가변 데이터가 주입되었습니다. RCE(원격코드실행) 위협이 가중되므로 인자 분할 형식으... | `security/shelljs-exec-injection.yaml` |

## THENIFY

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `multiargs-code-execution` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/multiargs-code-execution.yaml` |

## VM2

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `vm2-code-injection` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/vm2-code-injection.yaml` |
| `vm2-context-injection` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/vm2-context-injection.yaml` |

## VUE

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `avoid-v-html` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/xss/templates/avoid-v-html.yaml` |

## WKHTMLTOIMAGE

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `wkhtmltoimage-injection` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/wkhtmltoimage-injection.yaml` |

## WKHTMLTOPDF

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `wkhtmltopdf-injection` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/wkhtmltopdf-injection.yaml` |

## XML2JSON

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `xml2json-xxe` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/audit/xml2json-xxe.yaml` |
