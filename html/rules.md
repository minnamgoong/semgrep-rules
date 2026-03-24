# Html Semgrep Rules Summary

`html` 디렉토리 하위의 규칙 목록입니다. (테스트 파일 제외)

## BEST-PRACTICE

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `robots-denied` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `robots-denied.yaml` |

## CORRECTNESS

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `https-equiv` | `ERROR` | HTTPS 꼬리표 결여 및 메타 데이터 누출 경하 점검. | `https-equiv.yaml` |

## SECURITY

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `eval-detected` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `audit/eval-detected.yaml` |
| `insecure-document-method` | `WARNING` | 보안 옵션 누사 및 예방 단속 필요. | `audit/insecure-document-method.yaml` |
| `missing-integrity` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `audit/missing-integrity.yaml` |
| `plaintext-http-link` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `plaintext-http-link.yaml` |
