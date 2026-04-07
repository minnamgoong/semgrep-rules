# Generic Semgrep Rules Summary

`generic` 디렉토리 하위의 규칙 목록입니다. (테스트 파일 제외)

## CI
\n| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `bash_reverse_shell` | `ERROR` | bash_reverse_shell 보안 인젝션 및 런타임 버그 전사 예방 점검. | `security/bash-reverse-shell.yaml` |
\n## DOCKERFILE
\n| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `alias-must-be-unique` | `ERROR` | Alias 식별자 고유율을 수하 하세요. | `correctness/alias-must-be-unique.yaml` |
| `copy-from-own-alias` | `ERROR` | 자기 자신의 스테이지 레이어를 출처(from)로 명명하는 순환 구성을 경보합니다. | `correctness/copy-from-own-alias.yaml` |
| `multiple-cmd-instructions` | `ERROR` | Dockerfile 내 `CMD` 절 중복 가압 금지. 마지막 절만 효력을 발휘합니다. | `correctness/multiple-cmd-instructions.yaml` |
\n## NGINX
\n| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `header-injection` | `ERROR` | Nginx 헤더 가압 버퍼 오염 위험 경고. | `security/header-injection.yaml` |
\n## SECRETS
\n| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `detected-amazon-mws-auth-token` | `ERROR` | 보안 기밀/인증 문자열(Secret) 노출이 감지되었습니다. 보안 저장소로 대두 전담 하세요. | `security/detected-amazon-mws-auth-token.yaml` |
| `detected-artifactory-password` | `ERROR` | 보안 기밀/인증 문자열(Secret) 노출이 감지되었습니다. 보안 저장소로 대두 전담 하세요. | `security/detected-artifactory-password.yaml` |
| `detected-artifactory-token` | `ERROR` | 보안 기밀/인증 문자열(Secret) 노출이 감지되었습니다. 보안 저장소로 대두 전담 하세요. | `security/detected-artifactory-token.yaml` |
| `detected-aws-access-key-id-value` | `ERROR` | AWS Access/Secret 자격증명이 노출되었습니다. | `security/detected-aws-access-key-id-value.yaml` |
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
\n## VISUALFORCE
\n| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `xss-from-unescaped-url-param` | `ERROR` | xss-from-unescaped-url-param 보안 인젝션 및 런타임 버그 전사 예방 점검. | `security/ncino/vf/XSSFromUnescapedURLParam.yaml` |
