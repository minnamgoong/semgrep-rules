# command-injection-formatted-runtime-call (런타임 커맨드 인젝션 경고)

## 개요
Runtime.exec에 동적 조립 문자열(String.format 등)을 인자로 전달하여 커맨드 인젝션 위험이 있습니다. 안정성을 위해 인자 리스트(String[]) 형식으로 전달하세요.

## 위험성
*   **Command Injection (명령 주입)**: 입력값에 공백과 함께 `; rm -rf /` 구조를 탑재하면 서버 권한으로 임의의 시스템 파괴 코드가 동작할 위험이 극히 높습니다.

## 조치 방안
*   단일 문자열 실행 구조를 버리고, `String[]` 배열로 명령어 및 인자를 일대일 정적 분할 전달하십시오.
