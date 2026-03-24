# command-injection-formatted-runtime-call (Runtime 커맨드 인젝션 경보)
## 개요
java.lang.Runtime 호출 인자에 가변 포맷 또는 동적 합산 문자열이 감지되었습니다. 외부 입력 탑재 시 명령어 주입(Command Injection) 위협이 가중되므로 정적 분할 전달이나 세척을 거치십시오.
## 조치 방안
*   명령어 인자를 배열분할 전달하거나 `ProcessBuilder`로 이월 전사 하십시오.
