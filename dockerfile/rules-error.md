# Dockerfile Semgrep Rules Summary

`dockerfile` 디렉토리 하위의 규칙 목록입니다. (테스트 파일 제외)

## CORRECTNESS
\n| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `invalid-port` | `ERROR` | Dockerfile 연쇄 점검: invalid-port 준행 오류 국면 감지. | `invalid-port.yaml` |
| `multiple-entrypoint-instructions` | `ERROR` | ENTRYPOINT 명령어 다수 사용 시 충돌 국면 점검. | `multiple-entrypoint-instructions.yaml` |
\n## SECURITY
\n| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `dockerfile-dockerd-socket-mount` | `ERROR` | Dockerfile 연쇄 점검: dockerfile-dockerd-socket-mount 준행 오류 국면 감지. | `dockerd-socket-mount.yaml` |
| `last-user-is-root` | `ERROR` | 마지막 실행 컨텍스트가 root로 전사 탑재 되었습니다. | `last-user-is-root.yaml` |
| `missing-user` | `ERROR` | Dockerfile에 USER 명령어가 부재하여 root 권한 폭주 우려가 있습니다. | `missing-user.yaml` |
| `missing-user-entrypoint` | `ERROR` | USER 명령어 누사로 인한 컨테이너 root 실행 위험 지점입니다. | `missing-user-entrypoint.yaml` |
