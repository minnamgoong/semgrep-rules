# command-injection-formatted-runtime-call (런타임 커맨드 인젝션 경고)

## 개요
`java.lang.Runtime.getRuntime().exec()` 메서드에 포매팅된 동적 문자열을 그대로 명령어 인자로 전달하는 형태를 감지합니다.

## 위험성
*   **Command Injection (명령 주입)**: 입력값에 공백과 함께 `; rm -rf /` 구조를 탑재하면 서버 권한으로 임의의 시스템 파괴 코드가 동작할 위험이 극히 높습니다.

## 조치 방안
*   단일 문자열 실행 구조를 버리고, `String[]` 배열로 명령어 및 인자를 일대일 정적 분할 전달하십시오.
