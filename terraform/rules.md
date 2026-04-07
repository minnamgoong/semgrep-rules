# Terraform Semgrep Rules Summary

`terraform` 디렉토리 하위의 규칙 목록입니다. (테스트 파일 제외)

## AWS

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `- id: aws-athena-client-can-disable-workgroup-encryption` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/aws-athena-client-can-disable-workgroup-encryption.yaml` |
| `- id: aws-athena-database-unencrypted` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/aws-athena-database-unencrypted.yaml` |
| `- id: aws-athena-workgroup-unencrypted` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/aws-athena-workgroup-unencrypted.yaml` |
| `- id: aws-backup-vault-unencrypted` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/aws-backup-vault-unencrypted.yaml` |
| `- id: aws-cloudtrail-encrypted-with-cmk` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/aws-cloudtrail-encrypted-with-cmk.yaml` |
| `- id: aws-cloudwatch-log-group-no-retention` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/aws-cloudwatch-log-group-no-retention.yaml` |
| `- id: aws-cloudwatch-log-group-unencrypted` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/aws-cloudwatch-log-group-unencrypted.yaml` |
| `- id: aws-codebuild-artifacts-unencrypted` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/aws-codebuild-artifacts-unencrypted.yaml` |
| `- id: aws-codebuild-project-artifacts-unencrypted` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/aws-codebuild-project-artifacts-unencrypted.yaml` |
| `- id: aws-codebuild-project-unencrypted` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/aws-codebuild-project-unencrypted.yaml` |
| `- id: aws-config-aggregator-not-all-regions` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/aws-config-aggregator-not-all-regions.yaml` |
| `- id: aws-db-instance-no-logging` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/aws-db-instance-no-logging.yaml` |
| `- id: aws-docdb-encrypted-with-cmk` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/aws-docdb-encrypted-with-cmk.yaml` |
| `- id: aws-documentdb-auditing-disabled` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/aws-documentdb-auditing-disabled.yaml` |
| `- id: aws-documentdb-storage-unencrypted` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/aws-documentdb-storage-unencrypted.yaml` |
| `- id: aws-dynamodb-point-in-time-recovery-disabled` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/aws-dynamodb-point-in-time-recovery-disabled.yaml` |
| `- id: aws-dynamodb-table-unencrypted` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/aws-dynamodb-table-unencrypted.yaml` |
| `- id: aws-ebs-snapshot-encrypted-with-cmk` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/aws-ebs-snapshot-encrypted-with-cmk.yaml` |
| `- id: aws-ebs-unencrypted` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/aws-ebs-unencrypted.yaml` |
| `- id: aws-ebs-volume-encrypted-with-cmk` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/aws-ebs-volume-encrypted-with-cmk.yaml` |
| `- id: aws-ebs-volume-unencrypted` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/aws-ebs-volume-unencrypted.yaml` |
| `- id: aws-ec2-has-public-ip` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/aws-ec2-has-public-ip.yaml` |
| `- id: aws-ec2-launch-configuration-ebs-block-device-unencrypted` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/aws-ec2-launch-configuration-ebs-block-device-unencrypted.yaml` |
| `- id: aws-ec2-launch-configuration-root-block-device-unencrypted` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/aws-ec2-launch-configuration-root-block-device-unencrypted.yml` |
| `- id: aws-ec2-launch-template-metadata-service-v1-enabled` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/aws-ec2-launch-template-metadata-service-v1-enabled.yaml` |
| `- id: aws-ec2-security-group-allows-public-ingress` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/aws-ec2-security-group-allows-public-ingress.yaml` |
| `aws-ec2-security-group-rule-missing-description` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/aws-ec2-security-group-rule-missing-description.yaml` |
| `- id: aws-ecr-image-scanning-disabled` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/aws-ecr-image-scanning-disabled.yaml` |
| `- id: aws-ecr-mutable-image-tags` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/aws-ecr-mutable-image-tags.yaml` |
| `- id: aws-ecr-repository-wildcard-principal` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/aws-ecr-repository-wildcard-principal.yaml` |
| `- id: aws-efs-filesystem-encrypted-with-cmk` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/aws-efs-filesystem-encrypted-with-cmk.yaml` |
| `- id: aws-elasticache-automatic-backup-not-enabled` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/aws-elasticache-automatic-backup-not-enabled.yaml` |
| `- id: aws-elasticsearch-insecure-tls-version` | `WARNING` | 보안 옵션 누사 및 예방 단속 필요. | `security/aws-elasticsearch-insecure-tls-version.yaml` |
| `- id: aws-elasticsearch-nodetonode-encryption-not-enabled` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/aws-elasticsearch-nodetonode-encryption.yaml` |
| `- id: aws-elb-access-logs-not-enabled` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/aws-elb-access-logs-not-enabled.yaml` |
| `- id: aws-emr-encrypted-with-cmk` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/aws-emr-encrypted-with-cmk.yaml` |
| `- id: aws-fsx-lustre-filesystem-encrypted-with-cmk` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/aws-fsx-lustre-files-ystem.yaml` |
| `- id: aws-fsx-lustre-filesystem-encrypted-with-cmk` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/aws-fsx-lustre-filesystem-encrypted-with-cmk.yaml` |
| `- id: aws-fsx-ontapfs-encrypted-with-cmk` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/aws-fsx-ontapfs-encrypted-with-cmk.yaml` |
| `- id: aws-fsx-windows-encrypted-with-cmk` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/aws-fsx-windows-encrypted-with-cmk.yaml` |
| `aws-glacier-vault-any-principal` | `ERROR` | IaC 보안 옵션 누락 경보: aws-glacier-vault-any-principal 설정율을 적용해 주십시오. | `security/aws-glacier-vault-any-principal.yaml` |
| `aws-iam-admin-policy` | `ERROR` | IaC 보안 옵션 누락 경보: aws-iam-admin-policy 설정율을 적용해 주십시오. | `security/aws-iam-admin-policy.yaml` |
| `aws-iam-admin-policy-ssoadmin` | `ERROR` | IaC 보안 옵션 누락 경보: aws-iam-admin-policy-ssoadmin 설정율을 적용해 주십시오. | `security/aws-iam-admin-policy-ssoadmin.yaml` |
| `- id: aws-imagebuilder-component-encrypted-with-cmk` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/aws-imagebuilder-component-encrypted-with-cmk.yaml` |
| `- id: aws-insecure-api-gateway-tls-version` | `WARNING` | 보안 옵션 누사 및 예방 단속 필요. | `security/aws-insecure-api-gateway-tls-version.yaml` |
| `- id: aws-insecure-cloudfront-distribution-tls-version` | `WARNING` | 보안 옵션 누사 및 예방 단속 필요. | `security/aws-cloudfront-insecure-tls.yaml` |
| `- id: aws-insecure-redshift-ssl-configuration` | `WARNING` | 보안 옵션 누사 및 예방 단속 필요. | `security/aws-insecure-redshift-ssl-configuration.yaml` |
| `- id: aws-kinesis-stream-encrypted-with-cmk` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/aws-kinesis-stream-encrypted-with-cmk.yaml` |
| `- id: aws-kinesis-stream-unencrypted` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/aws-kinesis-stream-unencrypted.yaml` |
| `- id: aws-kinesis-video-stream-encrypted-with-cmk` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/aws-kinesis-video-stream-encrypted-with-cmk.yaml` |
| `aws-kms-key-wildcard-principal` | `ERROR` | Terraform 구성 중 와일드카드(*) 권한 과잉 부여가 식별되었습니다. | `security/aws-kms-key-wildcard-principal.yaml` |
| `- id: aws-kms-no-rotation` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/aws-kms-no-rotation.yaml` |
| `aws-lambda-environment-credentials` | `ERROR` | IaC 보안 옵션 누락 경보: aws-lambda-environment-credentials 설정율을 적용해 주십시오. | `security/aws-lambda-environment-credentials.yaml` |
| `- id: aws-lambda-environment-unencrypted` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/aws-lambda-environment-unencrypted.yaml` |
| `aws-lambda-permission-unrestricted-source-arn` | `ERROR` | IaC 보안 옵션 누락 경보: aws-lambda-permission-unrestricted-source-arn 설정율을 적용해 주십시오. | `security/aws-lambda-permission-unrestricted-source-arn.yaml` |
| `- id: aws-lambda-x-ray-tracing-not-active` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/aws-lambda-x-ray-tracing-not-active.yaml` |
| `- id: aws-network-acl-allows-all-ports` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/aws-network-acl-allows-all-ports.yaml` |
| `- id: aws-network-acl-allows-public-ingress` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/aws-network-acl-allows-public-ingress.yaml` |
| `aws-opensearchserverless-encrypted-with-cmk` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/aws-opensearchserverless-encrypted-with-cmk.yaml` |
| `- id: aws-provider-static-credentials` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/aws-provider-static-credentials.yaml` |
| `aws-provisioner-exec` | `WARNING` | 프로비저너는 최후의 수단이므로 가능하면 피해야 합니다. 프로비저너 동작은 Terraform에서 계획의 일부로 매핑할 수 없으며 설계에 따라 임의의 셸 명령을 실행합니다. | `security/aws-provisioner-exec.yaml` |
| `- id: aws-qldb-inadequate-ledger-permissions-mode` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/aws-qldb-inadequate-ledger-permissions-mode.yaml` |
| `- id: aws-rds-backup-no-retention` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/aws-rds-backup-no-retention.yaml` |
| `- id: aws-rds-cluster-iam-authentication-not-enabled` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/aws-rds-cluster-iam-authentication-not-enabled.yaml` |
| `- id: aws-rds-iam-authentication-not-enabled` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/aws-rds-iam-authentication-not-enabled.yaml` |
| `- id: aws-rds-multiaz-not-enabled` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/aws-rds-multiaz-not-enabled.yaml` |
| `- id: aws-redshift-cluster-encrypted-with-cmk` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/aws-redshift-cluster-encrypted-with-cmk.yaml` |
| `- id: aws-s3-bucket-object-encrypted-with-cmk` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/aws-s3-bucket-object-encrypted-with-cmk.yaml` |
| `- id: aws-s3-bucket-versioning-not-enabled` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/aws-s3-bucket-versioning-not-enabled.yaml` |
| `- id: aws-s3-object-copy-encrypted-with-cmk` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/aws-s3-object-copy-encrypted-with-cmk.yaml` |
| `- id: aws-s3-object-lock-not-enabled` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/aws-s3-object-lock-not-enabled.yaml` |
| `- id: aws-sagemaker-domain-encrypted-with-cmk` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/aws-sagemaker-domain-encrypted-with-cmk.yaml` |
| `- id: aws-secretsmanager-secret-unencrypted` | `WARNING` | 자격증명/보안 기밀 문자열 누락 여부 점검. | `security/aws-secretsmanager-secret-unencrypted.yaml` |
| `- id: aws-sns-topic-unencrypted` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/aws-sns-topic-unencrypted.yaml` |
| `- id: aws-sqs-queue-policy-wildcard-action` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/aws-sqs-queue-policy-wildcard-action.yaml` |
| `aws-sqs-queue-policy-wildcard-principal` | `ERROR` | Terraform 구성 중 와일드카드(*) 권한 과잉 부여가 식별되었습니다. | `security/aws-sqs-queue-policy-wildcard-principal.yaml` |
| `- id: aws-sqs-queue-unencrypted` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/aws-sqs-queue-unencrypted.yaml` |
| `- id: aws-ssm-document-logging-issues` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/aws-ssm-document-logging-issues.yaml` |
| `- id: aws-subnet-has-public-ip-address` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/aws-subnet-has-public-ip-address.yaml` |
| `- id: aws-timestream-database-encrypted-with-cmk` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/aws-timestream-database-encrypted-with-cmk.yaml` |
| `- id: aws-transfer-server-is-public` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/aws-transfer-server-is-public.yaml` |
| `- id: aws-workspaces-root-volume-unencrypted` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/aws-workspaces-root-volume-unencrypted.yaml` |
| `- id: aws-workspaces-user-volume-unencrypted` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/aws-workspaces-user-volume-unencrypted.yaml` |
| `- id: insecure-load-balancer-tls-version` | `WARNING` | 보안 옵션 누사 및 예방 단속 필요. | `security/insecure-load-balancer-tls-version.yaml` |
| `lambda-permission-logs-missing-arn-asterisk` | `WARNING` | lambda-permission-logs-missing-arn-asterisk IaC 보안 설정 정비 및 예방 조치 요망. | `correctness/lambda-permission-logs-missing-arn-asterisk.yaml` |
| `lambda-redundant-field-with-image` | `WARNING` | lambda-redundant-field-with-image IaC 보안 설정 정비 및 예방 조치 요망. | `correctness/lambda-redundant-field-with-image.yaml` |
| `missing-alb-drop-http-headers` | `WARNING` | missing-alb-drop-http-headers IaC 보안 설정 정비 및 예방 조치 요망. | `best-practice/missing-alb-drop-http-headers.yaml` |
| `missing-api-gateway-cache-cluster` | `WARNING` | missing-api-gateway-cache-cluster IaC 보안 설정 정비 및 예방 조치 요망. | `best-practice/missing-api-gateway-cache-cluster.yaml` |
| `- id: missing-athena-workgroup-encryption` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/missing-athena-workgroup-encryption.yaml` |
| `missing-autoscaling-group-tags` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/missing-autoscaling-group-tags.yaml` |
| `- id: missing-aws-autoscaling-tags` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/missing-aws-autoscaling-tags.yaml` |
| `- id: missing-aws-cross-zone-lb` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/missing-aws-cross-zone-lb.yaml` |
| `- id: missing-aws-lb-deletion-protection` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/missing-aws-lb-deletion-protection.yaml` |
| `- id: missing-aws-qldb-deletion-protection` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/missing-aws-qldb-deletion-protection.yaml` |
| `missing-cloudwatch-log-group-kms-key` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/missing-cloudwatch-log-group-kms-key.yaml` |
| `missing-cloudwatch-log-group-retention` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/missing-cloudwatch-log-group-retention.yaml` |
| `- id: reserved-aws-lambda-environment-variable` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `correctness/reserved-aws-lambda-environment-variable.yaml` |
| `subscription-filter-missing-depends` | `WARNING` | subscription-filter-missing-depends IaC 보안 설정 정비 및 예방 조치 요망. | `correctness/subscription-filter-missing-depends.yaml` |
| `unrestricted-github-oidc-policy` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/unrestricted-github-oidc-policy.yaml` |
| `wildcard-assume-role` | `ERROR` | Terraform 구성 중 와일드카드(*) 권한 과잉 부여가 식별되었습니다. | `security/wildcard-assume-role.yaml` |

## AZURE

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `- id: appservice-account-identity-registered` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/appservice/appservice-account-identity-registered.yaml` |
| `appservice-authentication-enabled` | `ERROR` | IaC 보안 옵션 누락 경보: appservice-authentication-enabled 설정율을 적용해 주십시오. | `security/appservice/appservice-authentication-enabled.yaml` |
| `- id: appservice-enable-http2` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/appservice/appservice-enable-http2.yaml` |
| `appservice-enable-https-only` | `ERROR` | IaC 보안 옵션 누락 경보: appservice-enable-https-only 설정율을 적용해 주십시오. | `security/appservice/appservice-enable-https-only.yaml` |
| `- id: appservice-require-client-cert` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/appservice/appservice-require-client-cert.yaml` |
| `appservice-use-secure-tls-policy` | `ERROR` | IaC 보안 옵션 누락 경보: appservice-use-secure-tls-policy 설정율을 적용해 주십시오. | `security/appservice/appservice-use-secure-tls-policy.yaml` |
| `azure-ad-used-auth-service-fabric` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/azure-ad-used-auth-service-fabric.yaml` |
| `- id: azure-aks-apiserver-auth-ip-ranges` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/aks/azure-aks-apiserver-auth-ip-ranges.yaml` |
| `- id: azure-aks-private-clusters-enabled` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/aks/azure-aks-private-clusters-enabled.yaml` |
| `azure-aks-uses-azure-policies-addon` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/azure-aks-uses-azure-policies-addon.yaml` |
| `- id: azure-aks-uses-disk-encryptionset` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/aks/azure-aks-uses-disk-encryptionset.yaml` |
| `- id: azure-apiservices-use-virtualnetwork` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/apiservice/azure-apiservices-use-virtualnetwork.yaml` |
| `azure-appgateway-enables-waf` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/azure-appgateway-enables-waf.yaml` |
| `- id: azure-appservice-auth` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/appservice/azure-appservice-auth.yaml` |
| `- id: azure-appservice-client-certificate` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/appservice/azure-appservice-client-certificate.yaml` |
| `- id: azure-appservice-detailed-errormessages-enabled` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/appservice/azure-appservice-detailed-errormessages-enabled.yaml` |
| `- id: azure-appservice-disallowed-cors` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/appservice/azure-appservice-disallowed-cors.yaml` |
| `azure-appservice-dotnet-framework-version` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/azure-appservice-dotnet-framework-version.yaml` |
| `- id: azure-appservice-enabled-failed-request` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/appservice/azure-appservice-enabled-failed-request.yaml` |
| `azure-appservice-ftps-state` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/azure-appservice-ftps-state.yaml` |
| `- id: azure-appservice-http-logging-enabled` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/appservice/azure-appservice-http-logging-enabled.yaml` |
| `azure-appservice-https-20-enabled` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/azure-appservice-https-20-enabled.yaml` |
| `- id: azure-appservice-https-only` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/appservice/azure-appservice-https-only.yaml` |
| `- id: azure-appservice-identity` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/appservice/azure-appservice-identity.yaml` |
| `- id: azure-appservice-identityprovider-enabled` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/appservice/azure-appservice-identityprovider-enabled.yaml` |
| `azure-appservice-java-version` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/azure-appservice-java-version.yaml` |
| `- id: azure-appservice-min-tls-version` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/appservice/azure-appservice-min-tls-version.yaml` |
| `azure-appservice-php-version` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/azure-appservice-php-version.yaml` |
| `azure-appservice-python-version` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/azure-appservice-python-version.yaml` |
| `azure-appservice-used-azure-files` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/azure-appservice-used-azure-files.yaml` |
| `- id: azure-automation-encrypted` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/azure-automation-encrypted.yaml` |
| `- id: azure-batchaccount-uses-keyvault-encrpytion` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/azure-batchaccount-uses-keyvault-encrpytion.yaml` |
| `- id: azure-cognitiveservices-disables-public-network` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/azure-cognitiveservices-disables-public-network.yaml` |
| `- id: azure-containergroup-deployed-into-virtualnetwork` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/azure-containergroup-deployed-into-virtualnetwork.yaml` |
| `- id: azure-cosmosdb-accounts-restricted-access` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/azure-cosmosdb-accounts-restricted-access.yaml` |
| `- id: azure-cosmosdb-disable-access-key-write` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/azure-cosmosdb-disable-access-key-write.yaml` |
| `- id: azure-cosmosdb-disables-public-network` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/azure-cosmosdb-disables-public-network.yaml` |
| `- id: azure-cosmosdb-have-cmk` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/azure-cosmosdb-have-cmk.yaml` |
| `- id: azure-customrole-definition-subscription-owner` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/azure-customrole-definition-subscription-owner.yaml` |
| `- id: azure-dataexplorer-double-encryption-enabled` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/azure-dataexplorer-double-encryption-enabled.yaml` |
| `- id: azure-dataexplorer-uses-disk-encryption` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/azure-dataexplorer-uses-disk-encryption.yaml` |
| `- id: azure-datafactory-no-public-network-access` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/azure-datafactory-no-public-network-access.yaml` |
| `- id: azure-datafactory-uses-git-repository` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/azure-datafactory-uses-git-repository.yaml` |
| `- id: azure-datalake-store-encryption` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/azure-datalake-store-encryption.yaml` |
| `azure-defenderon-appservices` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/azure-defenderon-appservices.yaml` |
| `azure-defenderon-container-registry` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/azure-defenderon-container-registry.yaml` |
| `azure-defenderon-keyvaults` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/azure-defenderon-keyvaults.yaml` |
| `azure-defenderon-kubernetes` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/azure-defenderon-kubernetes.yaml` |
| `azure-defenderon-servers` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/azure-defenderon-servers.yaml` |
| `azure-defenderon-sqlservers` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/azure-defenderon-sqlservers.yaml` |
| `azure-defenderon-sqlservers-vms` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/azure-defenderon-sqlservers-vms.yaml` |
| `azure-defenderon-storage` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/azure-defenderon-storage.yaml` |
| `- id: azure-eventgrid-domain-network-access` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/azure-eventgrid-domain-network-access.yaml` |
| `azure-frontdoor-enables-waf` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/azure-frontdoor-enables-waf.yaml` |
| `azure-frontdoor-use-wafmode` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/azure-frontdoor-use-wafmode.yaml` |
| `- id: azure-functionapp-disallow-cors` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/azure-functionapp-disallow-cors.yaml` |
| `azure-functionapp-http-version-latest` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/azure-functionapp-http-version-latest.yaml` |
| `azure-functionapps-accessible-over-https` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/azure-functionapps-accessible-over-https.yaml` |
| `- id: azure-functionapps-enable-auth` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/azure-functionapps-enable-auth.yaml` |
| `- id: azure-instance-extensions` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/azure-instance-extensions.yaml` |
| `- id: azure-iot-no-public-network-access` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/azure-iot-no-public-network-access.yaml` |
| `- id: azure-key-backedby-hsm` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/azure-key-backedby-hsm.yaml` |
| `- id: azure-key-no-expiration-date` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/azure-key-no-expiration-date.yaml` |
| `azure-keyvault-enables-firewall-rules-settings` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/azure-keyvault-enables-firewall-rules-settings.yaml` |
| `azure-keyvault-enables-purge-protection` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/azure-keyvault-enables-purge-protection.yaml` |
| `azure-keyvault-enables-soft-delete` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/azure-keyvault-enables-soft-delete.yaml` |
| `azure-keyvault-recovery-enabled` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/azure-keyvault-recovery-enabled.yaml` |
| `- id: azure-managed-disk-encryption` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/azure-managed-disk-encryption.yaml` |
| `- id: azure-managed-disk-encryption-set` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/azure-managed-disk-encryption-set.yaml` |
| `azure-mariadb-geo-backup-enabled` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/azure-mariadb-geo-backup-enabled.yaml` |
| `- id: azure-mariadb-public-access-disabled` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/azure-mariadb-public-access-disabled.yaml` |
| `azure-mariadb-sslenforcement-enabled` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/azure-mariadb-sslenforcement-enabled.yaml` |
| `azure-monitor-log-profile-categories` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/azure-monitor-log-profile-categories.yaml` |
| `- id: azure-monitor-log-profile-retention-days` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/azure-monitor-log-profile-retention-days.yaml` |
| `azure-monitor-log-profile-retention-days` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/azure-monitor-log-profile-retention-days.yaml` |
| `- id: azure-mssql-service-mintls-version` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/azure-mssql-service-mintls-version.yaml` |
| `- id: azure-mysql-encryption-enabled` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/azure-mysql-encryption-enabled.yaml` |
| `azure-mysql-geo-backup-enabled` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/azure-mysql-geo-backup-enabled.yaml` |
| `- id: azure-mysql-mintls-version` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/azure-mysql-mintls-version.yaml` |
| `- id: azure-mysql-public-access-disabled` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/azure-mysql-public-access-disabled.yaml` |
| `azure-mysql-server-tlsenforcement-enabled` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/azure-mysql-server-tlsenforcement-enabled.yaml` |
| `azure-mysql-threat-detection-enabled` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/azure-mysql-threat-detection-enabled.yaml` |
| `azure-network-watcher-flowlog-period` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/azure-network-watcher-flowlog-period.yaml` |
| `- id: azure-networkinterface-enable-ip-forwarding` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/azure-networkinterface-enable-ip-forwarding.yaml` |
| `- id: azure-postgresql-encryption-enabled` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/azure-postgresql-encryption-enabled.yaml` |
| `azure-postgresql-flexi-server-geo-backup-enabled` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/azure-postgresql-flexi-server-geo-backup-enabled.yaml` |
| `azure-postgresql-geo-backup-enabled` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/azure-postgresql-geo-backup-enabled.yaml` |
| `- id: azure-postgresql-min-tls-version` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/azure-postgresql-min-tls-version.yaml` |
| `azure-postgresql-server-connection-throttling-enabled` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/azure-postgresql-server-connection-throttling-enabled.yaml` |
| `azure-postgresql-server-log-checkpoint-enabled` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/azure-postgresql-server-log-checkpoint-enabled.yaml` |
| `azure-postgresql-server-log-connections-enabled` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/azure-postgresql-server-log-connections-enabled.yaml` |
| `- id: azure-postgresql-server-public-access-disabled` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/azure-postgresql-server-public-access-disabled.yaml` |
| `azure-postgresql-ssl-enforcement-enabled` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/azure-postgresql-ssl-enforcement-enabled.yaml` |
| `azure-postgresql-threat-detection-enabled` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/azure-postgresql-threat-detection-enabled.yaml` |
| `- id: azure-redis-cache-enable-non-ssl-port` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/azure-redis-cache-enable-non-ssl-port.yaml` |
| `- id: azure-redis-cache-public-network-access-enabled` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/azure-redis-cache-public-network-access-enabled.yaml` |
| `- id: azure-remote-debugging-not-enabled` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/azure-remote-debugging-not-enabled.yaml` |
| `- id: azure-scale-set-password` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/azure-scale-set-password.yaml` |
| `- id: azure-search-publicnetwork-access-disabled` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/azure-search-publicnetwork-access-disabled.yaml` |
| `azure-secret-content-type` | `WARNING` | 자격증명/보안 기밀 문자열 누락 여부 점검. | `best-practice/azure-secret-content-type.yaml` |
| `azure-secret-expiration-date` | `WARNING` | 자격증명/보안 기밀 문자열 누락 여부 점검. | `best-practice/azure-secret-expiration-date.yaml` |
| `azure-securitcenter-email-alert` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/azure-securitcenter-email-alert.yaml` |
| `azure-securitycenter-contact-emails` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/azure-securitycenter-contact-emails.yaml` |
| `azure-securitycenter-contact-phone` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/azure-securitycenter-contact-phone.yaml` |
| `azure-securitycenter-email-alert-admins` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/azure-securitycenter-email-alert-admins.yaml` |
| `azure-securitycenter-standard-pricing` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/azure-securitycenter-standard-pricing.yaml` |
| `- id: azure-service-fabric-cluster-protection-level` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/azure-service-fabric-cluster-protection-level.yaml` |
| `azure-sqlserver-email-alerts-enabled` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/azure-sqlserver-email-alerts-enabled.yaml` |
| `azure-sqlserver-email-alerts-toadmins-enabled` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/azure-sqlserver-email-alerts-toadmins-enabled.yaml` |
| `- id: azure-sqlserver-no-public-access` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/azure-sqlserver-no-public-access.yaml` |
| `- id: azure-sqlserver-public-access-disabled` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/azure-sqlserver-public-access-disabled.yaml` |
| `azure-sqlserver-threat-detection-types` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/azure-sqlserver-threat-detection-types.yaml` |
| `- id: azure-storage-account-disable-public-access` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/azure-storage-account-disable-public-access.yaml` |
| `azure-storage-account-enables-secure-transfer` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/azure-storage-account-enables-secure-transfer.yaml` |
| `- id: azure-storage-account-minimum-tlsversion` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/azure-storage-account-minimum-tlsversion.yaml` |
| `- id: azure-storage-blob-service-container-private-access` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/azure-storage-blob-service-container-private-access.yaml` |
| `- id: azure-storage-sync-public-access-disabled` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/azure-storage-sync-public-access-disabled.yaml` |
| `azure-synapse-workscape-enables-managed-virtual-network` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/azure-synapse-workscape-enables-managed-virtual-network.yaml` |
| `- id: azure-vmencryption-at-host-enabled` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/azure-vmencryption-at-host-enabled.yaml` |
| `azure-vmscale-sets-auto-os-image-patching-enabled` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/azure-vmscale-sets-auto-os-image-patching-enabled.yaml` |
| `azure-waf-specificed-mode-app-gw` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/azure-waf-specificed-mode-app-gw.yaml` |
| `- id: functionapp-authentication-enabled` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/functionapp/functionapp-authentication-enabled.yaml` |
| `- id: functionapp-enable-http2` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/functionapp/functionapp-enable-http2.yaml` |
| `- id: keyvault-content-type-for-secret` | `INFO` | 자격증명/보안 기밀 문자열 누락 여부 점검. | `security/keyvault/keyvault-content-type-for-secret.yaml` |
| `- id: keyvault-ensure-key-expires` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/keyvault/keyvault-ensure-key-expires.yaml` |
| `- id: keyvault-ensure-secret-expires` | `INFO` | 자격증명/보안 기밀 문자열 누락 여부 점검. | `security/keyvault/keyvault-ensure-secret-expires.yaml` |
| `- id: keyvault-purge-enabled` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/keyvault/keyvault-purge-enabled.yaml` |
| `keyvault-specify-network-acl` | `ERROR` | IaC 보안 옵션 누락 경보: keyvault-specify-network-acl 설정율을 적용해 주십시오. | `security/keyvault/keyvault-specify-network-acl.yaml` |
| `- id: storage-allow-microsoft-service-bypass` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/storage/storage-allow-microsoft-service-bypass.yaml` |
| `storage-default-action-deny` | `ERROR` | IaC 보안 옵션 누락 경보: storage-default-action-deny 설정율을 적용해 주십시오. | `security/storage/storage-default-action-deny.yaml` |
| `- id: storage-enforce-https` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/storage/storage-enforce-https.yaml` |
| `- id: storage-queue-services-logging` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/storage/storage-queue-services-logging.yaml` |
| `storage-use-secure-tls-policy` | `ERROR` | IaC 보안 옵션 누락 경보: storage-use-secure-tls-policy 설정율을 적용해 주십시오. | `security/storage/storage-use-secure-tls-policy.yaml` |

## GCP

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `- id: gcp-artifact-registry-encrypted-with-cmk` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-artifact-registry-encrypted-with-cmk.yaml` |
| `- id: gcp-artifact-registry-private-repo-iam-binding` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-artifact-registry-private-repo-iam-binding.yaml` |
| `- id: gcp-artifact-registry-private-repo-iam-member` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-artifact-registry-private-repo-iam-member.yaml` |
| `- id: gcp-bigquery-dataset-encrypted-with-cmk` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-bigquery-dataset-encrypted-with-cmk.yaml` |
| `- id: gcp-bigquery-private-table-iam-binding` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-bigquery-private-table-iam-binding.yaml` |
| `- id: gcp-bigquery-private-table-iam-member` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-bigquery-private-table-iam-member.yaml` |
| `- id: gcp-bigquery-table-encrypted-with-cmk` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-bigquery-table-encrypted-with-cmk.yaml` |
| `- id: gcp-bigtable-instance-encrypted-with-cmk` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-bigtable-instance-encrypted-with-cmk.yaml` |
| `- id: gcp-build-workers-private` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-build-workers-private.yaml` |
| `- id: gcp-cloud-storage-logging` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-cloud-storage-logging.yaml` |
| `- id: gcp-compute-boot-disk-encryption` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-compute-boot-disk-encryption.yaml` |
| `- id: gcp-compute-disk-encryption` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-compute-disk-encryption.yaml` |
| `- id: gcp-compute-firewall-unrestricted-ingress-20` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-compute-firewall-unrestricted-ingress-20.yaml` |
| `- id: gcp-compute-firewall-unrestricted-ingress-21` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-compute-firewall-unrestricted-ingress-21.yaml` |
| `- id: gcp-compute-firewall-unrestricted-ingress-22` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-compute-firewall-unrestricted-ingress-22.yaml` |
| `- id: gcp-compute-firewall-unrestricted-ingress-3306` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-compute-firewall-unrestricted-ingress-3306.yaml` |
| `- id: gcp-compute-firewall-unrestricted-ingress-3389` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-compute-firewall-unrestricted-ingress-3389.yaml` |
| `- id: gcp-compute-firewall-unrestricted-ingress-80` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-compute-firewall-unrestricted-ingress-80.yaml` |
| `- id: gcp-compute-ip-forward` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-compute-ip-forward.yaml` |
| `- id: gcp-compute-os-login` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-compute-os-login.yaml` |
| `- id: gcp-compute-project-os-login` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-compute-project-os-login.yaml` |
| `- id: gcp-compute-public-ip` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-compute-public-ip.yaml` |
| `- id: gcp-compute-serial-ports` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-compute-serial-ports.yaml` |
| `- id: gcp-compute-shielded-vm` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/gcp-compute-shielded-vm.yaml` |
| `- id: gcp-compute-ssl-policy` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-compute-ssl-policy.yaml` |
| `- id: gcp-compute-template-ip-forward` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-compute-template-ip-forward.yaml` |
| `- id: gcp-compute-template-public-ip` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-compute-template-public-ip.yaml` |
| `- id: gcp-compute-template-shielded-vm` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/gcp-compute-template-shielded-vm.yaml` |
| `- id: gcp-dataflow-job-encrypted-with-cmk` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-dataflow-job-encrypted-with-cmk.yaml` |
| `- id: gcp-dataflow-private-job` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-dataflow-private-job.yaml` |
| `- id: gcp-datafusion-private-instance` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-datafusion-private-instance.yaml` |
| `- id: gcp-datafusion-stack-driver-logging` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-datafusion-stack-driver-logging.yaml` |
| `- id: gcp-datafusion-stack-driver-monitoring` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-datafusion-stack-driver-monitoring.yaml` |
| `- id: gcp-dataproc-cluster-encrypted-with-cmk` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-dataproc-cluster-encrypted-with-cmk.yaml` |
| `- id: gcp-dataproc-cluster-public-ip` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-dataproc-cluster-public-ip.yaml` |
| `- id: gcp-dataproc-private-cluster-iam-binding` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-dataproc-private-cluster-iam-binding.yaml` |
| `- id: gcp-dataproc-private-cluster-iam-member` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-dataproc-private-cluster-iam-member.yaml` |
| `- id: gcp-dns-key-specs-rsasha1` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-dns-key-specs-rsasha1.yaml` |
| `gcp-dnssec-enabled` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/gcp-dnssec-enabled.yaml` |
| `- id: gcp-folder-impersonation-roles-iam-binding` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-folder-impersonation-roles-iam-binding.yaml` |
| `- id: gcp-folder-impersonation-roles-iam-member` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-folder-impersonation-roles-iam-member.yaml` |
| `- id: gcp-folder-member-default-service-account-iam-binding` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-folder-member-default-service-account-iam-binding.yaml` |
| `- id: gcp-folder-member-default-service-account-iam-member` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-folder-member-default-service-account-iam-member.yaml` |
| `- id: gcp-gke-alias-ip-enabled` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/gcp-gke-alias-ip-enabled.yaml` |
| `- id: gcp-gke-basic-auth` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-gke-basic-auth.yaml` |
| `- id: gcp-gke-binary-authorization` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/gcp-gke-binary-authorization.yaml` |
| `- id: gcp-gke-client-certificate-disabled` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-gke-client-certificate-disabled.yaml` |
| `- id: gcp-gke-cluster-logging` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-gke-cluster-logging.yaml` |
| `- id: gcp-gke-enable-shielded-nodes` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/gcp-gke-enable-shielded-nodes.yaml` |
| `- id: gcp-gke-enabled-vpc-flow-logs` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-gke-enabled-vpc-flow-logs.yaml` |
| `- id: gcp-gke-ensure-integrity-monitoring` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-gke-ensure-integrity-monitoring.yaml` |
| `- id: gcp-gke-has-labels` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/gcp-gke-has-labels.yaml` |
| `- id: gcp-gke-kubernetes-rbac-google-groups` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-gke-kubernetes-rbac-google-groups.yaml` |
| `- id: gcp-gke-legacy-auth-enabled` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-gke-legacy-auth-enabled.yaml` |
| `- id: gcp-gke-legacy-instance-metadata-disabled` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-gke-legacy-instance-metadata-disabled.yaml` |
| `- id: gcp-gke-master-authz-networks-enabled` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-gke-master-authz-networks-enabled.yaml` |
| `- id: gcp-gke-metadata-server-enabled` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/gcp-gke-metadata-server-enabled.yaml` |
| `- id: gcp-gke-monitoring-enabled` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-gke-monitoring-enabled.yaml` |
| `- id: gcp-gke-network-policy-enabled` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-gke-network-policy-enabled.yaml` |
| `- id: gcp-gke-nodepool-auto-repair-enabled` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/gcp-gke-nodepool-auto-repair-enabled.yaml` |
| `gcp-gke-nodepool-auto-upgrade-enabled` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/gcp-gke-nodepool-auto-upgrade-enabled.yaml` |
| `- id: gcp-gke-nodepool-integrity-monitoring` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-gke-nodepool-integrity-monitoring.yaml` |
| `gcp-gke-nodepool-metadata-server-enabled` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/gcp-gke-nodepool-metadata-server-enabled.yaml` |
| `gcp-gke-nodepool-secure-boot-for-shielded-nodes` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/gcp-gke-nodepool-secure-boot-for-shielded-nodes.yaml` |
| `- id: gcp-gke-pod-security-policy-enabled` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-gke-pod-security-policy-enabled.yaml` |
| `- id: gcp-gke-private-cluster-config` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-gke-private-cluster-config.yaml` |
| `- id: gcp-gke-public-control-plane` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-gke-public-control-plane.yaml` |
| `- id: gcp-gke-secure-boot-for-shielded-nodes` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-gke-secure-boot-for-shielded-nodes.yaml` |
| `- id: gcp-gke-sql-backup-configuration-enabled` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/gcp-gke-sql-backup-configuration-enabled.yaml` |
| `- id: gcp-gke-use-cos-image` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/gcp-gke-use-cos-image.yaml` |
| `- id: gcp-insecure-load-balancer-tls-version` | `WARNING` | 보안 옵션 누사 및 예방 단속 필요. | `security/gcp-insecure-load-balancer-tls-version.yaml` |
| `- id: gcp-ipv6-private-google-enabled` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/gcp-ipv6-private-google-enabled.yaml` |
| `- id: gcp-kms-prevent-destroy` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-kms-prevent-destroy.yaml` |
| `- id: gcp-memory-store-for-redis-auth-enabled` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-memory-store-for-redis-auth-enabled.yaml` |
| `- id: gcp-memory-store-for-redis-intransit-encryption` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-memory-store-for-redis-intransit-encryption.yaml` |
| `gcp-mysql-local-in-file-off` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/gcp-mysql-local-in-file-off.yaml` |
| `- id: gcp-org-impersonation-roles-iam-binding` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-org-impersonation-roles-iam-binding.yaml` |
| `- id: gcp-org-impersonation-roles-iam-member` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-org-impersonation-roles-iam-member.yaml` |
| `- id: gcp-org-member-default-service-account-iam-binding` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-org-member-default-service-account-iam-binding.yaml` |
| `- id: gcp-org-member-default-service-account-iam-member` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-org-member-default-service-account-iam-member.yaml` |
| `gcp-postgresql-log-checkpoints` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/gcp-postgresql-log-checkpoints.yaml` |
| `gcp-postgresql-log-connection` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/gcp-postgresql-log-connection.yaml` |
| `gcp-postgresql-log-disconnection` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/gcp-postgresql-log-disconnection.yaml` |
| `gcp-postgresql-log-lock-waits` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/gcp-postgresql-log-lock-waits.yaml` |
| `gcp-postgresql-log-min-duration` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/gcp-postgresql-log-min-duration.yaml` |
| `gcp-postgresql-log-min-message` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/gcp-postgresql-log-min-message.yaml` |
| `gcp-postgresql-log-temp` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/gcp-postgresql-log-temp.yaml` |
| `- id: gcp-project-default-network` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-project-default-network.yaml` |
| `- id: gcp-project-member-default-service-account-iam-binding` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-project-member-default-service-account-iam-binding.yaml` |
| `- id: gcp-project-member-default-service-account-iam-member` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-project-member-default-service-account-iam-member.yaml` |
| `- id: gcp-project-service-account-user-iam-binding` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-project-service-account-user-iam-binding.yaml` |
| `- id: gcp-project-service-account-user-iam-member` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-project-service-account-user-iam-member.yaml` |
| `- id: gcp-pubsub-encrypted-with-cmk` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-pubsub-encrypted-with-cmk.yaml` |
| `- id: gcp-pubsub-private-topic-iam-binding` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-pubsub-private-topic-iam-binding.yaml` |
| `- id: gcp-pubsub-private-topic-iam-member` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-pubsub-private-topic-iam-member.yaml` |
| `- id: gcp-run-private-service-iam-binding` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-run-private-service-iam-binding.yaml` |
| `- id: gcp-run-private-service-iam-member` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-run-private-service-iam-member.yaml` |
| `- id: gcp-spanner-database-encrypted-with-cmk` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-spanner-database-encrypted-with-cmk.yaml` |
| `- id: gcp-sql-database-require-ssl` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-sql-database-require-ssl.yaml` |
| `- id: gcp-sql-database-ssl-insecure-value-postgres-mysql` | `WARNING` | 보안 옵션 누사 및 예방 단속 필요. | `security/gcp-sql-database-ssl-insecure-value-postgres-mysql.yaml` |
| `- id: gcp-sql-database-ssl-insecure-value-sqlserver` | `WARNING` | 보안 옵션 누사 및 예방 단속 필요. | `security/gcp-sql-database-ssl-insecure-value-sqlserver.yaml` |
| `- id: gcp-sql-public-database` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-sql-public-database.yaml` |
| `- id: gcp-sqlserver-no-public-ip` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-sqlserver-no-public-ip.yaml` |
| `- id: gcp-storage-bucket-not-public-iam-binding` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-storage-bucket-not-public-iam-binding.yaml` |
| `- id: gcp-storage-bucket-not-public-iam-member` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-storage-bucket-not-public-iam-member.yaml` |
| `- id: gcp-storage-bucket-uniform-access` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-storage-bucket-uniform-access.yaml` |
| `gcp-storage-versioning-enabled` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/gcp-storage-versioning-enabled.yaml` |
| `- id: gcp-sub-network-logging-enabled` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-sub-network-logging-enabled.yaml` |
| `- id: gcp-sub-network-private-google-enabled` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-sub-network-private-google-enabled.yaml` |
| `- id: gcp-vertexai-dataset-encrypted-with-cmk` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-vertexai-dataset-encrypted-with-cmk.yaml` |
| `- id: gcp-vertexai-metadata-store-encrypted-with-cmk` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-vertexai-metadata-store-encrypted-with-cmk.yaml` |
| `- id: gcp-vertexai-private-instance` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcp-vertexai-private-instance.yaml` |

## LANG

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `all-origins-allowed` | `WARNING` | all-origins-allowed IaC 보안 설정 정비 및 예방 조치 요망. | `security/s3-cors-all-origins.yaml` |
| `ec2-imdsv1-optional` | `ERROR` | IaC 보안 옵션 누락 경보: ec2-imdsv1-optional 설정율을 적용해 주십시오. | `security/ec2-imdsv1-optional.yaml` |
| `- id: ecr-image-scan-on-push` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/ecr-image-scan-on-push.yaml` |
| `eks-insufficient-control-plane-logging` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/eks-insufficient-control-plane-logging.yaml` |
| `- id: eks-public-endpoint-enabled` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/eks-public-endpoint-enabled.yaml` |
| `- id: elastic-search-encryption-at-rest` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/elastic-search-encryption-at-rest.yaml` |
| `- id: no-iam-admin-privileges` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/iam/no-iam-admin-privileges.yaml` |
| `- id: no-iam-creds-exposure` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/iam/no-iam-creds-exposure.yaml` |
| `- id: no-iam-data-exfiltration` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/iam/no-iam-data-exfiltration.yaml` |
| `- id: no-iam-priv-esc-funcs` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/iam/no-iam-priv-esc-funcs.yaml` |
| `- id: no-iam-priv-esc-other-users` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/iam/no-iam-priv-esc-other-users.yaml` |
| `- id: no-iam-priv-esc-roles` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/iam/no-iam-priv-esc-roles.yaml` |
| `- id: no-iam-resource-exposure` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/iam/no-iam-resource-exposure.yaml` |
| `- id: no-iam-star-actions` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/iam/no-iam-star-actions.yaml` |
| `rds-insecure-password-storage-in-source-code` | `WARNING` | rds-insecure-password-storage-in-source-code IaC 보안 설정 정비 및 예방 조치 요망. | `security/rds-insecure-password-storage-in-source-code.yaml` |
| `rds-public-access` | `WARNING` | rds-public-access IaC 보안 설정 정비 및 예방 조치 요망. | `security/rds-public-access.yaml` |
| `s3-public-read-bucket` | `WARNING` | S3 버킷 퍼블릭 오픈 및 암호화 누락 경보. | `security/s3-public-read-bucket.yaml` |
| `s3-public-rw-bucket` | `ERROR` | IaC 보안 옵션 누락 경보: s3-public-rw-bucket 설정율을 적용해 주십시오. | `security/s3-public-rw-bucket.yaml` |
| `s3-unencrypted-bucket` | `INFO` | S3 버킷 퍼블릭 오픈 및 암호화 누락 경보. | `security/s3-unencrypted-bucket.yaml` |
