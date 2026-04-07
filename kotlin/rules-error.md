# Kotlin Semgrep Rules Summary

`kotlin` 디렉토리 하위의 규칙 목록입니다. (테스트 파일 제외)

## LANG
\n| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `command-injection-formatted-runtime-call` | `ERROR` | java.lang.Runtime 호출 인자에 가변 포맷 또는 동적 합산 문자열이 감지되었습니다. 외부 입력 탑재 시 명령어 주입(Command Injection) 위협이 가중되므로 정적 분할 전달이나 세척을 거치십시오. | `security/command-injection-formatted-runtime-call.yaml` |
