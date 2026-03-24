# Generic Semgrep Rules Summary

`generic` 디렉토리 하위의 규칙 목록입니다. (테스트 파일 제외)

## BICEP

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `secure-parameter-for-secrets` | `WARNING` | 자격증명/보안 기밀 문자열 누락 여부 점검. | `security/secure-parameter-for-secrets.yaml` |

## CI

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `bash_reverse_shell` | `ERROR` | bash_reverse_shell 보안 인젝션 및 런타임 버그 전사 예방 점검. | `security/bash-reverse-shell.yaml` |
| `changed-semgrepignore` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `audit/changed-semgrepignore.yaml` |

## DOCKERFILE

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `alias-must-be-unique` | `ERROR` | Alias 식별자 고유율을 수하 하세요. | `correctness/alias-must-be-unique.yaml` |
| `copy-from-own-alias` | `ERROR` | 자기 자신의 스테이지 레이어를 출처(from)로 명명하는 순환 구성을 경보합니다. | `correctness/copy-from-own-alias.yaml` |
| `missing-yum-clean-all` | `WARNING` | missing-yum-clean-all 잠재적 결함 분기 정비 요망. | `best-practice/missing-yum-clean-all.yaml` |
| `missing-zypper-no-confirm-switch` | `WARNING` | missing-zypper-no-confirm-switch 잠재적 결함 분기 정비 요망. | `missing-zypper-no-confirm-switch.yaml` |
| `multiple-cmd-instructions` | `ERROR` | Dockerfile 내 `CMD` 절 중복 가압 금지. 마지막 절만 효력을 발휘합니다. | `correctness/multiple-cmd-instructions.yaml` |
| `use-absolute-workdir` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/use-absolute-workdir.yaml` |

## GRADLE

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `build-gradle-password-hardcoded` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/build-gradle-password-hardcoded.yaml` |

## HTML-TEMPLATES

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `unquoted-attribute-var` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/unquoted-attribute-var.yaml` |
| `var-in-href` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/var-in-href.yaml` |
| `var-in-script-src` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/var-in-script-src.yaml` |
| `var-in-script-tag` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/var-in-script-tag.yaml` |

## HUGO

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `invalid-base-url` | `WARNING` | invalid-base-url 잠재적 결함 분기 정비 요망. | `best-practice/invalid-base-url.yaml` |
| `localhost-base-url` | `WARNING` | localhost-base-url 잠재적 결함 분기 정비 요망. | `best-practice/localhost-base-url.yaml` |

## NGINX

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `alias-path-traversal` | `WARNING` | alias-path-traversal 잠재적 결함 분기 정비 요망. | `security/alias-path-traversal.yaml` |
| `dynamic-proxy-host` | `WARNING` | dynamic-proxy-host 잠재적 결함 분기 정비 요망. | `security/dynamic-proxy-host.yaml` |
| `dynamic-proxy-scheme` | `WARNING` | dynamic-proxy-scheme 잠재적 결함 분기 정비 요망. | `security/dynamic-proxy-scheme.yaml` |
| `header-injection` | `ERROR` | Nginx 헤더 가압 버퍼 오염 위험 경고. | `security/header-injection.yaml` |
| `header-redefinition` | `WARNING` | header-redefinition 잠재적 결함 분기 정비 요망. | `security/header-redefinition.yaml` |
| `insecure-redirect` | `WARNING` | 보안 옵션 누사 및 예방 단속 필요. | `security/insecure-redirect.yaml` |
| `insecure-ssl-version` | `WARNING` | 보안 옵션 누사 및 예방 단속 피로도 증대. | `security/insecure-ssl-version.yaml` |
| `missing-internal` | `WARNING` | missing-internal 잠재적 결함 분기 정비 요망. | `security/missing-internal.yaml` |
| `missing-ssl-version` | `WARNING` | missing-ssl-version 잠재적 결함 분기 정비 요망. | `security/missing-ssl-version.yaml` |
| `possible-nginx-h2c-smuggling` | `WARNING` | possible-nginx-h2c-smuggling 잠재적 결함 분기 정비 요망. | `security/possible-h2c-smuggling.yaml` |
| `request-host-used` | `WARNING` | request-host-used 잠재적 결함 분기 정비 요망. | `security/request-host-used.yaml` |

## SECRETS

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `adafruit-api-key` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/adafruit-api-key.yaml` |
| `adobe-client-id` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/adobe-client-id.yaml` |
| `adobe-client-secret` | `INFO` | 자격증명/보안 기밀 문자열 누락 여부 점검. | `gitleaks/adobe-client-secret.yaml` |
| `age-secret-key` | `INFO` | 자격증명/보안 기밀 문자열 누락 여부 점검. | `gitleaks/age-secret-key.yaml` |
| `airtable-api-key` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/airtable-api-key.yaml` |
| `algolia-api-key` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/algolia-api-key.yaml` |
| `alibaba-access-key-id` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/alibaba-access-key-id.yaml` |
| `alibaba-secret-key` | `INFO` | 자격증명/보안 기밀 문자열 누락 여부 점검. | `gitleaks/alibaba-secret-key.yaml` |
| `asana-client-id` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/asana-client-id.yaml` |
| `asana-client-secret` | `INFO` | 자격증명/보안 기밀 문자열 누락 여부 점검. | `gitleaks/asana-client-secret.yaml` |
| `atlassian-api-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/atlassian-api-token.yaml` |
| `authress-service-client-access-key` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/authress-service-client-access-key.yaml` |
| `aws-access-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/aws-access-token.yaml` |
| `beamer-api-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/beamer-api-token.yaml` |
| `bitbucket-client-id` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/bitbucket-client-id.yaml` |
| `bitbucket-client-secret` | `INFO` | 자격증명/보안 기밀 문자열 누락 여부 점검. | `gitleaks/bitbucket-client-secret.yaml` |
| `bittrex-access-key` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/bittrex-access-key.yaml` |
| `bittrex-secret-key` | `INFO` | 자격증명/보안 기밀 문자열 누락 여부 점검. | `gitleaks/bittrex-secret-key.yaml` |
| `clojars-api-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/clojars-api-token.yaml` |
| `cloudflare-api-key` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/cloudflare-api-key.yaml` |
| `cloudflare-global-api-key` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/cloudflare-global-api-key.yaml` |
| `cloudflare-origin-ca-key` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/cloudflare-origin-ca-key.yaml` |
| `codecov-access-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/codecov-access-token.yaml` |
| `coinbase-access-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/coinbase-access-token.yaml` |
| `confluent-access-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/confluent-access-token.yaml` |
| `confluent-secret-key` | `INFO` | 자격증명/보안 기밀 문자열 누락 여부 점검. | `gitleaks/confluent-secret-key.yaml` |
| `contentful-delivery-api-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/contentful-delivery-api-token.yaml` |
| `databricks-api-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/databricks-api-token.yaml` |
| `datadog-access-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/datadog-access-token.yaml` |
| `defined-networking-api-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/defined-networking-api-token.yaml` |
| `detected-amazon-mws-auth-token` | `ERROR` | 보안 기밀/인증 문자열(Secret) 노출이 감지되었습니다. 보안 저장소로 대두 전담 하세요. | `security/detected-amazon-mws-auth-token.yaml` |
| `detected-artifactory-password` | `ERROR` | 보안 기밀/인증 문자열(Secret) 노출이 감지되었습니다. 보안 저장소로 대두 전담 하세요. | `security/detected-artifactory-password.yaml` |
| `detected-artifactory-token` | `ERROR` | 보안 기밀/인증 문자열(Secret) 노출이 감지되었습니다. 보안 저장소로 대두 전담 하세요. | `security/detected-artifactory-token.yaml` |
| `detected-aws-access-key-id-value` | `ERROR` | AWS Access/Secret 자격증명이 노출되었습니다. | `security/detected-aws-access-key-id-value.yaml` |
| `detected-aws-account-id` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/detected-aws-account-id.yaml` |
| `detected-aws-appsync-graphql-key` | `ERROR` | AWS Access/Secret 자격증명이 노출되었습니다. | `security/detected-aws-appsync-graphql-key.yaml` |
| `detected-aws-secret-access-key` | `ERROR` | AWS Access/Secret 자격증명이 노출되었습니다. | `security/detected-aws-secret-access-key.yaml` |
| `detected-aws-session-token` | `ERROR` | AWS Access/Secret 자격증명이 노출되었습니다. | `security/detected-aws-session-token.yaml` |
| `detected-bcrypt-hash` | `ERROR` | 보안 기밀/인증 문자열(Secret) 노출이 감지되었습니다. 보안 저장소로 대두 전담 하세요. | `security/detected-bcrypt-hash.yaml` |
| `detected-codeclimate` | `ERROR` | 보안 기밀/인증 문자열(Secret) 노출이 감지되었습니다. 보안 저장소로 대두 전담 하세요. | `security/detected-codeclimate.yaml` |
| `detected-etc-shadow` | `ERROR` | 보안 기밀/인증 문자열(Secret) 노출이 감지되었습니다. 보안 저장소로 대두 전담 하세요. | `security/detected-etc-shadow.yaml` |
| `detected-facebook-access-token` | `ERROR` | Facebook 인증 토큰이 노출되었습니다. | `security/detected-facebook-access-token.yaml` |
| `detected-facebook-oauth` | `ERROR` | Facebook 인증 토큰이 노출되었습니다. | `security/detected-facebook-oauth.yaml` |
| `detected-generic-api-key` | `ERROR` | 보안 기밀/인증 문자열(Secret) 노출이 감지되었습니다. 보안 저장소로 대두 전담 하세요. | `security/detected-generic-api-key.yaml` |
| `detected-generic-secret` | `ERROR` | 보안 기밀/인증 문자열(Secret) 노출이 감지되었습니다. 보안 저장소로 대두 전담 하세요. | `security/detected-generic-secret.yaml` |
| `detected-github-token` | `ERROR` | GitHub 토큰 자격증명이 노출되었습니다. | `security/detected-github-token.yaml` |
| `detected-google-api-key` | `ERROR` | Google API/OAuth 자격증명이 노출되었습니다. | `security/detected-google-api-key.yaml` |
| `detected-google-cloud-api-key` | `ERROR` | Google API/OAuth 자격증명이 노출되었습니다. | `security/detected-google-cloud-api-key.yaml` |
| `detected-google-gcm-service-account` | `ERROR` | Google API/OAuth 자격증명이 노출되었습니다. | `security/detected-google-gcm-service-account.yaml` |
| `detected-google-oauth-access-token` | `ERROR` | Google API/OAuth 자격증명이 노출되었습니다. | `security/detected-google-oauth-access-token.yaml` |
| `detected-google-oauth-url` | `ERROR` | Google API/OAuth 자격증명이 노출되었습니다. | `security/detected-google-oauth.yaml` |
| `detected-heroku-api-key` | `ERROR` | 보안 기밀/인증 문자열(Secret) 노출이 감지되었습니다. 보안 저장소로 대두 전담 하세요. | `security/detected-heroku-api-key.yaml` |
| `detected-hockeyapp` | `ERROR` | 보안 기밀/인증 문자열(Secret) 노출이 감지되었습니다. 보안 저장소로 대두 전담 하세요. | `security/detected-hockeyapp.yaml` |
| `detected-jwt-token` | `ERROR` | 보안 기밀/인증 문자열(Secret) 노출이 감지되었습니다. 보안 저장소로 대두 전담 하세요. | `security/detected-jwt-token.yaml` |
| `detected-kolide-api-key` | `ERROR` | 보안 기밀/인증 문자열(Secret) 노출이 감지되었습니다. 보안 저장소로 대두 전담 하세요. | `security/detected-kolide-api-key.yaml` |
| `detected-mailchimp-api-key` | `ERROR` | 보안 기밀/인증 문자열(Secret) 노출이 감지되었습니다. 보안 저장소로 대두 전담 하세요. | `security/detected-mailchimp-api-key.yaml` |
| `detected-mailgun-api-key` | `ERROR` | 보안 기밀/인증 문자열(Secret) 노출이 감지되었습니다. 보안 저장소로 대두 전담 하세요. | `security/detected-mailgun-api-key.yaml` |
| `detected-npm-registry-auth-token` | `ERROR` | 보안 기밀/인증 문자열(Secret) 노출이 감지되었습니다. 보안 저장소로 대두 전담 하세요. | `security/detected-npm-registry-auth-token.yaml` |
| `detected-onfido-live-api-token` | `ERROR` | 보안 기밀/인증 문자열(Secret) 노출이 감지되었습니다. 보안 저장소로 대두 전담 하세요. | `security/detected-onfido-live-api-token.yaml` |
| `detected-outlook-team` | `ERROR` | 보안 기밀/인증 문자열(Secret) 노출이 감지되었습니다. 보안 저장소로 대두 전담 하세요. | `security/detected-outlook-team.yaml` |
| `detected-paypal-braintree-access-token` | `ERROR` | 보안 기밀/인증 문자열(Secret) 노출이 감지되었습니다. 보안 저장소로 대두 전담 하세요. | `security/detected-paypal-braintree-access-token.yaml` |
| `detected-pgp-private-key-block` | `ERROR` | 보안 기밀/인증 문자열(Secret) 노출이 감지되었습니다. 보안 저장소로 대두 전담 하세요. | `security/detected-pgp-private-key-block.yaml` |
| `detected-picatic-api-key` | `ERROR` | 보안 기밀/인증 문자열(Secret) 노출이 감지되었습니다. 보안 저장소로 대두 전담 하세요. | `security/detected-picatic-api-key.yaml` |
| `detected-private-key` | `ERROR` | 보안 기밀/인증 문자열(Secret) 노출이 감지되었습니다. 보안 저장소로 대두 전담 하세요. | `security/detected-private-key.yaml` |
| `detected-sauce-token` | `ERROR` | 보안 기밀/인증 문자열(Secret) 노출이 감지되었습니다. 보안 저장소로 대두 전담 하세요. | `security/detected-sauce-token.yaml` |
| `detected-sendgrid-api-key` | `ERROR` | 보안 기밀/인증 문자열(Secret) 노출이 감지되었습니다. 보안 저장소로 대두 전담 하세요. | `security/detected-sendgrid-api-key.yaml` |
| `detected-slack-token` | `ERROR` | Slack 토큰 자격증명이 노출되었습니다. | `security/detected-slack-token.yaml` |
| `detected-slack-webhook` | `ERROR` | Slack 토큰 자격증명이 노출되었습니다. | `security/detected-slack-webhook.yaml` |
| `detected-snyk-api-key` | `ERROR` | 보안 기밀/인증 문자열(Secret) 노출이 감지되었습니다. 보안 저장소로 대두 전담 하세요. | `security/detected-snyk-api-key.yaml` |
| `detected-softlayer-api-key` | `ERROR` | 보안 기밀/인증 문자열(Secret) 노출이 감지되었습니다. 보안 저장소로 대두 전담 하세요. | `security/detected-softlayer-api-key.yaml` |
| `detected-sonarqube-docs-api-key` | `ERROR` | 보안 기밀/인증 문자열(Secret) 노출이 감지되었습니다. 보안 저장소로 대두 전담 하세요. | `security/detected-sonarqube-docs-api-key.yaml` |
| `detected-square-access-token` | `ERROR` | 보안 기밀/인증 문자열(Secret) 노출이 감지되었습니다. 보안 저장소로 대두 전담 하세요. | `security/detected-square-access-token.yaml` |
| `detected-square-oauth-secret` | `ERROR` | 보안 기밀/인증 문자열(Secret) 노출이 감지되었습니다. 보안 저장소로 대두 전담 하세요. | `security/detected-square-oauth-secret.yaml` |
| `detected-ssh-password` | `ERROR` | 보안 기밀/인증 문자열(Secret) 노출이 감지되었습니다. 보안 저장소로 대두 전담 하세요. | `security/detected-ssh-password.yaml` |
| `detected-stripe-api-key` | `ERROR` | 보안 기밀/인증 문자열(Secret) 노출이 감지되었습니다. 보안 저장소로 대두 전담 하세요. | `security/detected-stripe-api-key.yaml` |
| `detected-stripe-restricted-api-key` | `ERROR` | 보안 기밀/인증 문자열(Secret) 노출이 감지되었습니다. 보안 저장소로 대두 전담 하세요. | `security/detected-stripe-restricted-api-key.yaml` |
| `detected-telegram-bot-api-key` | `ERROR` | 보안 기밀/인증 문자열(Secret) 노출이 감지되었습니다. 보안 저장소로 대두 전담 하세요. | `security/detected-telegram-bot-api-key.yaml` |
| `detected-twilio-api-key` | `ERROR` | 보안 기밀/인증 문자열(Secret) 노출이 감지되었습니다. 보안 저장소로 대두 전담 하세요. | `security/detected-twilio-api-key.yaml` |
| `detected-username-and-password-in-uri` | `ERROR` | 보안 기밀/인증 문자열(Secret) 노출이 감지되었습니다. 보안 저장소로 대두 전담 하세요. | `security/detected-username-and-password-in-uri.yaml` |
| `digitalocean-access-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/digitalocean-access-token.yaml` |
| `digitalocean-pat` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/digitalocean-pat.yaml` |
| `digitalocean-refresh-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/digitalocean-refresh-token.yaml` |
| `discord-api-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/discord-api-token.yaml` |
| `discord-client-id` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/discord-client-id.yaml` |
| `discord-client-secret` | `INFO` | 자격증명/보안 기밀 문자열 누락 여부 점검. | `gitleaks/discord-client-secret.yaml` |
| `doppler-api-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/doppler-api-token.yaml` |
| `droneci-access-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/droneci-access-token.yaml` |
| `dropbox-api-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/dropbox-api-token.yaml` |
| `dropbox-long-lived-api-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/dropbox-long-lived-api-token.yaml` |
| `dropbox-short-lived-api-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/dropbox-short-lived-api-token.yaml` |
| `duffel-api-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/duffel-api-token.yaml` |
| `dynatrace-api-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/dynatrace-api-token.yaml` |
| `easypost-api-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/easypost-api-token.yaml` |
| `easypost-test-api-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/easypost-test-api-token.yaml` |
| `etsy-access-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/etsy-access-token.yaml` |
| `facebook` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/facebook.yaml` |
| `facebook-access-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/facebook-access-token.yaml` |
| `facebook-page-access-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/facebook-page-access-token.yaml` |
| `facebook-secret` | `INFO` | 자격증명/보안 기밀 문자열 누락 여부 점검. | `gitleaks/facebook-secret.yaml` |
| `fastly-api-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/fastly-api-token.yaml` |
| `finicity-api-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/finicity-api-token.yaml` |
| `finicity-client-secret` | `INFO` | 자격증명/보안 기밀 문자열 누락 여부 점검. | `gitleaks/finicity-client-secret.yaml` |
| `finnhub-access-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/finnhub-access-token.yaml` |
| `flickr-access-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/flickr-access-token.yaml` |
| `flutterwave-encryption-key` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/flutterwave-encryption-key.yaml` |
| `flutterwave-public-key` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/flutterwave-public-key.yaml` |
| `flutterwave-secret-key` | `INFO` | 자격증명/보안 기밀 문자열 누락 여부 점검. | `gitleaks/flutterwave-secret-key.yaml` |
| `frameio-api-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/frameio-api-token.yaml` |
| `freshbooks-access-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/freshbooks-access-token.yaml` |
| `gcp-api-key` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/gcp-api-key.yaml` |
| `generic-api-key` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/generic-api-key.yaml` |
| `github-app-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/github-app-token.yaml` |
| `github-fine-grained-pat` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/github-fine-grained-pat.yaml` |
| `github-oauth` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/github-oauth.yaml` |
| `github-pat` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/github-pat.yaml` |
| `github-refresh-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/github-refresh-token.yaml` |
| `gitlab-pat` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/gitlab-pat.yaml` |
| `gitlab-ptt` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/gitlab-ptt.yaml` |
| `gitlab-rrt` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/gitlab-rrt.yaml` |
| `gitter-access-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/gitter-access-token.yaml` |
| `gocardless-api-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/gocardless-api-token.yaml` |
| `google-maps-apikeyleak` | `MEDIUM` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/google-maps-apikeyleak.yaml` |
| `grafana-api-key` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/grafana-api-key.yaml` |
| `grafana-cloud-api-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/grafana-cloud-api-token.yaml` |
| `grafana-service-account-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/grafana-service-account-token.yaml` |
| `harness-api-key` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/harness-api-key.yaml` |
| `hashicorp-tf-api-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/hashicorp-tf-api-token.yaml` |
| `hashicorp-tf-password` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/hashicorp-tf-password.yaml` |
| `heroku-api-key` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/heroku-api-key.yaml` |
| `hubspot-api-key` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/hubspot-api-key.yaml` |
| `huggingface-access-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/huggingface-access-token.yaml` |
| `huggingface-organization-api-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/huggingface-organization-api-token.yaml` |
| `infracost-api-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/infracost-api-token.yaml` |
| `intercom-api-key` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/intercom-api-key.yaml` |
| `intra42-client-secret` | `INFO` | 자격증명/보안 기밀 문자열 누락 여부 점검. | `gitleaks/intra42-client-secret.yaml` |
| `jfrog-api-key` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/jfrog-api-key.yaml` |
| `jfrog-identity-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/jfrog-identity-token.yaml` |
| `jwt` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/jwt.yaml` |
| `jwt-base64` | `INFO` | JWT 토큰 서명 및 디코드 검증 누락 여부 점검. | `gitleaks/jwt-base64.yaml` |
| `kraken-access-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/kraken-access-token.yaml` |
| `kucoin-access-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/kucoin-access-token.yaml` |
| `kucoin-secret-key` | `INFO` | 자격증명/보안 기밀 문자열 누락 여부 점검. | `gitleaks/kucoin-secret-key.yaml` |
| `launchdarkly-access-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/launchdarkly-access-token.yaml` |
| `linear-api-key` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/linear-api-key.yaml` |
| `linear-client-secret` | `INFO` | 자격증명/보안 기밀 문자열 누락 여부 점검. | `gitleaks/linear-client-secret.yaml` |
| `linkedin-client-id` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/linkedin-client-id.yaml` |
| `linkedin-client-secret` | `INFO` | 자격증명/보안 기밀 문자열 누락 여부 점검. | `gitleaks/linkedin-client-secret.yaml` |
| `lob-api-key` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/lob-api-key.yaml` |
| `lob-pub-api-key` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/lob-pub-api-key.yaml` |
| `mailchimp-api-key` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/mailchimp-api-key.yaml` |
| `mailgun-private-api-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/mailgun-private-api-token.yaml` |
| `mailgun-pub-key` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/mailgun-pub-key.yaml` |
| `mailgun-signing-key` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/mailgun-signing-key.yaml` |
| `mapbox-api-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/mapbox-api-token.yaml` |
| `mattermost-access-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/mattermost-access-token.yaml` |
| `messagebird-api-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/messagebird-api-token.yaml` |
| `messagebird-client-id` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/messagebird-client-id.yaml` |
| `microsoft-teams-webhook` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/microsoft-teams-webhook.yaml` |
| `netlify-access-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/netlify-access-token.yaml` |
| `new-relic-browser-api-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/new-relic-browser-api-token.yaml` |
| `new-relic-insert-key` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/new-relic-insert-key.yaml` |
| `new-relic-user-api-id` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/new-relic-user-api-id.yaml` |
| `new-relic-user-api-key` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/new-relic-user-api-key.yaml` |
| `npm-access-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/npm-access-token.yaml` |
| `nytimes-access-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/nytimes-access-token.yaml` |
| `okta-access-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/okta-access-token.yaml` |
| `openai-api-key` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/openai-api-key.yaml` |
| `plaid-api-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/plaid-api-token.yaml` |
| `plaid-client-id` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/plaid-client-id.yaml` |
| `plaid-secret-key` | `INFO` | 자격증명/보안 기밀 문자열 누락 여부 점검. | `gitleaks/plaid-secret-key.yaml` |
| `planetscale-api-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/planetscale-api-token.yaml` |
| `planetscale-oauth-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/planetscale-oauth-token.yaml` |
| `planetscale-password` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/planetscale-password.yaml` |
| `postman-api-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/postman-api-token.yaml` |
| `prefect-api-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/prefect-api-token.yaml` |
| `private-key` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/private-key.yaml` |
| `pulumi-api-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/pulumi-api-token.yaml` |
| `pypi-upload-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/pypi-upload-token.yaml` |
| `rapidapi-access-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/rapidapi-access-token.yaml` |
| `readme-api-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/readme-api-token.yaml` |
| `rubygems-api-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/rubygems-api-token.yaml` |
| `scalingo-api-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/scalingo-api-token.yaml` |
| `sendbird-access-id` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/sendbird-access-id.yaml` |
| `sendbird-access-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/sendbird-access-token.yaml` |
| `sendgrid-api-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/sendgrid-api-token.yaml` |
| `sendinblue-api-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/sendinblue-api-token.yaml` |
| `sentry-access-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/sentry-access-token.yaml` |
| `shippo-api-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/shippo-api-token.yaml` |
| `shopify-access-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/shopify-access-token.yaml` |
| `shopify-custom-access-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/shopify-custom-access-token.yaml` |
| `shopify-private-app-access-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/shopify-private-app-access-token.yaml` |
| `shopify-shared-secret` | `INFO` | 자격증명/보안 기밀 문자열 누락 여부 점검. | `gitleaks/shopify-shared-secret.yaml` |
| `sidekiq-secret` | `INFO` | 자격증명/보안 기밀 문자열 누락 여부 점검. | `gitleaks/sidekiq-secret.yaml` |
| `sidekiq-sensitive-url` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/sidekiq-sensitive-url.yaml` |
| `slack-app-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/slack-app-token.yaml` |
| `slack-bot-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/slack-bot-token.yaml` |
| `slack-config-access-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/slack-config-access-token.yaml` |
| `slack-config-refresh-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/slack-config-refresh-token.yaml` |
| `slack-legacy-bot-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/slack-legacy-bot-token.yaml` |
| `slack-legacy-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/slack-legacy-token.yaml` |
| `slack-legacy-workspace-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/slack-legacy-workspace-token.yaml` |
| `slack-user-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/slack-user-token.yaml` |
| `slack-webhook-url` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/slack-webhook-url.yaml` |
| `snyk-api-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/snyk-api-token.yaml` |
| `square-access-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/square-access-token.yaml` |
| `squarespace-access-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/squarespace-access-token.yaml` |
| `stripe-access-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/stripe-access-token.yaml` |
| `sumologic-access-id` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/sumologic-access-id.yaml` |
| `sumologic-access-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/sumologic-access-token.yaml` |
| `telegram-bot-api-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/telegram-bot-api-token.yaml` |
| `travisci-access-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/travisci-access-token.yaml` |
| `twilio-api-key` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/twilio-api-key.yaml` |
| `twitch-api-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/twitch-api-token.yaml` |
| `twitter-access-secret` | `INFO` | 자격증명/보안 기밀 문자열 누락 여부 점검. | `gitleaks/twitter-access-secret.yaml` |
| `twitter-access-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/twitter-access-token.yaml` |
| `twitter-api-key` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/twitter-api-key.yaml` |
| `twitter-api-secret` | `INFO` | 자격증명/보안 기밀 문자열 누락 여부 점검. | `gitleaks/twitter-api-secret.yaml` |
| `twitter-bearer-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/twitter-bearer-token.yaml` |
| `typeform-api-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/typeform-api-token.yaml` |
| `vault-batch-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/vault-batch-token.yaml` |
| `vault-service-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/vault-service-token.yaml` |
| `yandex-access-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/yandex-access-token.yaml` |
| `yandex-api-key` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/yandex-api-key.yaml` |
| `yandex-aws-access-token` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `gitleaks/yandex-aws-access-token.yaml` |
| `zendesk-secret-key` | `INFO` | 자격증명/보안 기밀 문자열 누락 여부 점검. | `gitleaks/zendesk-secret-key.yaml` |

## UNICODE

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `contains-bidirectional-characters` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/bidi.yml` |

## VISUALFORCE

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `csp-header-attribute` | `INFO` | csp-header-attribute 잠재적 결함 분기 정비 요망. | `security/ncino/xml/CSPHeaderAttribute.yaml` |
| `use-SRI-for-CDNs` | `WARNING` | use-SRI-for-CDNs 잠재적 결함 분기 정비 요망. | `security/ncino/html/UseSRIForCDNs.yaml` |
| `visualforce-page-api-version` | `WARNING` | visualforce-page-api-version 잠재적 결함 분기 정비 요망. | `security/ncino/xml/VisualForceAPIVersion.yaml` |
| `xss-from-unescaped-url-param` | `ERROR` | xss-from-unescaped-url-param 보안 인젝션 및 런타임 버그 전사 예방 점검. | `security/ncino/vf/XSSFromUnescapedURLParam.yaml` |
