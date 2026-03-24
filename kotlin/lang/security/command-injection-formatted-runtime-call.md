# command-injection-formatted-runtime-call (Runtime 커맨드 인젝션 경보)
## 개요
`java.lang.Runtime.getRuntime().exec()` 등의 하위 주관 가동 인자에 사용자 가변 문자열 합산 등이 수용되는 국면을 점검합니다.
## 조치 방안
*   명령어 인자를 배열분할 전달하거나 `ProcessBuilder`로 이월 전사 하십시오.
