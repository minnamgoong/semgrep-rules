# httpservlet-path-traversal (파일 경로 조작 위험)

## 개요
사용자 동적 입력을 기반으로 `java.io.File`, `java.nio.file.Path` 등의 디렉토리 접근 경로를 조립하는 패턴을 경보합니다.

## 위험성
*   **Path Traversal (디렉토리 탐색)**: 공격자가 `../../etc/passwd` 같이 도약 제어용 특수문자 입력 시, 허용되지 않은 상위 디렉토리 파일들이 누출될 수 있습니다.

## 조치 방안
*   파일명/경로를 조립할 때 `../` 등의 도약 문자를 걸러내는 Validation을 하거나, 사전 정의된 고정 허용 목록(White List)만을 가리키도록 코드를 구성하세요.
