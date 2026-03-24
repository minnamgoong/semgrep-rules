# tainted-env-from-http-request (환경변수를 통한 오염 주입 경보)

## 개요
HTTP Header, Parameter 등으로 주입된 유저 가변 데이터가 시스템 쉘 명령어 가동 환경(Environment Variables)으로 흐르는 것을 포착합니다.

## 위험성
*   **Command Injection (명령 주입)**: 특정 환경 변수 로드 연쇄 시 명령 우회 지점 파훼, 쉘 취약 설정(예: Shellshock 등)을 격발시키는 원격 제어 취약점이 될 소지가 있습니다.

## 조치 방안
*   외부 유저 정적 유입을 인위적 시스템 환경설정 변수에 담지 마세요.
