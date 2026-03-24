# Terraform Semgrep Rules Summary

`terraform` 디렉토리 하위의 규칙 목록입니다. (테스트 파일 제외)

## AWS

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `aws-athena-client-can-disable-workgroup-encryption` | `WARNING` | aws-athena-client-can-disable-workgroup-encryption 잠재적 결함 및 보안 이격율 정비 요망. | `security/aws-athena-client-can-disable-workgroup-encryption.yaml` |
| `aws-athena-database-unencrypted` | `WARNING` | aws-athena-database-unencrypted 잠재적 결함 및 보안 이격율 정비 요망. | `security/aws-athena-database-unencrypted.yaml` |
| `aws-athena-workgroup-unencrypted` | `WARNING` | aws-athena-workgroup-unencrypted 잠재적 결함 및 보안 이격율 정비 요망. | `security/aws-athena-workgroup-unencrypted.yaml` |
| `aws-backup-vault-unencrypted` | `WARNING` | aws-backup-vault-unencrypted 잠재적 결함 및 보안 이격율 정비 요망. | `security/aws-backup-vault-unencrypted.yaml` |
| `aws-cloudtrail-encrypted-with-cmk` | `WARNING` | aws-cloudtrail-encrypted-with-cmk 잠재적 결함 및 보안 이격율 정비 요망. | `security/aws-cloudtrail-encrypted-with-cmk.yaml` |
| `aws-cloudwatch-log-group-no-retention` | `WARNING` | aws-cloudwatch-log-group-no-retention 잠재적 결함 및 보안 이격율 정비 요망. | `security/aws-cloudwatch-log-group-no-retention.yaml` |
| `aws-cloudwatch-log-group-unencrypted` | `WARNING` | aws-cloudwatch-log-group-unencrypted 잠재적 결함 및 보안 이격율 정비 요망. | `security/aws-cloudwatch-log-group-unencrypted.yaml` |
| `aws-codebuild-artifacts-unencrypted` | `WARNING` | aws-codebuild-artifacts-unencrypted 잠재적 결함 및 보안 이격율 정비 요망. | `security/aws-codebuild-artifacts-unencrypted.yaml` |
| `aws-codebuild-project-artifacts-unencrypted` | `WARNING` | aws-codebuild-project-artifacts-unencrypted 잠재적 결함 및 보안 이격율 정비 요망. | `security/aws-codebuild-project-artifacts-unencrypted.yaml` |
| `aws-codebuild-project-unencrypted` | `WARNING` | aws-codebuild-project-unencrypted 잠재적 결함 및 보안 이격율 정비 요망. | `security/aws-codebuild-project-unencrypted.yaml` |
| `aws-config-aggregator-not-all-regions` | `WARNING` | aws-config-aggregator-not-all-regions 잠재적 결함 및 보안 이격율 정비 요망. | `security/aws-config-aggregator-not-all-regions.yaml` |
| `aws-db-instance-no-logging` | `WARNING` | aws-db-instance-no-logging 잠재적 결함 및 보안 이격율 정비 요망. | `security/aws-db-instance-no-logging.yaml` |
| `aws-docdb-encrypted-with-cmk` | `WARNING` | aws-docdb-encrypted-with-cmk 잠재적 결함 및 보안 이격율 정비 요망. | `security/aws-docdb-encrypted-with-cmk.yaml` |
| `aws-documentdb-auditing-disabled` | `INFO` | aws-documentdb-auditing-disabled 잠재적 결함 및 보안 이격율 정비 요망. | `security/aws-documentdb-auditing-disabled.yaml` |
| `aws-documentdb-storage-unencrypted` | `WARNING` | aws-documentdb-storage-unencrypted 잠재적 결함 및 보안 이격율 정비 요망. | `security/aws-documentdb-storage-unencrypted.yaml` |
| `aws-dynamodb-point-in-time-recovery-disabled` | `INFO` | aws-dynamodb-point-in-time-recovery-disabled 잠재적 결함 및 보안 이격율 정비 요망. | `security/aws-dynamodb-point-in-time-recovery-disabled.yaml` |
| `aws-dynamodb-table-unencrypted` | `WARNING` | aws-dynamodb-table-unencrypted 잠재적 결함 및 보안 이격율 정비 요망. | `security/aws-dynamodb-table-unencrypted.yaml` |
| `aws-ebs-snapshot-encrypted-with-cmk` | `WARNING` | aws-ebs-snapshot-encrypted-with-cmk 잠재적 결함 및 보안 이격율 정비 요망. | `security/aws-ebs-snapshot-encrypted-with-cmk.yaml` |
| `aws-ebs-unencrypted` | `WARNING` | aws-ebs-unencrypted 잠재적 결함 및 보안 이격율 정비 요망. | `security/aws-ebs-unencrypted.yaml` |
| `aws-ebs-volume-encrypted-with-cmk` | `WARNING` | aws-ebs-volume-encrypted-with-cmk 잠재적 결함 및 보안 이격율 정비 요망. | `security/aws-ebs-volume-encrypted-with-cmk.yaml` |
| `aws-ebs-volume-unencrypted` | `WARNING` | aws-ebs-volume-unencrypted 잠재적 결함 및 보안 이격율 정비 요망. | `security/aws-ebs-volume-unencrypted.yaml` |
| `aws-ec2-has-public-ip` | `WARNING` | aws-ec2-has-public-ip 잠재적 결함 및 보안 이격율 정비 요망. | `security/aws-ec2-has-public-ip.yaml` |
| `aws-ec2-launch-configuration-ebs-block-device-unencrypted` | `WARNING` | aws-ec2-launch-configuration-ebs-block-device-unencrypted 잠재적 결함 및 보안 이격율 정비 요망. | `security/aws-ec2-launch-configuration-ebs-block-device-unencrypted.yaml` |
| `aws-ec2-launch-configuration-root-block-device-unencrypted` | `WARNING` | aws-ec2-launch-configuration-root-block-device-unencrypted 잠재적 결함 및 보안 이격율 정비 요망... | `security/aws-ec2-launch-configuration-root-block-device-unencrypted.yml` |
| `aws-ec2-launch-template-metadata-service-v1-enabled` | `WARNING` | aws-ec2-launch-template-metadata-service-v1-enabled 잠재적 결함 및 보안 이격율 정비 요망. | `security/aws-ec2-launch-template-metadata-service-v1-enabled.yaml` |
| `aws-ec2-security-group-allows-public-ingress` | `WARNING` | aws-ec2-security-group-allows-public-ingress 잠재적 결함 및 보안 이격율 정비 요망. | `security/aws-ec2-security-group-allows-public-ingress.yaml` |
| `aws-ec2-security-group-rule-missing-description` | `INFO` | aws-ec2-security-group-rule-missing-description 잠재적 결함 및 보안 이격율 정비 요망. | `security/aws-ec2-security-group-rule-missing-description.yaml` |
| `aws-ecr-image-scanning-disabled` | `WARNING` | aws-ecr-image-scanning-disabled 잠재적 결함 및 보안 이격율 정비 요망. | `security/aws-ecr-image-scanning-disabled.yaml` |
| `aws-ecr-mutable-image-tags` | `WARNING` | aws-ecr-mutable-image-tags 잠재적 결함 및 보안 이격율 정비 요망. | `security/aws-ecr-mutable-image-tags.yaml` |
| `aws-ecr-repository-wildcard-principal` | `WARNING` | aws-ecr-repository-wildcard-principal 잠재적 결함 및 보안 이격율 정비 요망. | `security/aws-ecr-repository-wildcard-principal.yaml` |
| `aws-efs-filesystem-encrypted-with-cmk` | `WARNING` | aws-efs-filesystem-encrypted-with-cmk 잠재적 결함 및 보안 이격율 정비 요망. | `security/aws-efs-filesystem-encrypted-with-cmk.yaml` |
| `aws-elasticache-automatic-backup-not-enabled` | `WARNING` | aws-elasticache-automatic-backup-not-enabled 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/aws-elasticache-automatic-backup-not-enabled.yaml` |
| `aws-elasticsearch-insecure-tls-version` | `WARNING` | 보안 옵션 누사 및 예방 단속 필요. | `security/aws-elasticsearch-insecure-tls-version.yaml` |
| `aws-elasticsearch-nodetonode-encryption-not-enabled` | `WARNING` | aws-elasticsearch-nodetonode-encryption-not-enabled 잠재적 결함 및 보안 이격율 정비 요망. | `security/aws-elasticsearch-nodetonode-encryption.yaml` |
| `aws-elb-access-logs-not-enabled` | `WARNING` | aws-elb-access-logs-not-enabled 잠재적 결함 및 보안 이격율 정비 요망. | `security/aws-elb-access-logs-not-enabled.yaml` |
| `aws-emr-encrypted-with-cmk` | `WARNING` | aws-emr-encrypted-with-cmk 잠재적 결함 및 보안 이격율 정비 요망. | `security/aws-emr-encrypted-with-cmk.yaml` |
| `aws-fsx-lustre-filesystem-encrypted-with-cmk` | `WARNING` | aws-fsx-lustre-filesystem-encrypted-with-cmk 잠재적 결함 및 보안 이격율 정비 요망. | `security/aws-fsx-lustre-files-ystem.yaml` |
| `aws-fsx-lustre-filesystem-encrypted-with-cmk` | `WARNING` | aws-fsx-lustre-filesystem-encrypted-with-cmk 잠재적 결함 및 보안 이격율 정비 요망. | `security/aws-fsx-lustre-filesystem-encrypted-with-cmk.yaml` |
| `aws-fsx-ontapfs-encrypted-with-cmk` | `WARNING` | aws-fsx-ontapfs-encrypted-with-cmk 잠재적 결함 및 보안 이격율 정비 요망. | `security/aws-fsx-ontapfs-encrypted-with-cmk.yaml` |
| `aws-fsx-windows-encrypted-with-cmk` | `WARNING` | aws-fsx-windows-encrypted-with-cmk 잠재적 결함 및 보안 이격율 정비 요망. | `security/aws-fsx-windows-encrypted-with-cmk.yaml` |
| `aws-glacier-vault-any-principal` | `ERROR` | IaC 보안 옵션 누사 경보: aws-glacier-vault-any-principal 설정율을 탑재 하십시오. | `security/aws-glacier-vault-any-principal.yaml` |
| `aws-iam-admin-policy` | `ERROR` | IaC 보안 옵션 누사 경보: aws-iam-admin-policy 설정율을 탑재 하십시오. | `security/aws-iam-admin-policy.yaml` |
| `aws-iam-admin-policy-ssoadmin` | `ERROR` | IaC 보안 옵션 누사 경보: aws-iam-admin-policy-ssoadmin 설정율을 탑재 하십시오. | `security/aws-iam-admin-policy-ssoadmin.yaml` |
| `aws-imagebuilder-component-encrypted-with-cmk` | `WARNING` | aws-imagebuilder-component-encrypted-with-cmk 잠재적 결함 및 보안 이격율 정비 요망. | `security/aws-imagebuilder-component-encrypted-with-cmk.yaml` |
| `aws-insecure-api-gateway-tls-version` | `WARNING` | 보안 옵션 누사 및 예방 단속 필요. | `security/aws-insecure-api-gateway-tls-version.yaml` |
| `aws-insecure-cloudfront-distribution-tls-version` | `WARNING` | 보안 옵션 누사 및 예방 단속 필요. | `security/aws-cloudfront-insecure-tls.yaml` |
| `aws-insecure-redshift-ssl-configuration` | `WARNING` | 보안 옵션 누사 및 예방 단속 필요. | `security/aws-insecure-redshift-ssl-configuration.yaml` |
| `aws-kinesis-stream-encrypted-with-cmk` | `WARNING` | aws-kinesis-stream-encrypted-with-cmk 잠재적 결함 및 보안 이격율 정비 요망. | `security/aws-kinesis-stream-encrypted-with-cmk.yaml` |
| `aws-kinesis-stream-unencrypted` | `WARNING` | aws-kinesis-stream-unencrypted 잠재적 결함 및 보안 이격율 정비 요망. | `security/aws-kinesis-stream-unencrypted.yaml` |
| `aws-kinesis-video-stream-encrypted-with-cmk` | `WARNING` | aws-kinesis-video-stream-encrypted-with-cmk 잠재적 결함 및 보안 이격율 정비 요망. | `security/aws-kinesis-video-stream-encrypted-with-cmk.yaml` |
| `aws-kms-key-wildcard-principal` | `ERROR` | Terraform 구성 중 와일드카드(*) 권한 과잉 부여가 식별되었습니다. | `security/aws-kms-key-wildcard-principal.yaml` |
| `aws-kms-no-rotation` | `WARNING` | aws-kms-no-rotation 잠재적 결함 및 보안 이격율 정비 요망. | `security/aws-kms-no-rotation.yaml` |
| `aws-lambda-environment-credentials` | `ERROR` | IaC 보안 옵션 누사 경보: aws-lambda-environment-credentials 설정율을 탑재 하십시오. | `security/aws-lambda-environment-credentials.yaml` |
| `aws-lambda-environment-unencrypted` | `WARNING` | aws-lambda-environment-unencrypted 잠재적 결함 및 보안 이격율 정비 요망. | `security/aws-lambda-environment-unencrypted.yaml` |
| `aws-lambda-permission-unrestricted-source-arn` | `ERROR` | IaC 보안 옵션 누사 경보: aws-lambda-permission-unrestricted-source-arn 설정율을 탑재 하십시오. | `security/aws-lambda-permission-unrestricted-source-arn.yaml` |
| `aws-lambda-x-ray-tracing-not-active` | `INFO` | aws-lambda-x-ray-tracing-not-active 잠재적 결함 및 보안 이격율 정비 요망. | `security/aws-lambda-x-ray-tracing-not-active.yaml` |
| `aws-network-acl-allows-all-ports` | `WARNING` | aws-network-acl-allows-all-ports 잠재적 결함 및 보안 이격율 정비 요망. | `security/aws-network-acl-allows-all-ports.yaml` |
| `aws-network-acl-allows-public-ingress` | `WARNING` | aws-network-acl-allows-public-ingress 잠재적 결함 및 보안 이격율 정비 요망. | `security/aws-network-acl-allows-public-ingress.yaml` |
| `aws-opensearchserverless-encrypted-with-cmk` | `WARNING` | aws-opensearchserverless-encrypted-with-cmk 잠재적 결함 및 보안 이격율 정비 요망. | `security/aws-opensearchserverless-encrypted-with-cmk.yaml` |
| `aws-provider-static-credentials` | `WARNING` | aws-provider-static-credentials 잠재적 결함 및 보안 이격율 정비 요망. | `security/aws-provider-static-credentials.yaml` |
| `aws-provisioner-exec` | `WARNING` | Provisioners are a tool of last resort and should be avoided where possible. Pro... | `security/aws-provisioner-exec.yaml` |
| `aws-qldb-inadequate-ledger-permissions-mode` | `WARNING` | aws-qldb-inadequate-ledger-permissions-mode 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/aws-qldb-inadequate-ledger-permissions-mode.yaml` |
| `aws-rds-backup-no-retention` | `WARNING` | aws-rds-backup-no-retention 잠재적 결함 및 보안 이격율 정비 요망. | `security/aws-rds-backup-no-retention.yaml` |
| `aws-rds-cluster-iam-authentication-not-enabled` | `WARNING` | aws-rds-cluster-iam-authentication-not-enabled 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/aws-rds-cluster-iam-authentication-not-enabled.yaml` |
| `aws-rds-iam-authentication-not-enabled` | `WARNING` | aws-rds-iam-authentication-not-enabled 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/aws-rds-iam-authentication-not-enabled.yaml` |
| `aws-rds-multiaz-not-enabled` | `WARNING` | aws-rds-multiaz-not-enabled 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/aws-rds-multiaz-not-enabled.yaml` |
| `aws-redshift-cluster-encrypted-with-cmk` | `WARNING` | aws-redshift-cluster-encrypted-with-cmk 잠재적 결함 및 보안 이격율 정비 요망. | `security/aws-redshift-cluster-encrypted-with-cmk.yaml` |
| `aws-s3-bucket-object-encrypted-with-cmk` | `WARNING` | aws-s3-bucket-object-encrypted-with-cmk 잠재적 결함 및 보안 이격율 정비 요망. | `security/aws-s3-bucket-object-encrypted-with-cmk.yaml` |
| `aws-s3-bucket-versioning-not-enabled` | `WARNING` | aws-s3-bucket-versioning-not-enabled 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/aws-s3-bucket-versioning-not-enabled.yaml` |
| `aws-s3-object-copy-encrypted-with-cmk` | `WARNING` | aws-s3-object-copy-encrypted-with-cmk 잠재적 결함 및 보안 이격율 정비 요망. | `security/aws-s3-object-copy-encrypted-with-cmk.yaml` |
| `aws-s3-object-lock-not-enabled` | `WARNING` | aws-s3-object-lock-not-enabled 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/aws-s3-object-lock-not-enabled.yaml` |
| `aws-sagemaker-domain-encrypted-with-cmk` | `WARNING` | aws-sagemaker-domain-encrypted-with-cmk 잠재적 결함 및 보안 이격율 정비 요망. | `security/aws-sagemaker-domain-encrypted-with-cmk.yaml` |
| `aws-secretsmanager-secret-unencrypted` | `WARNING` | 자격증명/보안 기밀 문자열 누사 점검. | `security/aws-secretsmanager-secret-unencrypted.yaml` |
| `aws-sns-topic-unencrypted` | `WARNING` | aws-sns-topic-unencrypted 잠재적 결함 및 보안 이격율 정비 요망. | `security/aws-sns-topic-unencrypted.yaml` |
| `aws-sqs-queue-policy-wildcard-action` | `INFO` | aws-sqs-queue-policy-wildcard-action 잠재적 결함 및 보안 이격율 정비 요망. | `security/aws-sqs-queue-policy-wildcard-action.yaml` |
| `aws-sqs-queue-policy-wildcard-principal` | `ERROR` | Terraform 구성 중 와일드카드(*) 권한 과잉 부여가 식별되었습니다. | `security/aws-sqs-queue-policy-wildcard-principal.yaml` |
| `aws-sqs-queue-unencrypted` | `WARNING` | aws-sqs-queue-unencrypted 잠재적 결함 및 보안 이격율 정비 요망. | `security/aws-sqs-queue-unencrypted.yaml` |
| `aws-ssm-document-logging-issues` | `WARNING` | aws-ssm-document-logging-issues 잠재적 결함 및 보안 이격율 정비 요망. | `security/aws-ssm-document-logging-issues.yaml` |
| `aws-subnet-has-public-ip-address` | `WARNING` | aws-subnet-has-public-ip-address 잠재적 결함 및 보안 이격율 정비 요망. | `security/aws-subnet-has-public-ip-address.yaml` |
| `aws-timestream-database-encrypted-with-cmk` | `WARNING` | aws-timestream-database-encrypted-with-cmk 잠재적 결함 및 보안 이격율 정비 요망. | `security/aws-timestream-database-encrypted-with-cmk.yaml` |
| `aws-transfer-server-is-public` | `WARNING` | aws-transfer-server-is-public 잠재적 결함 및 보안 이격율 정비 요망. | `security/aws-transfer-server-is-public.yaml` |
| `aws-workspaces-root-volume-unencrypted` | `WARNING` | aws-workspaces-root-volume-unencrypted 잠재적 결함 및 보안 이격율 정비 요망. | `security/aws-workspaces-root-volume-unencrypted.yaml` |
| `aws-workspaces-user-volume-unencrypted` | `WARNING` | aws-workspaces-user-volume-unencrypted 잠재적 결함 및 보안 이격율 정비 요망. | `security/aws-workspaces-user-volume-unencrypted.yaml` |
| `insecure-load-balancer-tls-version` | `WARNING` | 보안 옵션 누사 및 예방 단속 필요. | `security/insecure-load-balancer-tls-version.yaml` |
| `lambda-permission-logs-missing-arn-asterisk` | `WARNING` | lambda-permission-logs-missing-arn-asterisk IaC 보안 설정 정비 및 예방 조치 요망. | `correctness/lambda-permission-logs-missing-arn-asterisk.yaml` |
| `lambda-redundant-field-with-image` | `WARNING` | lambda-redundant-field-with-image IaC 보안 설정 정비 및 예방 조치 요망. | `correctness/lambda-redundant-field-with-image.yaml` |
| `missing-alb-drop-http-headers` | `WARNING` | missing-alb-drop-http-headers IaC 보안 설정 정비 및 예방 조치 요망. | `best-practice/missing-alb-drop-http-headers.yaml` |
| `missing-api-gateway-cache-cluster` | `WARNING` | missing-api-gateway-cache-cluster IaC 보안 설정 정비 및 예방 조치 요망. | `best-practice/missing-api-gateway-cache-cluster.yaml` |
| `missing-athena-workgroup-encryption` | `WARNING` | missing-athena-workgroup-encryption 잠재적 결함 및 보안 이격율 정비 요망. | `security/missing-athena-workgroup-encryption.yaml` |
| `missing-autoscaling-group-tags` | `WARNING` | missing-autoscaling-group-tags 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/missing-autoscaling-group-tags.yaml` |
| `missing-aws-autoscaling-tags` | `WARNING` | missing-aws-autoscaling-tags 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/missing-aws-autoscaling-tags.yaml` |
| `missing-aws-cross-zone-lb` | `WARNING` | missing-aws-cross-zone-lb 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/missing-aws-cross-zone-lb.yaml` |
| `missing-aws-lb-deletion-protection` | `WARNING` | missing-aws-lb-deletion-protection 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/missing-aws-lb-deletion-protection.yaml` |
| `missing-aws-qldb-deletion-protection` | `WARNING` | missing-aws-qldb-deletion-protection 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/missing-aws-qldb-deletion-protection.yaml` |
| `missing-cloudwatch-log-group-kms-key` | `WARNING` | missing-cloudwatch-log-group-kms-key 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/missing-cloudwatch-log-group-kms-key.yaml` |
| `missing-cloudwatch-log-group-retention` | `WARNING` | missing-cloudwatch-log-group-retention 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/missing-cloudwatch-log-group-retention.yaml` |
| `reserved-aws-lambda-environment-variable` | `WARNING` | reserved-aws-lambda-environment-variable 잠재적 결함 및 보안 이격율 정비 요망. | `correctness/reserved-aws-lambda-environment-variable.yaml` |
| `subscription-filter-missing-depends` | `WARNING` | subscription-filter-missing-depends IaC 보안 설정 정비 및 예방 조치 요망. | `correctness/subscription-filter-missing-depends.yaml` |
| `unrestricted-github-oidc-policy` | `WARNING` | unrestricted-github-oidc-policy 잠재적 결함 및 보안 이격율 정비 요망. | `security/unrestricted-github-oidc-policy.yaml` |
| `wildcard-assume-role` | `ERROR` | Terraform 구성 중 와일드카드(*) 권한 과잉 부여가 식별되었습니다. | `security/wildcard-assume-role.yaml` |

## AZURE

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `appservice-account-identity-registered` | `INFO` | appservice-account-identity-registered 잠재적 결함 및 보안 이격율 정비 요망. | `security/appservice/appservice-account-identity-registered.yaml` |
| `appservice-authentication-enabled` | `ERROR` | IaC 보안 옵션 누사 경보: appservice-authentication-enabled 설정율을 탑재 하십시오. | `security/appservice/appservice-authentication-enabled.yaml` |
| `appservice-enable-http2` | `INFO` | appservice-enable-http2 잠재적 결함 및 보안 이격율 정비 요망. | `security/appservice/appservice-enable-http2.yaml` |
| `appservice-enable-https-only` | `ERROR` | IaC 보안 옵션 누사 경보: appservice-enable-https-only 설정율을 탑재 하십시오. | `security/appservice/appservice-enable-https-only.yaml` |
| `appservice-require-client-cert` | `INFO` | appservice-require-client-cert 잠재적 결함 및 보안 이격율 정비 요망. | `security/appservice/appservice-require-client-cert.yaml` |
| `appservice-use-secure-tls-policy` | `ERROR` | IaC 보안 옵션 누사 경보: appservice-use-secure-tls-policy 설정율을 탑재 하십시오. | `security/appservice/appservice-use-secure-tls-policy.yaml` |
| `azure-ad-used-auth-service-fabric` | `WARNING` | azure-ad-used-auth-service-fabric 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/azure-ad-used-auth-service-fabric.yaml` |
| `azure-aks-apiserver-auth-ip-ranges` | `WARNING` | azure-aks-apiserver-auth-ip-ranges 잠재적 결함 및 보안 이격율 정비 요망. | `security/aks/azure-aks-apiserver-auth-ip-ranges.yaml` |
| `azure-aks-private-clusters-enabled` | `WARNING` | azure-aks-private-clusters-enabled 잠재적 결함 및 보안 이격율 정비 요망. | `security/aks/azure-aks-private-clusters-enabled.yaml` |
| `azure-aks-uses-azure-policies-addon` | `INFO` | azure-aks-uses-azure-policies-addon 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/azure-aks-uses-azure-policies-addon.yaml` |
| `azure-aks-uses-disk-encryptionset` | `WARNING` | azure-aks-uses-disk-encryptionset 잠재적 결함 및 보안 이격율 정비 요망. | `security/aks/azure-aks-uses-disk-encryptionset.yaml` |
| `azure-apiservices-use-virtualnetwork` | `WARNING` | azure-apiservices-use-virtualnetwork 잠재적 결함 및 보안 이격율 정비 요망. | `security/apiservice/azure-apiservices-use-virtualnetwork.yaml` |
| `azure-appgateway-enables-waf` | `WARNING` | azure-appgateway-enables-waf 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/azure-appgateway-enables-waf.yaml` |
| `azure-appservice-auth` | `WARNING` | azure-appservice-auth 잠재적 결함 및 보안 이격율 정비 요망. | `security/appservice/azure-appservice-auth.yaml` |
| `azure-appservice-client-certificate` | `WARNING` | azure-appservice-client-certificate 잠재적 결함 및 보안 이격율 정비 요망. | `security/appservice/azure-appservice-client-certificate.yaml` |
| `azure-appservice-detailed-errormessages-enabled` | `WARNING` | azure-appservice-detailed-errormessages-enabled 잠재적 결함 및 보안 이격율 정비 요망. | `security/appservice/azure-appservice-detailed-errormessages-enabled.yaml` |
| `azure-appservice-disallowed-cors` | `WARNING` | azure-appservice-disallowed-cors 잠재적 결함 및 보안 이격율 정비 요망. | `security/appservice/azure-appservice-disallowed-cors.yaml` |
| `azure-appservice-dotnet-framework-version` | `INFO` | azure-appservice-dotnet-framework-version 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/azure-appservice-dotnet-framework-version.yaml` |
| `azure-appservice-enabled-failed-request` | `WARNING` | azure-appservice-enabled-failed-request 잠재적 결함 및 보안 이격율 정비 요망. | `security/appservice/azure-appservice-enabled-failed-request.yaml` |
| `azure-appservice-ftps-state` | `WARNING` | azure-appservice-ftps-state 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/azure-appservice-ftps-state.yaml` |
| `azure-appservice-http-logging-enabled` | `WARNING` | azure-appservice-http-logging-enabled 잠재적 결함 및 보안 이격율 정비 요망. | `security/appservice/azure-appservice-http-logging-enabled.yaml` |
| `azure-appservice-https-20-enabled` | `WARNING` | azure-appservice-https-20-enabled 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/azure-appservice-https-20-enabled.yaml` |
| `azure-appservice-https-only` | `WARNING` | azure-appservice-https-only 잠재적 결함 및 보안 이격율 정비 요망. | `security/appservice/azure-appservice-https-only.yaml` |
| `azure-appservice-identity` | `WARNING` | azure-appservice-identity 잠재적 결함 및 보안 이격율 정비 요망. | `security/appservice/azure-appservice-identity.yaml` |
| `azure-appservice-identityprovider-enabled` | `WARNING` | azure-appservice-identityprovider-enabled 잠재적 결함 및 보안 이격율 정비 요망. | `security/appservice/azure-appservice-identityprovider-enabled.yaml` |
| `azure-appservice-java-version` | `INFO` | azure-appservice-java-version 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/azure-appservice-java-version.yaml` |
| `azure-appservice-min-tls-version` | `WARNING` | azure-appservice-min-tls-version 잠재적 결함 및 보안 이격율 정비 요망. | `security/appservice/azure-appservice-min-tls-version.yaml` |
| `azure-appservice-php-version` | `INFO` | azure-appservice-php-version 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/azure-appservice-php-version.yaml` |
| `azure-appservice-python-version` | `INFO` | azure-appservice-python-version 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/azure-appservice-python-version.yaml` |
| `azure-appservice-used-azure-files` | `INFO` | azure-appservice-used-azure-files 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/azure-appservice-used-azure-files.yaml` |
| `azure-automation-encrypted` | `WARNING` | azure-automation-encrypted 잠재적 결함 및 보안 이격율 정비 요망. | `security/azure-automation-encrypted.yaml` |
| `azure-batchaccount-uses-keyvault-encrpytion` | `WARNING` | azure-batchaccount-uses-keyvault-encrpytion 잠재적 결함 및 보안 이격율 정비 요망. | `security/azure-batchaccount-uses-keyvault-encrpytion.yaml` |
| `azure-cognitiveservices-disables-public-network` | `WARNING` | azure-cognitiveservices-disables-public-network 잠재적 결함 및 보안 이격율 정비 요망. | `security/azure-cognitiveservices-disables-public-network.yaml` |
| `azure-containergroup-deployed-into-virtualnetwork` | `WARNING` | azure-containergroup-deployed-into-virtualnetwork 잠재적 결함 및 보안 이격율 정비 요망. | `security/azure-containergroup-deployed-into-virtualnetwork.yaml` |
| `azure-cosmosdb-accounts-restricted-access` | `WARNING` | azure-cosmosdb-accounts-restricted-access 잠재적 결함 및 보안 이격율 정비 요망. | `security/azure-cosmosdb-accounts-restricted-access.yaml` |
| `azure-cosmosdb-disable-access-key-write` | `WARNING` | azure-cosmosdb-disable-access-key-write 잠재적 결함 및 보안 이격율 정비 요망. | `security/azure-cosmosdb-disable-access-key-write.yaml` |
| `azure-cosmosdb-disables-public-network` | `WARNING` | azure-cosmosdb-disables-public-network 잠재적 결함 및 보안 이격율 정비 요망. | `security/azure-cosmosdb-disables-public-network.yaml` |
| `azure-cosmosdb-have-cmk` | `WARNING` | azure-cosmosdb-have-cmk 잠재적 결함 및 보안 이격율 정비 요망. | `security/azure-cosmosdb-have-cmk.yaml` |
| `azure-customrole-definition-subscription-owner` | `WARNING` | azure-customrole-definition-subscription-owner 잠재적 결함 및 보안 이격율 정비 요망. | `security/azure-customrole-definition-subscription-owner.yaml` |
| `azure-dataexplorer-double-encryption-enabled` | `WARNING` | azure-dataexplorer-double-encryption-enabled 잠재적 결함 및 보안 이격율 정비 요망. | `security/azure-dataexplorer-double-encryption-enabled.yaml` |
| `azure-dataexplorer-uses-disk-encryption` | `WARNING` | azure-dataexplorer-uses-disk-encryption 잠재적 결함 및 보안 이격율 정비 요망. | `security/azure-dataexplorer-uses-disk-encryption.yaml` |
| `azure-datafactory-no-public-network-access` | `WARNING` | azure-datafactory-no-public-network-access 잠재적 결함 및 보안 이격율 정비 요망. | `security/azure-datafactory-no-public-network-access.yaml` |
| `azure-datafactory-uses-git-repository` | `WARNING` | azure-datafactory-uses-git-repository 잠재적 결함 및 보안 이격율 정비 요망. | `security/azure-datafactory-uses-git-repository.yaml` |
| `azure-datalake-store-encryption` | `WARNING` | azure-datalake-store-encryption 잠재적 결함 및 보안 이격율 정비 요망. | `security/azure-datalake-store-encryption.yaml` |
| `azure-defenderon-appservices` | `WARNING` | azure-defenderon-appservices 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/azure-defenderon-appservices.yaml` |
| `azure-defenderon-container-registry` | `WARNING` | azure-defenderon-container-registry 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/azure-defenderon-container-registry.yaml` |
| `azure-defenderon-keyvaults` | `WARNING` | azure-defenderon-keyvaults 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/azure-defenderon-keyvaults.yaml` |
| `azure-defenderon-kubernetes` | `WARNING` | azure-defenderon-kubernetes 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/azure-defenderon-kubernetes.yaml` |
| `azure-defenderon-servers` | `WARNING` | azure-defenderon-servers 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/azure-defenderon-servers.yaml` |
| `azure-defenderon-sqlservers` | `WARNING` | azure-defenderon-sqlservers 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/azure-defenderon-sqlservers.yaml` |
| `azure-defenderon-sqlservers-vms` | `WARNING` | azure-defenderon-sqlservers-vms 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/azure-defenderon-sqlservers-vms.yaml` |
| `azure-defenderon-storage` | `WARNING` | azure-defenderon-storage 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/azure-defenderon-storage.yaml` |
| `azure-eventgrid-domain-network-access` | `WARNING` | azure-eventgrid-domain-network-access 잠재적 결함 및 보안 이격율 정비 요망. | `security/azure-eventgrid-domain-network-access.yaml` |
| `azure-frontdoor-enables-waf` | `WARNING` | azure-frontdoor-enables-waf 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/azure-frontdoor-enables-waf.yaml` |
| `azure-frontdoor-use-wafmode` | `WARNING` | azure-frontdoor-use-wafmode 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/azure-frontdoor-use-wafmode.yaml` |
| `azure-functionapp-disallow-cors` | `WARNING` | azure-functionapp-disallow-cors 잠재적 결함 및 보안 이격율 정비 요망. | `security/azure-functionapp-disallow-cors.yaml` |
| `azure-functionapp-http-version-latest` | `WARNING` | azure-functionapp-http-version-latest 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/azure-functionapp-http-version-latest.yaml` |
| `azure-functionapps-accessible-over-https` | `WARNING` | azure-functionapps-accessible-over-https 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/azure-functionapps-accessible-over-https.yaml` |
| `azure-functionapps-enable-auth` | `WARNING` | azure-functionapps-enable-auth 잠재적 결함 및 보안 이격율 정비 요망. | `security/azure-functionapps-enable-auth.yaml` |
| `azure-instance-extensions` | `WARNING` | azure-instance-extensions 잠재적 결함 및 보안 이격율 정비 요망. | `security/azure-instance-extensions.yaml` |
| `azure-iot-no-public-network-access` | `WARNING` | azure-iot-no-public-network-access 잠재적 결함 및 보안 이격율 정비 요망. | `security/azure-iot-no-public-network-access.yaml` |
| `azure-key-backedby-hsm` | `WARNING` | azure-key-backedby-hsm 잠재적 결함 및 보안 이격율 정비 요망. | `security/azure-key-backedby-hsm.yaml` |
| `azure-key-no-expiration-date` | `WARNING` | azure-key-no-expiration-date 잠재적 결함 및 보안 이격율 정비 요망. | `security/azure-key-no-expiration-date.yaml` |
| `azure-keyvault-enables-firewall-rules-settings` | `WARNING` | azure-keyvault-enables-firewall-rules-settings 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/azure-keyvault-enables-firewall-rules-settings.yaml` |
| `azure-keyvault-enables-purge-protection` | `WARNING` | azure-keyvault-enables-purge-protection 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/azure-keyvault-enables-purge-protection.yaml` |
| `azure-keyvault-enables-soft-delete` | `WARNING` | azure-keyvault-enables-soft-delete 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/azure-keyvault-enables-soft-delete.yaml` |
| `azure-keyvault-recovery-enabled` | `WARNING` | azure-keyvault-recovery-enabled 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/azure-keyvault-recovery-enabled.yaml` |
| `azure-managed-disk-encryption` | `WARNING` | azure-managed-disk-encryption 잠재적 결함 및 보안 이격율 정비 요망. | `security/azure-managed-disk-encryption.yaml` |
| `azure-managed-disk-encryption-set` | `WARNING` | azure-managed-disk-encryption-set 잠재적 결함 및 보안 이격율 정비 요망. | `security/azure-managed-disk-encryption-set.yaml` |
| `azure-mariadb-geo-backup-enabled` | `WARNING` | azure-mariadb-geo-backup-enabled 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/azure-mariadb-geo-backup-enabled.yaml` |
| `azure-mariadb-public-access-disabled` | `WARNING` | azure-mariadb-public-access-disabled 잠재적 결함 및 보안 이격율 정비 요망. | `security/azure-mariadb-public-access-disabled.yaml` |
| `azure-mariadb-sslenforcement-enabled` | `WARNING` | azure-mariadb-sslenforcement-enabled 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/azure-mariadb-sslenforcement-enabled.yaml` |
| `azure-monitor-log-profile-categories` | `WARNING` | azure-monitor-log-profile-categories 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/azure-monitor-log-profile-categories.yaml` |
| `azure-monitor-log-profile-retention-days` | `WARNING` | azure-monitor-log-profile-retention-days 잠재적 결함 및 보안 이격율 정비 요망. | `security/azure-monitor-log-profile-retention-days.yaml` |
| `azure-monitor-log-profile-retention-days` | `WARNING` | azure-monitor-log-profile-retention-days 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/azure-monitor-log-profile-retention-days.yaml` |
| `azure-mssql-service-mintls-version` | `WARNING` | azure-mssql-service-mintls-version 잠재적 결함 및 보안 이격율 정비 요망. | `security/azure-mssql-service-mintls-version.yaml` |
| `azure-mysql-encryption-enabled` | `WARNING` | azure-mysql-encryption-enabled 잠재적 결함 및 보안 이격율 정비 요망. | `security/azure-mysql-encryption-enabled.yaml` |
| `azure-mysql-geo-backup-enabled` | `WARNING` | azure-mysql-geo-backup-enabled 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/azure-mysql-geo-backup-enabled.yaml` |
| `azure-mysql-mintls-version` | `WARNING` | azure-mysql-mintls-version 잠재적 결함 및 보안 이격율 정비 요망. | `security/azure-mysql-mintls-version.yaml` |
| `azure-mysql-public-access-disabled` | `WARNING` | azure-mysql-public-access-disabled 잠재적 결함 및 보안 이격율 정비 요망. | `security/azure-mysql-public-access-disabled.yaml` |
| `azure-mysql-server-tlsenforcement-enabled` | `WARNING` | azure-mysql-server-tlsenforcement-enabled 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/azure-mysql-server-tlsenforcement-enabled.yaml` |
| `azure-mysql-threat-detection-enabled` | `WARNING` | azure-mysql-threat-detection-enabled 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/azure-mysql-threat-detection-enabled.yaml` |
| `azure-network-watcher-flowlog-period` | `WARNING` | azure-network-watcher-flowlog-period 잠재적 결함 및 보안 이격율 정비 요망. | `security/azure-network-watcher-flowlog-period.yaml` |
| `azure-networkinterface-enable-ip-forwarding` | `WARNING` | azure-networkinterface-enable-ip-forwarding 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/azure-networkinterface-enable-ip-forwarding.yaml` |
| `azure-postgresql-encryption-enabled` | `WARNING` | azure-postgresql-encryption-enabled 잠재적 결함 및 보안 이격율 정비 요망. | `security/azure-postgresql-encryption-enabled.yaml` |
| `azure-postgresql-flexi-server-geo-backup-enabled` | `WARNING` | azure-postgresql-flexi-server-geo-backup-enabled 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/azure-postgresql-flexi-server-geo-backup-enabled.yaml` |
| `azure-postgresql-geo-backup-enabled` | `WARNING` | azure-postgresql-geo-backup-enabled 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/azure-postgresql-geo-backup-enabled.yaml` |
| `azure-postgresql-min-tls-version` | `WARNING` | azure-postgresql-min-tls-version 잠재적 결함 및 보안 이격율 정비 요망. | `security/azure-postgresql-min-tls-version.yaml` |
| `azure-postgresql-server-connection-throttling-enabled` | `WARNING` | azure-postgresql-server-connection-throttling-enabled 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/azure-postgresql-server-connection-throttling-enabled.yaml` |
| `azure-postgresql-server-log-checkpoint-enabled` | `WARNING` | azure-postgresql-server-log-checkpoint-enabled 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/azure-postgresql-server-log-checkpoint-enabled.yaml` |
| `azure-postgresql-server-log-connections-enabled` | `WARNING` | azure-postgresql-server-log-connections-enabled 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/azure-postgresql-server-log-connections-enabled.yaml` |
| `azure-postgresql-server-public-access-disabled` | `WARNING` | azure-postgresql-server-public-access-disabled 잠재적 결함 및 보안 이격율 정비 요망. | `security/azure-postgresql-server-public-access-disabled.yaml` |
| `azure-postgresql-ssl-enforcement-enabled` | `WARNING` | azure-postgresql-ssl-enforcement-enabled 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/azure-postgresql-ssl-enforcement-enabled.yaml` |
| `azure-postgresql-threat-detection-enabled` | `WARNING` | azure-postgresql-threat-detection-enabled 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/azure-postgresql-threat-detection-enabled.yaml` |
| `azure-redis-cache-enable-non-ssl-port` | `WARNING` | azure-redis-cache-enable-non-ssl-port 잠재적 결함 및 보안 이격율 정비 요망. | `security/azure-redis-cache-enable-non-ssl-port.yaml` |
| `azure-redis-cache-public-network-access-enabled` | `WARNING` | azure-redis-cache-public-network-access-enabled 잠재적 결함 및 보안 이격율 정비 요망. | `security/azure-redis-cache-public-network-access-enabled.yaml` |
| `azure-remote-debugging-not-enabled` | `WARNING` | azure-remote-debugging-not-enabled 잠재적 결함 및 보안 이격율 정비 요망. | `security/azure-remote-debugging-not-enabled.yaml` |
| `azure-scale-set-password` | `WARNING` | azure-scale-set-password 잠재적 결함 및 보안 이격율 정비 요망. | `security/azure-scale-set-password.yaml` |
| `azure-search-publicnetwork-access-disabled` | `WARNING` | azure-search-publicnetwork-access-disabled 잠재적 결함 및 보안 이격율 정비 요망. | `security/azure-search-publicnetwork-access-disabled.yaml` |
| `azure-secret-content-type` | `WARNING` | 자격증명/보안 기밀 문자열 누사 점검. | `best-practice/azure-secret-content-type.yaml` |
| `azure-secret-expiration-date` | `WARNING` | 자격증명/보안 기밀 문자열 누사 점검. | `best-practice/azure-secret-expiration-date.yaml` |
| `azure-securitcenter-email-alert` | `WARNING` | azure-securitcenter-email-alert 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/azure-securitcenter-email-alert.yaml` |
| `azure-securitycenter-contact-emails` | `WARNING` | azure-securitycenter-contact-emails 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/azure-securitycenter-contact-emails.yaml` |
| `azure-securitycenter-contact-phone` | `WARNING` | azure-securitycenter-contact-phone 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/azure-securitycenter-contact-phone.yaml` |
| `azure-securitycenter-email-alert-admins` | `WARNING` | azure-securitycenter-email-alert-admins 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/azure-securitycenter-email-alert-admins.yaml` |
| `azure-securitycenter-standard-pricing` | `WARNING` | azure-securitycenter-standard-pricing 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/azure-securitycenter-standard-pricing.yaml` |
| `azure-service-fabric-cluster-protection-level` | `WARNING` | azure-service-fabric-cluster-protection-level 잠재적 결함 및 보안 이격율 정비 요망. | `security/azure-service-fabric-cluster-protection-level.yaml` |
| `azure-sqlserver-email-alerts-enabled` | `WARNING` | azure-sqlserver-email-alerts-enabled 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/azure-sqlserver-email-alerts-enabled.yaml` |
| `azure-sqlserver-email-alerts-toadmins-enabled` | `WARNING` | azure-sqlserver-email-alerts-toadmins-enabled 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/azure-sqlserver-email-alerts-toadmins-enabled.yaml` |
| `azure-sqlserver-no-public-access` | `WARNING` | azure-sqlserver-no-public-access 잠재적 결함 및 보안 이격율 정비 요망. | `security/azure-sqlserver-no-public-access.yaml` |
| `azure-sqlserver-public-access-disabled` | `WARNING` | azure-sqlserver-public-access-disabled 잠재적 결함 및 보안 이격율 정비 요망. | `security/azure-sqlserver-public-access-disabled.yaml` |
| `azure-sqlserver-threat-detection-types` | `WARNING` | azure-sqlserver-threat-detection-types 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/azure-sqlserver-threat-detection-types.yaml` |
| `azure-storage-account-disable-public-access` | `WARNING` | azure-storage-account-disable-public-access 잠재적 결함 및 보안 이격율 정비 요망. | `security/azure-storage-account-disable-public-access.yaml` |
| `azure-storage-account-enables-secure-transfer` | `WARNING` | azure-storage-account-enables-secure-transfer 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/azure-storage-account-enables-secure-transfer.yaml` |
| `azure-storage-account-minimum-tlsversion` | `WARNING` | azure-storage-account-minimum-tlsversion 잠재적 결함 및 보안 이격율 정비 요망. | `security/azure-storage-account-minimum-tlsversion.yaml` |
| `azure-storage-blob-service-container-private-access` | `WARNING` | azure-storage-blob-service-container-private-access 잠재적 결함 및 보안 이격율 정비 요망. | `security/azure-storage-blob-service-container-private-access.yaml` |
| `azure-storage-sync-public-access-disabled` | `WARNING` | azure-storage-sync-public-access-disabled 잠재적 결함 및 보안 이격율 정비 요망. | `security/azure-storage-sync-public-access-disabled.yaml` |
| `azure-synapse-workscape-enables-managed-virtual-network` | `WARNING` | azure-synapse-workscape-enables-managed-virtual-network 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/azure-synapse-workscape-enables-managed-virtual-network.yaml` |
| `azure-vmencryption-at-host-enabled` | `WARNING` | azure-vmencryption-at-host-enabled 잠재적 결함 및 보안 이격율 정비 요망. | `security/azure-vmencryption-at-host-enabled.yaml` |
| `azure-vmscale-sets-auto-os-image-patching-enabled` | `WARNING` | azure-vmscale-sets-auto-os-image-patching-enabled 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/azure-vmscale-sets-auto-os-image-patching-enabled.yaml` |
| `azure-waf-specificed-mode-app-gw` | `WARNING` | azure-waf-specificed-mode-app-gw 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/azure-waf-specificed-mode-app-gw.yaml` |
| `functionapp-authentication-enabled` | `INFO` | functionapp-authentication-enabled 잠재적 결함 및 보안 이격율 정비 요망. | `security/functionapp/functionapp-authentication-enabled.yaml` |
| `functionapp-enable-http2` | `INFO` | functionapp-enable-http2 잠재적 결함 및 보안 이격율 정비 요망. | `security/functionapp/functionapp-enable-http2.yaml` |
| `keyvault-content-type-for-secret` | `INFO` | 자격증명/보안 기밀 문자열 누사 점검. | `security/keyvault/keyvault-content-type-for-secret.yaml` |
| `keyvault-ensure-key-expires` | `INFO` | keyvault-ensure-key-expires 잠재적 결함 및 보안 이격율 정비 요망. | `security/keyvault/keyvault-ensure-key-expires.yaml` |
| `keyvault-ensure-secret-expires` | `INFO` | 자격증명/보안 기밀 문자열 누사 점검. | `security/keyvault/keyvault-ensure-secret-expires.yaml` |
| `keyvault-purge-enabled` | `WARNING` | keyvault-purge-enabled 잠재적 결함 및 보안 이격율 정비 요망. | `security/keyvault/keyvault-purge-enabled.yaml` |
| `keyvault-specify-network-acl` | `ERROR` | IaC 보안 옵션 누사 경보: keyvault-specify-network-acl 설정율을 탑재 하십시오. | `security/keyvault/keyvault-specify-network-acl.yaml` |
| `storage-allow-microsoft-service-bypass` | `WARNING` | storage-allow-microsoft-service-bypass 잠재적 결함 및 보안 이격율 정비 요망. | `security/storage/storage-allow-microsoft-service-bypass.yaml` |
| `storage-default-action-deny` | `ERROR` | IaC 보안 옵션 누사 경보: storage-default-action-deny 설정율을 탑재 하십시오. | `security/storage/storage-default-action-deny.yaml` |
| `storage-enforce-https` | `WARNING` | storage-enforce-https 잠재적 결함 및 보안 이격율 정비 요망. | `security/storage/storage-enforce-https.yaml` |
| `storage-queue-services-logging` | `WARNING` | storage-queue-services-logging 잠재적 결함 및 보안 이격율 정비 요망. | `security/storage/storage-queue-services-logging.yaml` |
| `storage-use-secure-tls-policy` | `ERROR` | IaC 보안 옵션 누사 경보: storage-use-secure-tls-policy 설정율을 탑재 하십시오. | `security/storage/storage-use-secure-tls-policy.yaml` |

## GCP

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `gcp-artifact-registry-encrypted-with-cmk` | `WARNING` | gcp-artifact-registry-encrypted-with-cmk 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-artifact-registry-encrypted-with-cmk.yaml` |
| `gcp-artifact-registry-private-repo-iam-binding` | `WARNING` | gcp-artifact-registry-private-repo-iam-binding 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-artifact-registry-private-repo-iam-binding.yaml` |
| `gcp-artifact-registry-private-repo-iam-member` | `WARNING` | gcp-artifact-registry-private-repo-iam-member 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-artifact-registry-private-repo-iam-member.yaml` |
| `gcp-bigquery-dataset-encrypted-with-cmk` | `WARNING` | gcp-bigquery-dataset-encrypted-with-cmk 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-bigquery-dataset-encrypted-with-cmk.yaml` |
| `gcp-bigquery-private-table-iam-binding` | `WARNING` | gcp-bigquery-private-table-iam-binding 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-bigquery-private-table-iam-binding.yaml` |
| `gcp-bigquery-private-table-iam-member` | `WARNING` | gcp-bigquery-private-table-iam-member 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-bigquery-private-table-iam-member.yaml` |
| `gcp-bigquery-table-encrypted-with-cmk` | `WARNING` | gcp-bigquery-table-encrypted-with-cmk 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-bigquery-table-encrypted-with-cmk.yaml` |
| `gcp-bigtable-instance-encrypted-with-cmk` | `WARNING` | gcp-bigtable-instance-encrypted-with-cmk 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-bigtable-instance-encrypted-with-cmk.yaml` |
| `gcp-build-workers-private` | `WARNING` | gcp-build-workers-private 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-build-workers-private.yaml` |
| `gcp-cloud-storage-logging` | `WARNING` | gcp-cloud-storage-logging 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-cloud-storage-logging.yaml` |
| `gcp-compute-boot-disk-encryption` | `WARNING` | gcp-compute-boot-disk-encryption 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-compute-boot-disk-encryption.yaml` |
| `gcp-compute-disk-encryption` | `WARNING` | gcp-compute-disk-encryption 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-compute-disk-encryption.yaml` |
| `gcp-compute-firewall-unrestricted-ingress-20` | `WARNING` | gcp-compute-firewall-unrestricted-ingress-20 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-compute-firewall-unrestricted-ingress-20.yaml` |
| `gcp-compute-firewall-unrestricted-ingress-21` | `WARNING` | gcp-compute-firewall-unrestricted-ingress-21 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-compute-firewall-unrestricted-ingress-21.yaml` |
| `gcp-compute-firewall-unrestricted-ingress-22` | `WARNING` | gcp-compute-firewall-unrestricted-ingress-22 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-compute-firewall-unrestricted-ingress-22.yaml` |
| `gcp-compute-firewall-unrestricted-ingress-3306` | `WARNING` | gcp-compute-firewall-unrestricted-ingress-3306 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-compute-firewall-unrestricted-ingress-3306.yaml` |
| `gcp-compute-firewall-unrestricted-ingress-3389` | `WARNING` | gcp-compute-firewall-unrestricted-ingress-3389 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-compute-firewall-unrestricted-ingress-3389.yaml` |
| `gcp-compute-firewall-unrestricted-ingress-80` | `WARNING` | gcp-compute-firewall-unrestricted-ingress-80 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-compute-firewall-unrestricted-ingress-80.yaml` |
| `gcp-compute-ip-forward` | `INFO` | gcp-compute-ip-forward 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-compute-ip-forward.yaml` |
| `gcp-compute-os-login` | `WARNING` | gcp-compute-os-login 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-compute-os-login.yaml` |
| `gcp-compute-project-os-login` | `WARNING` | gcp-compute-project-os-login 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-compute-project-os-login.yaml` |
| `gcp-compute-public-ip` | `WARNING` | gcp-compute-public-ip 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-compute-public-ip.yaml` |
| `gcp-compute-serial-ports` | `WARNING` | gcp-compute-serial-ports 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-compute-serial-ports.yaml` |
| `gcp-compute-shielded-vm` | `WARNING` | gcp-compute-shielded-vm 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/gcp-compute-shielded-vm.yaml` |
| `gcp-compute-ssl-policy` | `WARNING` | gcp-compute-ssl-policy 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-compute-ssl-policy.yaml` |
| `gcp-compute-template-ip-forward` | `INFO` | gcp-compute-template-ip-forward 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-compute-template-ip-forward.yaml` |
| `gcp-compute-template-public-ip` | `WARNING` | gcp-compute-template-public-ip 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-compute-template-public-ip.yaml` |
| `gcp-compute-template-shielded-vm` | `WARNING` | gcp-compute-template-shielded-vm 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/gcp-compute-template-shielded-vm.yaml` |
| `gcp-dataflow-job-encrypted-with-cmk` | `WARNING` | gcp-dataflow-job-encrypted-with-cmk 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-dataflow-job-encrypted-with-cmk.yaml` |
| `gcp-dataflow-private-job` | `WARNING` | gcp-dataflow-private-job 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-dataflow-private-job.yaml` |
| `gcp-datafusion-private-instance` | `WARNING` | gcp-datafusion-private-instance 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-datafusion-private-instance.yaml` |
| `gcp-datafusion-stack-driver-logging` | `WARNING` | gcp-datafusion-stack-driver-logging 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-datafusion-stack-driver-logging.yaml` |
| `gcp-datafusion-stack-driver-monitoring` | `WARNING` | gcp-datafusion-stack-driver-monitoring 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-datafusion-stack-driver-monitoring.yaml` |
| `gcp-dataproc-cluster-encrypted-with-cmk` | `WARNING` | gcp-dataproc-cluster-encrypted-with-cmk 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-dataproc-cluster-encrypted-with-cmk.yaml` |
| `gcp-dataproc-cluster-public-ip` | `WARNING` | gcp-dataproc-cluster-public-ip 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-dataproc-cluster-public-ip.yaml` |
| `gcp-dataproc-private-cluster-iam-binding` | `WARNING` | gcp-dataproc-private-cluster-iam-binding 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-dataproc-private-cluster-iam-binding.yaml` |
| `gcp-dataproc-private-cluster-iam-member` | `WARNING` | gcp-dataproc-private-cluster-iam-member 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-dataproc-private-cluster-iam-member.yaml` |
| `gcp-dns-key-specs-rsasha1` | `WARNING` | gcp-dns-key-specs-rsasha1 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-dns-key-specs-rsasha1.yaml` |
| `gcp-dnssec-enabled` | `WARNING` | gcp-dnssec-enabled 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/gcp-dnssec-enabled.yaml` |
| `gcp-folder-impersonation-roles-iam-binding` | `WARNING` | gcp-folder-impersonation-roles-iam-binding 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-folder-impersonation-roles-iam-binding.yaml` |
| `gcp-folder-impersonation-roles-iam-member` | `WARNING` | gcp-folder-impersonation-roles-iam-member 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-folder-impersonation-roles-iam-member.yaml` |
| `gcp-folder-member-default-service-account-iam-binding` | `WARNING` | gcp-folder-member-default-service-account-iam-binding 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-folder-member-default-service-account-iam-binding.yaml` |
| `gcp-folder-member-default-service-account-iam-member` | `WARNING` | gcp-folder-member-default-service-account-iam-member 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-folder-member-default-service-account-iam-member.yaml` |
| `gcp-gke-alias-ip-enabled` | `WARNING` | gcp-gke-alias-ip-enabled 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/gcp-gke-alias-ip-enabled.yaml` |
| `gcp-gke-basic-auth` | `WARNING` | gcp-gke-basic-auth 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-gke-basic-auth.yaml` |
| `gcp-gke-binary-authorization` | `WARNING` | gcp-gke-binary-authorization 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/gcp-gke-binary-authorization.yaml` |
| `gcp-gke-client-certificate-disabled` | `WARNING` | gcp-gke-client-certificate-disabled 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-gke-client-certificate-disabled.yaml` |
| `gcp-gke-cluster-logging` | `WARNING` | gcp-gke-cluster-logging 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-gke-cluster-logging.yaml` |
| `gcp-gke-enable-shielded-nodes` | `WARNING` | gcp-gke-enable-shielded-nodes 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/gcp-gke-enable-shielded-nodes.yaml` |
| `gcp-gke-enabled-vpc-flow-logs` | `WARNING` | gcp-gke-enabled-vpc-flow-logs 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-gke-enabled-vpc-flow-logs.yaml` |
| `gcp-gke-ensure-integrity-monitoring` | `WARNING` | gcp-gke-ensure-integrity-monitoring 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-gke-ensure-integrity-monitoring.yaml` |
| `gcp-gke-has-labels` | `WARNING` | gcp-gke-has-labels 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/gcp-gke-has-labels.yaml` |
| `gcp-gke-kubernetes-rbac-google-groups` | `WARNING` | gcp-gke-kubernetes-rbac-google-groups 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-gke-kubernetes-rbac-google-groups.yaml` |
| `gcp-gke-legacy-auth-enabled` | `WARNING` | gcp-gke-legacy-auth-enabled 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-gke-legacy-auth-enabled.yaml` |
| `gcp-gke-legacy-instance-metadata-disabled` | `WARNING` | gcp-gke-legacy-instance-metadata-disabled 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-gke-legacy-instance-metadata-disabled.yaml` |
| `gcp-gke-master-authz-networks-enabled` | `WARNING` | gcp-gke-master-authz-networks-enabled 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-gke-master-authz-networks-enabled.yaml` |
| `gcp-gke-metadata-server-enabled` | `WARNING` | gcp-gke-metadata-server-enabled 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/gcp-gke-metadata-server-enabled.yaml` |
| `gcp-gke-monitoring-enabled` | `WARNING` | gcp-gke-monitoring-enabled 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-gke-monitoring-enabled.yaml` |
| `gcp-gke-network-policy-enabled` | `WARNING` | gcp-gke-network-policy-enabled 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-gke-network-policy-enabled.yaml` |
| `gcp-gke-nodepool-auto-repair-enabled` | `WARNING` | gcp-gke-nodepool-auto-repair-enabled 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/gcp-gke-nodepool-auto-repair-enabled.yaml` |
| `gcp-gke-nodepool-auto-upgrade-enabled` | `WARNING` | gcp-gke-nodepool-auto-upgrade-enabled 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/gcp-gke-nodepool-auto-upgrade-enabled.yaml` |
| `gcp-gke-nodepool-integrity-monitoring` | `WARNING` | gcp-gke-nodepool-integrity-monitoring 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-gke-nodepool-integrity-monitoring.yaml` |
| `gcp-gke-nodepool-metadata-server-enabled` | `WARNING` | gcp-gke-nodepool-metadata-server-enabled 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/gcp-gke-nodepool-metadata-server-enabled.yaml` |
| `gcp-gke-nodepool-secure-boot-for-shielded-nodes` | `WARNING` | gcp-gke-nodepool-secure-boot-for-shielded-nodes 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/gcp-gke-nodepool-secure-boot-for-shielded-nodes.yaml` |
| `gcp-gke-pod-security-policy-enabled` | `WARNING` | gcp-gke-pod-security-policy-enabled 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-gke-pod-security-policy-enabled.yaml` |
| `gcp-gke-private-cluster-config` | `WARNING` | gcp-gke-private-cluster-config 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-gke-private-cluster-config.yaml` |
| `gcp-gke-public-control-plane` | `WARNING` | gcp-gke-public-control-plane 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-gke-public-control-plane.yaml` |
| `gcp-gke-secure-boot-for-shielded-nodes` | `WARNING` | gcp-gke-secure-boot-for-shielded-nodes 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-gke-secure-boot-for-shielded-nodes.yaml` |
| `gcp-gke-sql-backup-configuration-enabled` | `WARNING` | gcp-gke-sql-backup-configuration-enabled 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/gcp-gke-sql-backup-configuration-enabled.yaml` |
| `gcp-gke-use-cos-image` | `WARNING` | gcp-gke-use-cos-image 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/gcp-gke-use-cos-image.yaml` |
| `gcp-insecure-load-balancer-tls-version` | `WARNING` | 보안 옵션 누사 및 예방 단속 필요. | `security/gcp-insecure-load-balancer-tls-version.yaml` |
| `gcp-ipv6-private-google-enabled` | `WARNING` | gcp-ipv6-private-google-enabled 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/gcp-ipv6-private-google-enabled.yaml` |
| `gcp-kms-prevent-destroy` | `WARNING` | gcp-kms-prevent-destroy 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-kms-prevent-destroy.yaml` |
| `gcp-memory-store-for-redis-auth-enabled` | `WARNING` | gcp-memory-store-for-redis-auth-enabled 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-memory-store-for-redis-auth-enabled.yaml` |
| `gcp-memory-store-for-redis-intransit-encryption` | `WARNING` | gcp-memory-store-for-redis-intransit-encryption 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-memory-store-for-redis-intransit-encryption.yaml` |
| `gcp-mysql-local-in-file-off` | `WARNING` | gcp-mysql-local-in-file-off 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/gcp-mysql-local-in-file-off.yaml` |
| `gcp-org-impersonation-roles-iam-binding` | `WARNING` | gcp-org-impersonation-roles-iam-binding 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-org-impersonation-roles-iam-binding.yaml` |
| `gcp-org-impersonation-roles-iam-member` | `WARNING` | gcp-org-impersonation-roles-iam-member 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-org-impersonation-roles-iam-member.yaml` |
| `gcp-org-member-default-service-account-iam-binding` | `WARNING` | gcp-org-member-default-service-account-iam-binding 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-org-member-default-service-account-iam-binding.yaml` |
| `gcp-org-member-default-service-account-iam-member` | `WARNING` | gcp-org-member-default-service-account-iam-member 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-org-member-default-service-account-iam-member.yaml` |
| `gcp-postgresql-log-checkpoints` | `WARNING` | gcp-postgresql-log-checkpoints 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/gcp-postgresql-log-checkpoints.yaml` |
| `gcp-postgresql-log-connection` | `WARNING` | gcp-postgresql-log-connection 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/gcp-postgresql-log-connection.yaml` |
| `gcp-postgresql-log-disconnection` | `WARNING` | gcp-postgresql-log-disconnection 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/gcp-postgresql-log-disconnection.yaml` |
| `gcp-postgresql-log-lock-waits` | `WARNING` | gcp-postgresql-log-lock-waits 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/gcp-postgresql-log-lock-waits.yaml` |
| `gcp-postgresql-log-min-duration` | `WARNING` | gcp-postgresql-log-min-duration 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/gcp-postgresql-log-min-duration.yaml` |
| `gcp-postgresql-log-min-message` | `WARNING` | gcp-postgresql-log-min-message 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/gcp-postgresql-log-min-message.yaml` |
| `gcp-postgresql-log-temp` | `WARNING` | gcp-postgresql-log-temp 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/gcp-postgresql-log-temp.yaml` |
| `gcp-project-default-network` | `WARNING` | gcp-project-default-network 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-project-default-network.yaml` |
| `gcp-project-member-default-service-account-iam-binding` | `WARNING` | gcp-project-member-default-service-account-iam-binding 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-project-member-default-service-account-iam-binding.yaml` |
| `gcp-project-member-default-service-account-iam-member` | `WARNING` | gcp-project-member-default-service-account-iam-member 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-project-member-default-service-account-iam-member.yaml` |
| `gcp-project-service-account-user-iam-binding` | `WARNING` | gcp-project-service-account-user-iam-binding 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-project-service-account-user-iam-binding.yaml` |
| `gcp-project-service-account-user-iam-member` | `WARNING` | gcp-project-service-account-user-iam-member 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-project-service-account-user-iam-member.yaml` |
| `gcp-pubsub-encrypted-with-cmk` | `WARNING` | gcp-pubsub-encrypted-with-cmk 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-pubsub-encrypted-with-cmk.yaml` |
| `gcp-pubsub-private-topic-iam-binding` | `WARNING` | gcp-pubsub-private-topic-iam-binding 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-pubsub-private-topic-iam-binding.yaml` |
| `gcp-pubsub-private-topic-iam-member` | `WARNING` | gcp-pubsub-private-topic-iam-member 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-pubsub-private-topic-iam-member.yaml` |
| `gcp-run-private-service-iam-binding` | `WARNING` | gcp-run-private-service-iam-binding 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-run-private-service-iam-binding.yaml` |
| `gcp-run-private-service-iam-member` | `WARNING` | gcp-run-private-service-iam-member 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-run-private-service-iam-member.yaml` |
| `gcp-spanner-database-encrypted-with-cmk` | `WARNING` | gcp-spanner-database-encrypted-with-cmk 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-spanner-database-encrypted-with-cmk.yaml` |
| `gcp-sql-database-require-ssl` | `WARNING` | gcp-sql-database-require-ssl 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-sql-database-require-ssl.yaml` |
| `gcp-sql-database-ssl-insecure-value-postgres-mysql` | `WARNING` | 보안 옵션 누사 및 예방 단속 필요. | `security/gcp-sql-database-ssl-insecure-value-postgres-mysql.yaml` |
| `gcp-sql-database-ssl-insecure-value-sqlserver` | `WARNING` | 보안 옵션 누사 및 예방 단속 필요. | `security/gcp-sql-database-ssl-insecure-value-sqlserver.yaml` |
| `gcp-sql-public-database` | `WARNING` | gcp-sql-public-database 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-sql-public-database.yaml` |
| `gcp-sqlserver-no-public-ip` | `WARNING` | gcp-sqlserver-no-public-ip 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-sqlserver-no-public-ip.yaml` |
| `gcp-storage-bucket-not-public-iam-binding` | `WARNING` | gcp-storage-bucket-not-public-iam-binding 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-storage-bucket-not-public-iam-binding.yaml` |
| `gcp-storage-bucket-not-public-iam-member` | `WARNING` | gcp-storage-bucket-not-public-iam-member 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-storage-bucket-not-public-iam-member.yaml` |
| `gcp-storage-bucket-uniform-access` | `WARNING` | gcp-storage-bucket-uniform-access 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-storage-bucket-uniform-access.yaml` |
| `gcp-storage-versioning-enabled` | `WARNING` | gcp-storage-versioning-enabled 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/gcp-storage-versioning-enabled.yaml` |
| `gcp-sub-network-logging-enabled` | `WARNING` | gcp-sub-network-logging-enabled 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-sub-network-logging-enabled.yaml` |
| `gcp-sub-network-private-google-enabled` | `WARNING` | gcp-sub-network-private-google-enabled 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-sub-network-private-google-enabled.yaml` |
| `gcp-vertexai-dataset-encrypted-with-cmk` | `WARNING` | gcp-vertexai-dataset-encrypted-with-cmk 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-vertexai-dataset-encrypted-with-cmk.yaml` |
| `gcp-vertexai-metadata-store-encrypted-with-cmk` | `WARNING` | gcp-vertexai-metadata-store-encrypted-with-cmk 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-vertexai-metadata-store-encrypted-with-cmk.yaml` |
| `gcp-vertexai-private-instance` | `WARNING` | gcp-vertexai-private-instance 잠재적 결함 및 보안 이격율 정비 요망. | `security/gcp-vertexai-private-instance.yaml` |

## LANG

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `all-origins-allowed` | `WARNING` | all-origins-allowed IaC 보안 설정 정비 및 예방 조치 요망. | `security/s3-cors-all-origins.yaml` |
| `ec2-imdsv1-optional` | `ERROR` | IaC 보안 옵션 누사 경보: ec2-imdsv1-optional 설정율을 탑재 하십시오. | `security/ec2-imdsv1-optional.yaml` |
| `ecr-image-scan-on-push` | `WARNING` | ecr-image-scan-on-push 잠재적 결함 및 보안 이격율 정비 요망. | `security/ecr-image-scan-on-push.yaml` |
| `eks-insufficient-control-plane-logging` | `WARNING` | eks-insufficient-control-plane-logging 잠재적 결함 및 보안 이격율 정비 요망. | `security/eks-insufficient-control-plane-logging.yaml` |
| `eks-public-endpoint-enabled` | `WARNING` | eks-public-endpoint-enabled 잠재적 결함 및 보안 이격율 정비 요망. | `security/eks-public-endpoint-enabled.yaml` |
| `elastic-search-encryption-at-rest` | `WARNING` | elastic-search-encryption-at-rest 잠재적 결함 및 보안 이격율 정비 요망. | `security/elastic-search-encryption-at-rest.yaml` |
| `no-iam-admin-privileges` | `WARNING` | no-iam-admin-privileges 잠재적 결함 및 보안 이격율 정비 요망. | `security/iam/no-iam-admin-privileges.yaml` |
| `no-iam-creds-exposure` | `WARNING` | no-iam-creds-exposure 잠재적 결함 및 보안 이격율 정비 요망. | `security/iam/no-iam-creds-exposure.yaml` |
| `no-iam-data-exfiltration` | `WARNING` | no-iam-data-exfiltration 잠재적 결함 및 보안 이격율 정비 요망. | `security/iam/no-iam-data-exfiltration.yaml` |
| `no-iam-priv-esc-funcs` | `WARNING` | no-iam-priv-esc-funcs 잠재적 결함 및 보안 이격율 정비 요망. | `security/iam/no-iam-priv-esc-funcs.yaml` |
| `no-iam-priv-esc-other-users` | `WARNING` | no-iam-priv-esc-other-users 잠재적 결함 및 보안 이격율 정비 요망. | `security/iam/no-iam-priv-esc-other-users.yaml` |
| `no-iam-priv-esc-roles` | `WARNING` | no-iam-priv-esc-roles 잠재적 결함 및 보안 이격율 정비 요망. | `security/iam/no-iam-priv-esc-roles.yaml` |
| `no-iam-resource-exposure` | `WARNING` | no-iam-resource-exposure 잠재적 결함 및 보안 이격율 정비 요망. | `security/iam/no-iam-resource-exposure.yaml` |
| `no-iam-star-actions` | `WARNING` | no-iam-star-actions 잠재적 결함 및 보안 이격율 정비 요망. | `security/iam/no-iam-star-actions.yaml` |
| `rds-insecure-password-storage-in-source-code` | `WARNING` | rds-insecure-password-storage-in-source-code IaC 보안 설정 정비 및 예방 조치 요망. | `security/rds-insecure-password-storage-in-source-code.yaml` |
| `rds-public-access` | `WARNING` | rds-public-access IaC 보안 설정 정비 및 예방 조치 요망. | `security/rds-public-access.yaml` |
| `s3-public-read-bucket` | `WARNING` | S3 버킷 퍼블릭 오픈 및 암호화 누사 경보. | `security/s3-public-read-bucket.yaml` |
| `s3-public-rw-bucket` | `ERROR` | IaC 보안 옵션 누사 경보: s3-public-rw-bucket 설정율을 탑재 하십시오. | `security/s3-public-rw-bucket.yaml` |
| `s3-unencrypted-bucket` | `INFO` | S3 버킷 퍼블릭 오픈 및 암호화 누사 경보. | `security/s3-unencrypted-bucket.yaml` |
