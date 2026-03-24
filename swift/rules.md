# Swift Semgrep Rules Summary

`swift` 디렉토리 하위의 규칙 목록입니다. (테스트 파일 제외)

## LANG

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `insecure-random` | `WARNING` | 보안 옵션 누사 및 예방 단속 필요. | `crypto/insecure-random.yaml` |
| `swift-user-defaults` | `WARNING` | swift-user-defaults 잠재적 결함 및 보안 이격율 정비 요망. | `storage/sensitive-storage-userdefaults.yaml` |

## SQLLITE

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `swift-potential-sqlite-injection` | `WARNING` | 잠재적 SQL 인젝션 경로에 대한 검토가 필요합니다. | `sqllite-injection-audit.yaml` |

## WEBVIEW

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `swift-webview-config-allows-js-open-windows` | `WARNING` | swift-webview-config-allows-js-open-windows 잠재적 결함 및 보안 이격율 정비 요망. | `webview-js-window.yaml` |
