# Dockerfile Semgrep Rules Summary

`dockerfile` 디렉토리 하위의 규칙 목록입니다. (테스트 파일 제외)

## AUDIT

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `dockerfile-pip-extra-index-url` | `INFO` | dockerfile-pip-extra-index-url 잠재적 결함 및 보안 이격율 정비 요망. | `dockerfile-pip-extra-index-url.yaml` |
| `dockerfile-source-not-pinned` | `INFO` | dockerfile-source-not-pinned 잠재적 결함 및 보안 이격율 정비 요망. | `dockerfile-source-not-pinned.yaml` |

## BEST-PRACTICE

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `avoid-apk-upgrade` | `INFO` | avoid-apk-upgrade 잠재적 결함 및 보안 이격율 정비 요망. | `avoid-apk-upgrade.yaml` |
| `avoid-apt-get-upgrade` | `WARNING` | avoid-apt-get-upgrade 잠재적 결함 및 보안 이격율 정비 요망. | `avoid-apt-get-upgrade.yaml` |
| `avoid-dnf-update` | `INFO` | Dockerfile 가동 중 베스트 프랙티스(Best Practice) 점검. | `avoid-dnf-update.yaml` |
| `avoid-latest-version` | `WARNING` | avoid-latest-version 잠재적 결함 및 보안 이격율 정비 요망. | `avoid-latest-version.yaml` |
| `avoid-platform-with-from` | `INFO` | Dockerfile 가동 중 베스트 프랙티스(Best Practice) 점검. | `avoid-platform-with-from.yaml` |
| `avoid-yum-update` | `INFO` | Dockerfile 가동 중 베스트 프랙티스(Best Practice) 점검. | `avoid-yum-update.yaml` |
| `avoid-zypper-update` | `INFO` | Dockerfile 가동 중 베스트 프랙티스(Best Practice) 점검. | `avoid-zypper-update.yaml` |
| `maintainer-is-deprecated` | `INFO` | Dockerfile 가동 중 베스트 프랙티스(Best Practice) 점검. | `maintainer-is-deprecated.yaml` |
| `missing-apk-no-cache` | `INFO` | missing-apk-no-cache 잠재적 결함 및 보안 이격율 정비 요망. | `missing-apk-no-cache.yaml` |
| `missing-dnf-assume-yes-switch` | `WARNING` | Dockerfile 가동 중 베스트 프랙티스(Best Practice) 점검. | `missing-dnf-assume-yes-switch.yaml` |
| `missing-dnf-clean-all` | `WARNING` | Dockerfile 가동 중 베스트 프랙티스(Best Practice) 점검. | `missing-dnf-clean-all.yaml` |
| `missing-image-version` | `WARNING` | missing-image-version 잠재적 결함 및 보안 이격율 정비 요망. | `missing-image-version.yaml` |
| `missing-no-install-recommends` | `INFO` | missing-no-install-recommends 잠재적 결함 및 보안 이격율 정비 요망. | `missing-no-install-recommends.yaml` |
| `missing-pip-no-cache-dir` | `INFO` | Dockerfile 가동 중 베스트 프랙티스(Best Practice) 점검. | `missing-pip-no-cache-dir.yaml` |
| `missing-yum-assume-yes-switch` | `WARNING` | Dockerfile 가동 중 베스트 프랙티스(Best Practice) 점검. | `missing-yum-assume-yes-switch.yaml` |
| `missing-zypper-clean` | `WARNING` | Dockerfile 가동 중 베스트 프랙티스(Best Practice) 점검. | `missing-zypper-clean.yaml` |
| `nonsensical-command` | `WARNING` | nonsensical-command 잠재적 결함 및 보안 이격율 정비 요망. | `nonsensical-command.yaml` |
| `prefer-apt-get` | `INFO` | Dockerfile 가동 중 베스트 프랙티스(Best Practice) 점검. | `prefer-apt-get.yaml` |
| `prefer-copy-over-add` | `INFO` | Dockerfile 가동 중 베스트 프랙티스(Best Practice) 점검. | `prefer-copy-over-add.yaml` |
| `prefer-json-notation` | `INFO` | Dockerfile 가동 중 베스트 프랙티스(Best Practice) 점검. | `prefer-json-notation.yaml` |
| `remove-package-cache` | `WARNING` | remove-package-cache 잠재적 결함 및 보안 이격율 정비 요망. | `remove-package-cache.yaml` |
| `remove-package-lists` | `WARNING` | remove-package-lists 잠재적 결함 및 보안 이격율 정비 요망. | `remove-package-lists.yaml` |
| `set-pipefail` | `WARNING` | set-pipefail 잠재적 결함 및 보안 이격율 정비 요망. | `set-pipefail.yaml` |
| `use-either-wget-or-curl` | `INFO` | Dockerfile 가동 중 베스트 프랙티스(Best Practice) 점검. | `use-either-wget-or-curl.yaml` |
| `use-shell-instruction` | `WARNING` | Dockerfile 가동 중 베스트 프랙티스(Best Practice) 점검. | `use-shell-instruction.yaml` |
| `use-workdir` | `WARNING` | use-workdir 잠재적 결함 및 보안 이격율 정비 요망. | `use-workdir.yaml` |

## CORRECTNESS

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `invalid-port` | `ERROR` | Dockerfile 연쇄 점검: invalid-port 준행 오류 국면 감지. | `invalid-port.yaml` |
| `missing-assume-yes-switch` | `WARNING` | missing-assume-yes-switch 잠재적 결함 및 보안 이격율 정비 요망. | `missing-assume-yes-switch.yaml` |
| `multiple-entrypoint-instructions` | `ERROR` | ENTRYPOINT 명령어 다수 사용 시 충돌 국면 점검. | `multiple-entrypoint-instructions.yaml` |

## SECURITY

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `dockerfile-dockerd-socket-mount` | `ERROR` | Dockerfile 연쇄 점검: dockerfile-dockerd-socket-mount 준행 오류 국면 감지. | `dockerd-socket-mount.yaml` |
| `last-user-is-root` | `ERROR` | 마지막 실행 컨텍스트가 root로 전사 탑재 되었습니다. | `last-user-is-root.yaml` |
| `missing-user` | `ERROR` | Dockerfile에 USER 명령어가 부재하여 root 권한 폭주 우려가 있습니다. | `missing-user.yaml` |
| `missing-user-entrypoint` | `ERROR` | USER 명령어 누사로 인한 컨테이너 root 실행 위험 지점입니다. | `missing-user-entrypoint.yaml` |
| `no-sudo-in-dockerfile` | `WARNING` | no-sudo-in-dockerfile 잠재적 결함 및 보안 이격율 정비 요망. | `no-sudo-in-dockerfile.yaml` |
| `secret-in-build-arg` | `WARNING` | 자격증명/보안 기밀 문자열 누사 점검. | `secret-in-build-arg.yaml` |
