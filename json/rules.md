# Json Semgrep Rules Summary

`json` 디렉토리 하위의 규칙 목록입니다. (테스트 파일 제외)

## AWS

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `- id: public-s3-bucket` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/public-s3-bucket.yaml` |
| `- id: public-s3-policy-statement` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/public-s3-policy-statement.yaml` |
| `wildcard-assume-role` | `ERROR` | wildcard-assume-role 보안 인젝션 및 런타임 버그 전사 예방 점검. | `security/wildcard-assume-role.yaml` |

## NPM

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `- id: package-dependencies-check` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/package-dependencies-check.yml` |
