# Html Semgrep Rules Summary

`html` 디렉토리 하위의 규칙 목록입니다. (테스트 파일 제외)

## BEST-PRACTICE

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `robots-denied` | `INFO` | robots-denied 잠재적 결함 및 보안 이격율 정비 요망. | `robots-denied.yaml` |

## CORRECTNESS

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `https-equiv` | `ERROR` | HTTPS 꼬리표 결여 및 메타 데이터 누출 경하 점검. | `https-equiv.yaml` |

## SECURITY

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `eval-detected` | `WARNING` | eval-detected 잠재적 결함 및 보안 이격율 정비 요망. | `audit/eval-detected.yaml` |
| `insecure-document-method` | `WARNING` | 보안 옵션 누사 및 예방 단속 필요. | `audit/insecure-document-method.yaml` |
| `missing-integrity` | `WARNING` | missing-integrity 잠재적 결함 및 보안 이격율 정비 요망. | `audit/missing-integrity.yaml` |
| `plaintext-http-link` | `WARNING` | plaintext-http-link 잠재적 결함 및 보안 이격율 정비 요망. | `plaintext-http-link.yaml` |
