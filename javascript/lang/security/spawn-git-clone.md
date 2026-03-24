# spawn-git-clone (Git Clone 인젝션 경보)

## 개요
`spawn` 등을 통해 시스템 `git clone` 바이너리를 구동할 때 유저 제공 주소 파라미터를 그대로 탑재하는 경우를 주시합니다.

## 위험성
*   **Argument Injection**: `--upload-pack` 같은 Git 전용 위험 옵션을 URL 주소 위치에 탑재해 해커가 로컬 쉘 명령어 연쇄 실행을 유도할 수 있습니다.

## 조치 방안
*   인가된 Git 저장소 Base URL 이외의 부가 옵션이 붙지 않도록 유저 입력값 초입 유효성 루프를 정비하십시오.
