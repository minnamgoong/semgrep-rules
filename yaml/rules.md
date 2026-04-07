# Yaml Semgrep Rules Summary

`yaml` 디렉토리 하위의 규칙 목록입니다. (테스트 파일 제외)

## ARGO

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `argo-workflow-parameter-command-injection` | `ERROR` | Argo 워크플로우 매개변수 가동 중 원격 명령어 주입(Command Injection) 우려가 수렴됩니다. | `security/argo-workflow-parameter-command-injection.yaml` |
| `event-binding-payload-with-hyphen` | `WARNING` | 설정(YAML) 파이프라인 및 가변 인젝션 옵션 단속 점검. | `correctness/event-binding-payload-with-hyphen.yaml` |

## DOCKER-COMPOSE

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `- id: exposing-docker-socket-volume` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/exposing-docker-socket-volume.yaml` |
| `- id: no-new-privileges` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/no-new-privileges.yaml` |
| `- id: privileged-service` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/privileged-service.yaml` |
| `- id: seccomp-confinement-disabled` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/seccomp-confinement-disabled.yaml` |
| `- id: selinux-separation-disabled` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/selinux-separation-disabled.yaml` |
| `- id: writable-filesystem-service` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/writable-filesystem-service.yaml` |

## GITHUB-ACTIONS

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `allowed-unsecure-commands` | `WARNING` | 설정(YAML) 파이프라인 및 가변 인젝션 옵션 단속 점검. | `security/allowed-unsecure-commands.yaml` |
| `curl-eval` | `ERROR` | curl-eval 보안 인젝션 및 런타임 버그 전사 예방 점검. | `security/curl-eval.yaml` |
| `detect-shai-hulud-backdoor` | `ERROR` | detect-shai-hulud-backdoor 보안 인젝션 및 런타임 버그 전사 예방 점검. | `security/detect-shai-hulud-backdoor.yaml` |
| `github-script-injection` | `ERROR` | github-script-injection 보안 인젝션 및 런타임 버그 전사 예방 점검. | `security/github-script-injection.yaml` |
| `- id: pull-request-target-code-checkout` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/pull-request-target-code-checkout.yaml` |
| `run-shell-injection` | `ERROR` | run-shell-injection 보안 인젝션 및 런타임 버그 전사 예방 점검. | `security/run-shell-injection.yaml` |
| `semgrep-github-action-push-without-branches` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `semgrep-configuration/semgrep-github-action-push-without-branches.yml` |
| `third-party-action-not-pinned-to-commit-sha` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/third-party-action-not-pinned-to-commit-sha.yml` |
| `unsafe-add-mask-workflow-command` | `WARNING` | 설정(YAML) 파이프라인 및 가변 인젝션 옵션 단속 점검. | `security/audit/unsafe-add-mask-workflow-command.yaml` |
| `- id: workflow-run-target-code-checkout` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/workflow-run-target-code-checkout.yaml` |

## GITLAB

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `changes-with-when-never` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `correctness/changes-with-when-never.yaml` |

## KUBERNETES

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `- id: allow-privilege-escalation` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/allow-privilege-escalation.yaml` |
| `- id: allow-privilege-escalation-no-securitycontext` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/allow-privilege-escalation-no-securitycontext.yaml` |
| `- id: allow-privilege-escalation-true` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/allow-privilege-escalation-true.yaml` |
| `- id: exposing-docker-socket-hostpath` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/exposing-docker-socket-hostpath.yaml` |
| `flask-debugging-enabled` | `WARNING` | 설정(YAML) 파이프라인 및 가변 인젝션 옵션 단속 점검. | `security/env/flask-debugging-enabled.yaml` |
| `- id: hostipc-pod` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/hostipc-pod.yaml` |
| `- id: hostnetwork-pod` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/hostnetwork-pod.yaml` |
| `- id: hostpid-pod` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/hostpid-pod.yaml` |
| `legacy-api-clusterrole-excessive-permissions` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/legacy-api-clusterrole-excessive-permissions.yaml` |
| `no-fractional-cpu-limits` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/no-fractional-cpu-limits.yaml` |
| `- id: privileged-container` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/privileged-container.yaml` |
| `- id: run-as-non-root` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/run-as-non-root.yaml` |
| `- id: run-as-non-root-container-level` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/run-as-non-root-container-level.yaml` |
| `- id: run-as-non-root-container-level-missing-security-context` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/run-as-non-root-container-level-missing-security-context.yaml` |
| `- id: run-as-non-root-security-context-pod-level` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/run-as-non-root-security-context-pod-level.yaml` |
| `- id: run-as-non-root-unsafe-value` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/run-as-non-root-unsafe-value.yaml` |
| `- id: seccomp-confinement-disabled` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/seccomp-confinement-disabled.yaml` |
| `- id: secrets-in-config-file` | `WARNING` | 자격증명/보안 기밀 문자열 누락 여부 점검. | `security/secrets-in-config-file.yaml` |
| `- id: skip-tls-verify-cluster` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/skip-tls-verify-cluster.yaml` |
| `- id: skip-tls-verify-service` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/skip-tls-verify-service.yaml` |
| `- id: writable-filesystem-container` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/writable-filesystem-container.yaml` |

## OPENAPI

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `api-key-in-query-parameter` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/api-key-in-query-parameter.yaml` |
| `openai-consequential-action-false` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/openai-consequential-action-false.yaml` |
| `use-of-basic-authentication` | `ERROR` | use-of-basic-authentication 보안 인젝션 및 런타임 버그 전사 예방 점검. | `security/use-of-basic-authentication.yaml` |

## SEMGREP

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `interfile-true-under-metadata-and-no-options` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `interfile-true-under-metadata-and-no-options.yaml` |
| `interfile-true-under-metadata-and-options-already-present` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `interfile-true-under-metadata-and-options-already-present.yaml` |
| `- id: metadata-category` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `metadata-category.yaml` |
| `missing-message-field` | `WARNING` | 이 규칙에는 메시지가 없습니다. Semgrep에는 규칙에 메시지가 있어야 합니다. 규칙의 기능을 설명하는 메시지를 포함합니다. 이것이 문제인 이유와 해결 방법을 설명하는 메시지를 작성해 보세요. | `missing-message-field.yaml` |
| `- id: missing-language-field` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `missing-language-field.yaml` |
| `- id: duplicate-id` | `ERROR` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `duplicate-id.yaml` |
| `duplicate-pattern` | `ERROR` | Semgrep 규칙 저작 메타 데이터 정합성 점검: duplicate-pattern 누락 경보. | `duplicate-pattern.yaml` |
| `empty-message` | `WARNING` | 이 규칙에는 빈 메시지 필드가 있습니다. 이 규칙이 문제가 되는 이유와 해결 방법을 전달하는 메시지 필드를 추가해 보세요. 이렇게 하면 결과가 해결될 가능성이 높아집니다. | `empty-message.yaml` |
| `lang-consistency-bash` | `WARNING` | semgrep.dev 정규화와 다른 언어 구성에서 '$X'를 발견했습니다. 대신 'bash'를 사용하세요. | `consistency/lang-consistency-bash.yaml` |
| `lang-consistency-cpp` | `WARNING` | semgrep.dev 정규화와 다른 언어 구성에서 '$X'를 발견했습니다. 대신 'cpp'를 사용하세요. | `consistency/lang-consistency-cpp.yaml` |
| `lang-consistency-csharp` | `WARNING` | semgrep.dev 정규화와 다른 언어 구성에서 '$X'를 발견했습니다. 대신 'csharp'를 사용하세요. | `consistency/lang-consistency-csharp.yaml` |
| `lang-consistency-dockerfile` | `WARNING` | semgrep.dev 정규화와 다른 언어 구성에서 '$X'를 발견했습니다. 대신 'dockerfile'을 사용하세요. | `consistency/lang-consistency-dockerfile.yaml` |
| `lang-consistency-elixir` | `WARNING` | semgrep.dev 정규화와 다른 언어 구성에서 '$X'를 발견했습니다. 대신 '엘릭서'를 사용하세요. | `consistency/lang-consistency-elixir.yaml` |
| `lang-consistency-go` | `WARNING` | semgrep.dev 정규화와 다른 언어 구성에서 '$X'를 발견했습니다. 대신 'go'를 사용하세요. | `consistency/lang-consistency-go.yaml` |
| `lang-consistency-hcl` | `WARNING` | semgrep.dev 정규화와 다른 언어 구성에서 '$X'를 발견했습니다. Please use 'hcl' instead. | `consistency/lang-consistency-hcl.yaml` |
| `lang-consistency-js` | `WARNING` | semgrep.dev 정규화와 다른 언어 구성에서 '$X'를 발견했습니다. 대신 'js'를 사용하세요. | `consistency/lang-consistency-js.yaml` |
| `lang-consistency-kotlin` | `WARNING` | semgrep.dev 정규화와 다른 언어 구성에서 '$X'를 발견했습니다. 대신 'kotlin'을 사용하세요. | `consistency/lang-consistency-kotlin.yaml` |
| `lang-consistency-python` | `WARNING` | semgrep.dev 정규화와 다른 언어 구성에서 '$X'를 발견했습니다. 대신 '파이썬'을 사용하세요. | `consistency/lang-consistency-python.yaml` |
| `lang-consistency-regex` | `WARNING` | semgrep.dev 정규화와 다른 언어 구성에서 '$X'를 발견했습니다. 대신 '정규식'을 사용하세요. | `consistency/lang-consistency-regex.yaml` |
| `lang-consistency-solidity` | `WARNING` | semgrep.dev 정규화와 다른 언어 구성에서 '$X'를 발견했습니다. 대신 'solidity'를 사용하세요. | `consistency/lang-consistency-solidity.yaml` |
| `lang-consistency-ts` | `WARNING` | semgrep.dev 정규화와 다른 언어 구성에서 '$X'를 발견했습니다. 대신 'ts'를 사용하세요. | `consistency/lang-consistency-ts.yaml` |
| `message-whitespace-check` | `WARNING` | 규칙 메시지에 추가 공백이 있는 것 같습니다. 이는 결과 결과에서 어색해 보일 수 있습니다. 추가 공백을 제거하십시오! | `message-whitespace.yaml` |
| `- id: metadata-confidence` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `metadata-confidence.yaml` |
| `- id: metadata-confidence-incorrect-value` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `metadata-confidence-incorrect-value.yaml` |
| `metadata-cwe` | `ERROR` | Semgrep 규칙 저작 메타 데이터 정합성 점검: metadata-cwe 누락 경보. | `metadata-cwe.yaml` |
| `metadata-cwe-prohibited-or-discouraged` | `ERROR` | Semgrep 규칙 저작 메타 데이터 정합성 점검: metadata-cwe-prohibited-or-discouraged 누락 경보. | `metadata-cwe-prohibited-or-discouraged.yaml` |
| `- id: metadata-deepsemgrep` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `metadata-deepsemgrep.yaml` |
| `- id: metadata-impact` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `metadata-impact.yaml` |
| `- id: metadata-impact-incorrect-value` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `metadata-impact-incorrect-value.yaml` |
| `- id: metadata-incorrect-option` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `metadata-incorrect-option.yaml` |
| `metadata-license` | `ERROR` | Semgrep 규칙 저작 메타 데이터 정합성 점검: metadata-license 누락 경보. | `metadata-license.yaml` |
| `- id: metadata-likelihood` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `metadata-likelihood.yaml` |
| `- id: metadata-likelihood-incorrect-value` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `metadata-likelihood-incorrect-value.yaml` |
| `metadata-owasp` | `ERROR` | Semgrep 규칙 저작 메타 데이터 정합성 점검: metadata-owasp 누락 경보. | `metadata-owasp.yaml` |
| `metadata-references` | `ERROR` | Semgrep 규칙 저작 메타 데이터 정합성 점검: metadata-references 누락 경보. | `metadata-references.yaml` |
| `- id: metadata-subcategory` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `metadata-subcategory.yaml` |
| `- id: metadata-subcategory-incorrect-value` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `metadata-subcategory-incorrect-value.yaml` |
| `- id: metadata-technology` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `metadata-technology.yaml` |
| `- id: missing-deconstructed-value` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `rule-missing-deconstructed-value.yaml` |
| `multi-line-message` | `WARNING` | 이 규칙에는 터미널에 제대로 표시되지 않을 수 있는 여러 줄의 메시지 필드가 있습니다. 한 줄에 있는지 확인하십시오. 예를 들어 `메시지: |`가 아닌 `메시지: >-`를 사용하세요. | `multi-line-message.yaml` |
| `- id: slow-pattern-general-func` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `slow-pattern-general-function.yaml` |
| `- id: slow-pattern-general-property` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `slow-pattern-general-property.yaml` |
| `- id: slow-pattern-single-metavariable` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `slow-pattern-single-metavariable.yaml` |
| `- id: slow-pattern-top-ellipsis` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `slow-pattern-top-ellipsis.yaml` |
| `- id: unnecessary-parent-operator` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `unnecessary-parent.yaml` |
| `unsatisfiable-rule` | `ERROR` | Semgrep 규칙 저작 메타 데이터 정합성 점검: unsatisfiable-rule 누락 경보. | `unsatisfiable.yaml` |
| `yaml-key-indentation-check` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `key-indentation.yaml` |
