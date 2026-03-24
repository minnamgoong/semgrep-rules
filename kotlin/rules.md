# Kotlin Semgrep Rules Summary

`kotlin` 디렉토리 하위의 규칙 목록입니다. (테스트 파일 제외)

## GRADLE

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `build-gradle-password-hardcoded` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/build-gradle-password-hardcoded.yaml` |

## LANG

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `6.2.5` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/unencrypted-socket.yaml` |
| `6.2.5` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/use-of-sha1.yaml` |
| `6.2.5` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/no-null-cipher.yaml` |
| `9.1.3` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/defaulthttpclient-is-deprecated.yaml` |
| `anonymous-ldap-bind` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/anonymous-ldap-bind.yaml` |
| `bad-hexa-conversion` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/bad-hexa-conversion.yaml` |
| `command-injection-formatted-runtime-call` | `ERROR` | java.lang.Runtime 호출 인자에 가변 포맷 또는 동적 합산 문자열이 감지되었습니다. 외부 입력 탑재 시 명령어 주입(Command ... | `security/command-injection-formatted-runtime-call.yaml` |
| `cookie-missing-httponly` | `WARNING` | 쿠키 보안 속성(Secure/HttpOnly) 누출 우려 점검. | `security/cookie-missing-httponly.yaml` |
| `cookie-missing-secure-flag` | `WARNING` | 쿠키 보안 속성(Secure/HttpOnly) 누출 우려 점검. | `security/cookie-missing-secure-flag.yaml` |
| `ecb-cipher` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/ecb-cipher.yaml` |
| `gcm-detection` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/gcm-detection.yaml` |
| `use-of-md5` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/use-of-md5.yaml` |
| `use-of-weak-rsa-key` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/weak-rsa.yaml` |
