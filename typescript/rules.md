# Typescript Semgrep Rules Summary

`typescript` 디렉토리 하위의 규칙 목록입니다. (테스트 파일 제외)

## ANGULAR

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `angular-bypasssecuritytrust` | `WARNING` | Angular 프론트엔드 이격율 주사 점검. | `security/audit/angular-domsanitizer.yaml` |

## AWS-CDK

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `aws-cdk-bucket-enforcessl` | `ERROR` | S3 버킷에 전송 중 암호화(SSL/TLS) 강제화 옵션이 누락되었습니다. 데이터 전송 기밀성을 위해 해당 옵션을 활성화하십시오. | `security/audit/awscdk-bucket-enforcessl.yml` |
| `awscdk-bucket-encryption` | `ERROR` | AWS CDK S3 버킷 생성 시 기본 암호화(KMS_MANAGED 등) 설정이 누락되었습니다. 데이터 보안을 위해 암호화 모드를 지정하세요. | `security/audit/awscdk-bucket-encryption.yml` |
| `awscdk-bucket-grantpublicaccessmethod` | `WARNING` | awscdk-bucket-grantpublicaccessmethod 잠재적 결함 및 보안 이격율 정비 요망. | `security/awscdk-bucket-grantpublicaccessmethod.yml` |
| `awscdk-codebuild-project-public` | `WARNING` | awscdk-codebuild-project-public 잠재적 결함 및 보안 이격율 정비 요망. | `security/awscdk-codebuild-project-public.yml` |
| `awscdk-sqs-unencryptedqueue` | `WARNING` | awscdk-sqs-unencryptedqueue 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/awscdk-sqs-unencryptedqueue.yml` |

## LANG

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `cors-regex-wildcard` | `WARNING` | cors-regex-wildcard 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/cors-regex-wildcard.yaml` |
| `moment-deprecated` | `INFO` | moment-deprecated 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/moment-deprecated.yaml` |
| `useless-ternary` | `ERROR` | 불필요한 삼항 연산자(a ? true : false 등) 사용이 감지되었습니다. 논리 직관성을 위해 단순 불리언 캐스팅 등으로 대체하세요. | `correctness/useless-ternary.yaml` |

## NESTJS

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `14.4.8` | `WARNING` | nestjs-header-cors-any 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/nestjs-header-cors-any.yaml` |
| `nestjs-header-xss-disabled` | `WARNING` | nestjs-header-xss-disabled 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/nestjs-header-xss-disabled.yaml` |
| `nestjs-open-redirect` | `WARNING` | nestjs-open-redirect 잠재적 결함 및 보안 이격율 정비 요망. | `security/audit/nestjs-open-redirect.yaml` |

## REACT

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `define-styled-components-on-module-level` | `WARNING` | define-styled-components-on-module-level 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/define-styled-components-on-module-level.yaml` |
| `i18next-key-format` | `WARNING` | i18next-key-format 잠재적 결함 및 보안 이격율 정비 요망. | `portability/i18next/i18next-key-format.yaml` |
| `jsx-label-not-i18n` | `WARNING` | jsx-label-not-i18n 잠재적 결함 및 보안 이격율 정비 요망. | `portability/i18next/jsx-label-not-i18n.yaml` |
| `jsx-not-internationalized` | `INFO` | jsx-not-internationalized 잠재적 결함 및 보안 이격율 정비 요망. | `portability/i18next/jsx-not-internationalized.yaml` |
| `mui-snackbar-message` | `WARNING` | mui-snackbar-message 잠재적 결함 및 보안 이격율 정비 요망. | `portability/i18next/mui-snackbar-message.yaml` |
| `react-dangerouslysetinnerhtml` | `WARNING` | React 컴포넌트 데이터 바인딩 가압 점검. | `security/audit/react-dangerouslysetinnerhtml.yaml` |
| `react-find-dom` | `WARNING` | React 컴포넌트 데이터 바인딩 가압 점검. | `best-practice/react-find-dom.yaml` |
| `react-href-var` | `WARNING` | React 컴포넌트 데이터 바인딩 가압 점검. | `security/audit/react-href-var.yaml` |
| `react-insecure-request` | `ERROR` | React 애플리케이션에서 암호화되지 않은 HTTP 요청이 감지되었습니다. 스니핑 공격에 노출되므로 https:// 사용을 권장합니다. | `security/react-insecure-request.yaml` |
| `react-jwt-decoded-property` | `INFO` | JWT 토큰 서명 및 디코드 검증 누사 점검. | `security/audit/react-jwt-decoded-property.yaml` |
| `react-jwt-in-localstorage` | `INFO` | JWT 토큰 서명 및 디코드 검증 누사 점검. | `security/audit/react-jwt-in-localstorage.yaml` |
| `react-legacy-component` | `WARNING` | React 컴포넌트 데이터 바인딩 가압 점검. | `best-practice/react-legacy-component.yaml` |
| `react-markdown-insecure-html` | `WARNING` | React 컴포넌트 데이터 바인딩 가압 점검. | `security/react-markdown-insecure-html.yaml` |
| `react-props-in-state` | `WARNING` | React 컴포넌트 데이터 바인딩 가압 점검. | `best-practice/react-props-in-state.yaml` |
| `react-props-spreading` | `INFO` | React 컴포넌트 데이터 바인딩 가압 점검. | `best-practice/react-props-spreading.yaml` |
| `react-unsanitized-method` | `WARNING` | React 컴포넌트 데이터 바인딩 가압 점검. | `security/audit/react-unsanitized-method.yaml` |
| `react-unsanitized-property` | `WARNING` | React 컴포넌트 데이터 바인딩 가압 점검. | `security/audit/react-unsanitized-property.yaml` |
| `useselect-label-not-i18n` | `WARNING` | useselect-label-not-i18n 잠재적 결함 및 보안 이격율 정비 요망. | `portability/i18next/useselect-label-not-i18n.yaml` |
