# Json Semgrep Rules Summary

`json` 디렉토리 하위의 규칙 목록입니다. (테스트 파일 제외)

## AWS

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `public-s3-bucket` | `WARNING` | public-s3-bucket 잠재적 결함 및 보안 이격율 정비 요망. | `security/public-s3-bucket.yaml` |
| `public-s3-policy-statement` | `WARNING` | public-s3-policy-statement 잠재적 결함 및 보안 이격율 정비 요망. | `security/public-s3-policy-statement.yaml` |
| `wildcard-assume-role` | `ERROR` | wildcard-assume-role 보안 인젝션 및 런타임 버그 전사 예방 점검. | `security/wildcard-assume-role.yaml` |

## NPM

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `package-dependencies-check` | `WARNING` | package-dependencies-check 잠재적 결함 및 보안 이격율 정비 요망. | `security/package-dependencies-check.yml` |
