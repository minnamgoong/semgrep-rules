# Typescript Semgrep Rules Summary

`typescript` 디렉토리 하위의 규칙 목록입니다. (테스트 파일 제외)

## AWS-CDK
\n| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `aws-cdk-bucket-enforcessl` | `ERROR` | S3 버킷에 전송 중 암호화(SSL/TLS) 강제화 옵션이 누락되었습니다. 데이터 전송 기밀성을 위해 해당 옵션을 활성화하십시오. | `security/audit/awscdk-bucket-enforcessl.yml` |
| `awscdk-bucket-encryption` | `ERROR` | AWS CDK S3 버킷 생성 시 기본 암호화(KMS_MANAGED 등) 설정이 누락되었습니다. 데이터 보안을 위해 암호화 모드를 지정하세요. | `security/audit/awscdk-bucket-encryption.yml` |
\n## LANG
\n| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `useless-ternary` | `ERROR` | 불필요한 삼항 연산자(a ? true : false 등) 사용이 감지되었습니다. 논리 직관성을 위해 단순 불리언 캐스팅 등으로 대체하세요. | `correctness/useless-ternary.yaml` |
\n## REACT
\n| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `react-insecure-request` | `ERROR` | React 애플리케이션에서 암호화되지 않은 HTTP 요청이 감지되었습니다. 스니핑 공격에 노출되므로 https:// 사용을 권장합니다. | `security/react-insecure-request.yaml` |
