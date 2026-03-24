# Problem-based-packs Semgrep Rules Summary

`problem-based-packs` 디렉토리 하위의 규칙 목록입니다. (테스트 파일 제외)

## INSECURE-TRANSPORT

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `bypass-tls-verification` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `js-node/bypass-tls-verification.yaml` |
| `bypass-tls-verification` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `go-stdlib/bypass-tls-verification.yaml` |
| `bypass-tls-verification` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `java-spring/bypass-tls-verification.yaml` |
| `bypass-tls-verification` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `java-stdlib/bypass-tls-verification.yaml` |
| `disallow-old-tls-versions` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `go-stdlib/disallow-old-tls-versions.yaml` |
| `disallow-old-tls-versions1` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `js-node/disallow-old-tls-versions1.yaml` |
| `disallow-old-tls-versions1` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `java-stdlib/disallow-old-tls-versions1.yaml` |
| `disallow-old-tls-versions2` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `js-node/disallow-old-tls-versions2.yaml` |
| `disallow-old-tls-versions2` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `java-stdlib/disallow-old-tls-versions2.yaml` |
| `ftp-request` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `js-node/ftp-request.yaml` |
| `ftp-request` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `go-stdlib/ftp-request.yaml` |
| `ftp-request` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `java-stdlib/ftp-request.yaml` |
| `gorequest-http-request` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `go-stdlib/gorequest-http-request.yaml` |
| `grequests-http-request` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `go-stdlib/grequests-http-request.yaml` |
| `http-client-requests` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `ruby-stdlib/http-client-requests.yaml` |
| `http-components-request` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `java-stdlib/http-components-request.yaml` |
| `http-customized-request` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `go-stdlib/http-customized-request.yaml` |
| `http-request` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `js-node/http-request.yaml` |
| `http-request` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `go-stdlib/http-request.yaml` |
| `httpclient-http-request` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `java-stdlib/httpclient-http-request.yaml` |
| `httpget-http-request` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `java-stdlib/httpget-http-request.yaml` |
| `httpurlconnection-http-request` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `java-stdlib/httpurlconnection-http-request.yaml` |
| `net-ftp-request` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `ruby-stdlib/net-ftp-request.yaml` |
| `net-http-request` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `ruby-stdlib/net-http-request.yaml` |
| `net-telnet-request` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `ruby-stdlib/net-telnet-request.yaml` |
| `openuri-request` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `ruby-stdlib/openuri-request.yaml` |
| `rest-http-client-support` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `js-node/rest-http-client-support.yaml` |
| `sling-http-request` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `go-stdlib/sling-http-request.yaml` |
| `socket-request` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `java-stdlib/socket-request.yaml` |
| `spring-ftp-request` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `java-spring/spring-ftp-request.yaml` |
| `spring-http-request` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `java-spring/spring-http-request.yaml` |
| `telnet-request` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `js-node/telnet-request.yaml` |
| `telnet-request` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `go-stdlib/telnet-request.yaml` |
| `telnet-request` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `java-stdlib/telnet-request.yaml` |
| `tls-renegotiation` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `java-stdlib/tls-renegotiation.yaml` |
| `unirest-http-request` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `java-stdlib/unirest-http-request.yaml` |
| `using-http-server` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `js-node/using-http-server.yaml` |
