# Terraform Semgrep Rules Summary

`terraform` 디렉토리 하위의 규칙 목록입니다. (테스트 파일 제외)

## AWS
\n| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `aws-glacier-vault-any-principal` | `ERROR` | IaC 보안 옵션 누락 경보: aws-glacier-vault-any-principal 설정율을 적용해 주십시오. | `security/aws-glacier-vault-any-principal.yaml` |
| `aws-iam-admin-policy` | `ERROR` | IaC 보안 옵션 누락 경보: aws-iam-admin-policy 설정율을 적용해 주십시오. | `security/aws-iam-admin-policy.yaml` |
| `aws-iam-admin-policy-ssoadmin` | `ERROR` | IaC 보안 옵션 누락 경보: aws-iam-admin-policy-ssoadmin 설정율을 적용해 주십시오. | `security/aws-iam-admin-policy-ssoadmin.yaml` |
| `aws-kms-key-wildcard-principal` | `ERROR` | Terraform 구성 중 와일드카드(*) 권한 과잉 부여가 식별되었습니다. | `security/aws-kms-key-wildcard-principal.yaml` |
| `aws-lambda-environment-credentials` | `ERROR` | IaC 보안 옵션 누락 경보: aws-lambda-environment-credentials 설정율을 적용해 주십시오. | `security/aws-lambda-environment-credentials.yaml` |
| `aws-lambda-permission-unrestricted-source-arn` | `ERROR` | IaC 보안 옵션 누락 경보: aws-lambda-permission-unrestricted-source-arn 설정율을 적용해 주십시오. | `security/aws-lambda-permission-unrestricted-source-arn.yaml` |
| `aws-sqs-queue-policy-wildcard-principal` | `ERROR` | Terraform 구성 중 와일드카드(*) 권한 과잉 부여가 식별되었습니다. | `security/aws-sqs-queue-policy-wildcard-principal.yaml` |
| `wildcard-assume-role` | `ERROR` | Terraform 구성 중 와일드카드(*) 권한 과잉 부여가 식별되었습니다. | `security/wildcard-assume-role.yaml` |
\n## AZURE
\n| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `appservice-authentication-enabled` | `ERROR` | IaC 보안 옵션 누락 경보: appservice-authentication-enabled 설정율을 적용해 주십시오. | `security/appservice/appservice-authentication-enabled.yaml` |
| `appservice-enable-https-only` | `ERROR` | IaC 보안 옵션 누락 경보: appservice-enable-https-only 설정율을 적용해 주십시오. | `security/appservice/appservice-enable-https-only.yaml` |
| `appservice-use-secure-tls-policy` | `ERROR` | IaC 보안 옵션 누락 경보: appservice-use-secure-tls-policy 설정율을 적용해 주십시오. | `security/appservice/appservice-use-secure-tls-policy.yaml` |
| `keyvault-specify-network-acl` | `ERROR` | IaC 보안 옵션 누락 경보: keyvault-specify-network-acl 설정율을 적용해 주십시오. | `security/keyvault/keyvault-specify-network-acl.yaml` |
| `storage-default-action-deny` | `ERROR` | IaC 보안 옵션 누락 경보: storage-default-action-deny 설정율을 적용해 주십시오. | `security/storage/storage-default-action-deny.yaml` |
| `storage-use-secure-tls-policy` | `ERROR` | IaC 보안 옵션 누락 경보: storage-use-secure-tls-policy 설정율을 적용해 주십시오. | `security/storage/storage-use-secure-tls-policy.yaml` |
\n## LANG
\n| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `ec2-imdsv1-optional` | `ERROR` | IaC 보안 옵션 누락 경보: ec2-imdsv1-optional 설정율을 적용해 주십시오. | `security/ec2-imdsv1-optional.yaml` |
| `s3-public-rw-bucket` | `ERROR` | IaC 보안 옵션 누락 경보: s3-public-rw-bucket 설정율을 적용해 주십시오. | `security/s3-public-rw-bucket.yaml` |
