# Problem-based-packs Semgrep Rules Summary

`problem-based-packs` 디렉토리 하위의 규칙 목록입니다. (테스트 파일 제외)

## INSECURE-TRANSPORT

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `bypass-tls-verification` | `WARNING` | bypass-tls-verification 잠재적 결함 및 보안 이격율 정비 요망. | `js-node/bypass-tls-verification.yaml` |
| `bypass-tls-verification` | `WARNING` | bypass-tls-verification 잠재적 결함 및 보안 이격율 정비 요망. | `go-stdlib/bypass-tls-verification.yaml` |
| `bypass-tls-verification` | `WARNING` | bypass-tls-verification 잠재적 결함 및 보안 이격율 정비 요망. | `java-spring/bypass-tls-verification.yaml` |
| `bypass-tls-verification` | `WARNING` | bypass-tls-verification 잠재적 결함 및 보안 이격율 정비 요망. | `java-stdlib/bypass-tls-verification.yaml` |
| `disallow-old-tls-versions` | `WARNING` | disallow-old-tls-versions 잠재적 결함 및 보안 이격율 정비 요망. | `go-stdlib/disallow-old-tls-versions.yaml` |
| `disallow-old-tls-versions1` | `WARNING` | disallow-old-tls-versions1 잠재적 결함 및 보안 이격율 정비 요망. | `js-node/disallow-old-tls-versions1.yaml` |
| `disallow-old-tls-versions1` | `WARNING` | disallow-old-tls-versions1 잠재적 결함 및 보안 이격율 정비 요망. | `java-stdlib/disallow-old-tls-versions1.yaml` |
| `disallow-old-tls-versions2` | `WARNING` | disallow-old-tls-versions2 잠재적 결함 및 보안 이격율 정비 요망. | `js-node/disallow-old-tls-versions2.yaml` |
| `disallow-old-tls-versions2` | `WARNING` | disallow-old-tls-versions2 잠재적 결함 및 보안 이격율 정비 요망. | `java-stdlib/disallow-old-tls-versions2.yaml` |
| `ftp-request` | `WARNING` | ftp-request 잠재적 결함 및 보안 이격율 정비 요망. | `js-node/ftp-request.yaml` |
| `ftp-request` | `WARNING` | ftp-request 잠재적 결함 및 보안 이격율 정비 요망. | `go-stdlib/ftp-request.yaml` |
| `ftp-request` | `WARNING` | ftp-request 잠재적 결함 및 보안 이격율 정비 요망. | `java-stdlib/ftp-request.yaml` |
| `gorequest-http-request` | `WARNING` | gorequest-http-request 잠재적 결함 및 보안 이격율 정비 요망. | `go-stdlib/gorequest-http-request.yaml` |
| `grequests-http-request` | `WARNING` | grequests-http-request 잠재적 결함 및 보안 이격율 정비 요망. | `go-stdlib/grequests-http-request.yaml` |
| `http-client-requests` | `WARNING` | http-client-requests 잠재적 결함 및 보안 이격율 정비 요망. | `ruby-stdlib/http-client-requests.yaml` |
| `http-components-request` | `WARNING` | http-components-request 잠재적 결함 및 보안 이격율 정비 요망. | `java-stdlib/http-components-request.yaml` |
| `http-customized-request` | `WARNING` | http-customized-request 잠재적 결함 및 보안 이격율 정비 요망. | `go-stdlib/http-customized-request.yaml` |
| `http-request` | `WARNING` | http-request 잠재적 결함 및 보안 이격율 정비 요망. | `js-node/http-request.yaml` |
| `http-request` | `WARNING` | http-request 잠재적 결함 및 보안 이격율 정비 요망. | `go-stdlib/http-request.yaml` |
| `httpclient-http-request` | `WARNING` | httpclient-http-request 잠재적 결함 및 보안 이격율 정비 요망. | `java-stdlib/httpclient-http-request.yaml` |
| `httpget-http-request` | `WARNING` | httpget-http-request 잠재적 결함 및 보안 이격율 정비 요망. | `java-stdlib/httpget-http-request.yaml` |
| `httpurlconnection-http-request` | `WARNING` | httpurlconnection-http-request 잠재적 결함 및 보안 이격율 정비 요망. | `java-stdlib/httpurlconnection-http-request.yaml` |
| `net-ftp-request` | `WARNING` | net-ftp-request 잠재적 결함 및 보안 이격율 정비 요망. | `ruby-stdlib/net-ftp-request.yaml` |
| `net-http-request` | `WARNING` | net-http-request 잠재적 결함 및 보안 이격율 정비 요망. | `ruby-stdlib/net-http-request.yaml` |
| `net-telnet-request` | `WARNING` | net-telnet-request 잠재적 결함 및 보안 이격율 정비 요망. | `ruby-stdlib/net-telnet-request.yaml` |
| `openuri-request` | `WARNING` | openuri-request 잠재적 결함 및 보안 이격율 정비 요망. | `ruby-stdlib/openuri-request.yaml` |
| `rest-http-client-support` | `WARNING` | rest-http-client-support 잠재적 결함 및 보안 이격율 정비 요망. | `js-node/rest-http-client-support.yaml` |
| `sling-http-request` | `WARNING` | sling-http-request 잠재적 결함 및 보안 이격율 정비 요망. | `go-stdlib/sling-http-request.yaml` |
| `socket-request` | `WARNING` | socket-request 잠재적 결함 및 보안 이격율 정비 요망. | `java-stdlib/socket-request.yaml` |
| `spring-ftp-request` | `WARNING` | spring-ftp-request 잠재적 결함 및 보안 이격율 정비 요망. | `java-spring/spring-ftp-request.yaml` |
| `spring-http-request` | `WARNING` | spring-http-request 잠재적 결함 및 보안 이격율 정비 요망. | `java-spring/spring-http-request.yaml` |
| `telnet-request` | `WARNING` | telnet-request 잠재적 결함 및 보안 이격율 정비 요망. | `js-node/telnet-request.yaml` |
| `telnet-request` | `WARNING` | telnet-request 잠재적 결함 및 보안 이격율 정비 요망. | `go-stdlib/telnet-request.yaml` |
| `telnet-request` | `WARNING` | telnet-request 잠재적 결함 및 보안 이격율 정비 요망. | `java-stdlib/telnet-request.yaml` |
| `tls-renegotiation` | `WARNING` | tls-renegotiation 잠재적 결함 및 보안 이격율 정비 요망. | `java-stdlib/tls-renegotiation.yaml` |
| `unirest-http-request` | `WARNING` | unirest-http-request 잠재적 결함 및 보안 이격율 정비 요망. | `java-stdlib/unirest-http-request.yaml` |
| `using-http-server` | `WARNING` | using-http-server 잠재적 결함 및 보안 이격율 정비 요망. | `js-node/using-http-server.yaml` |
