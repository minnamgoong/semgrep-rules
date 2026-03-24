# shelljs-exec-injection (Shelljs 실행 인젝션 위험)

## 개요
`shelljs.exec()`에 가변 문자열 합체본을 전사하여 OS 명령을 실행을 기동하는 연산을 포획합니다.

## 위험성
*   **OS Command Injection**: 클라이언트 유입 단의 스페이스, 파이프 매개변수 조작으로 백그라운드 서버 코어 탈취 피해를 무방비로 입게 됩니다.

## 조치 방안
*   가변 문자열 그대로 전달하지 말고, `child_process` 범용 배열 인자 전달 방식을 우회 고용하세요.
