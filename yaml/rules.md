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
| `exposing-docker-socket-volume` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/exposing-docker-socket-volume.yaml` |
| `no-new-privileges` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/no-new-privileges.yaml` |
| `privileged-service` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/privileged-service.yaml` |
| `seccomp-confinement-disabled` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/seccomp-confinement-disabled.yaml` |
| `selinux-separation-disabled` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/selinux-separation-disabled.yaml` |
| `writable-filesystem-service` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/writable-filesystem-service.yaml` |

## GITHUB-ACTIONS

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `allowed-unsecure-commands` | `WARNING` | 설정(YAML) 파이프라인 및 가변 인젝션 옵션 단속 점검. | `security/allowed-unsecure-commands.yaml` |
| `curl-eval` | `ERROR` | curl-eval 보안 인젝션 및 런타임 버그 전사 예방 점검. | `security/curl-eval.yaml` |
| `detect-shai-hulud-backdoor` | `ERROR` | detect-shai-hulud-backdoor 보안 인젝션 및 런타임 버그 전사 예방 점검. | `security/detect-shai-hulud-backdoor.yaml` |
| `github-script-injection` | `ERROR` | github-script-injection 보안 인젝션 및 런타임 버그 전사 예방 점검. | `security/github-script-injection.yaml` |
| `pull-request-target-code-checkout` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/pull-request-target-code-checkout.yaml` |
| `run-shell-injection` | `ERROR` | run-shell-injection 보안 인젝션 및 런타임 버그 전사 예방 점검. | `security/run-shell-injection.yaml` |
| `semgrep-github-action-push-without-branches` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `semgrep-configuration/semgrep-github-action-push-without-branches.yml` |
| `third-party-action-not-pinned-to-commit-sha` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/third-party-action-not-pinned-to-commit-sha.yml` |
| `unsafe-add-mask-workflow-command` | `WARNING` | 설정(YAML) 파이프라인 및 가변 인젝션 옵션 단속 점검. | `security/audit/unsafe-add-mask-workflow-command.yaml` |
| `workflow-run-target-code-checkout` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/workflow-run-target-code-checkout.yaml` |

## GITLAB

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `changes-with-when-never` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `correctness/changes-with-when-never.yaml` |

## KUBERNETES

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `allow-privilege-escalation` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/allow-privilege-escalation.yaml` |
| `allow-privilege-escalation-no-securitycontext` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/allow-privilege-escalation-no-securitycontext.yaml` |
| `allow-privilege-escalation-true` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/allow-privilege-escalation-true.yaml` |
| `exposing-docker-socket-hostpath` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/exposing-docker-socket-hostpath.yaml` |
| `flask-debugging-enabled` | `WARNING` | 설정(YAML) 파이프라인 및 가변 인젝션 옵션 단속 점검. | `security/env/flask-debugging-enabled.yaml` |
| `hostipc-pod` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/hostipc-pod.yaml` |
| `hostnetwork-pod` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/hostnetwork-pod.yaml` |
| `hostpid-pod` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/hostpid-pod.yaml` |
| `legacy-api-clusterrole-excessive-permissions` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/legacy-api-clusterrole-excessive-permissions.yaml` |
| `no-fractional-cpu-limits` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `best-practice/no-fractional-cpu-limits.yaml` |
| `privileged-container` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/privileged-container.yaml` |
| `run-as-non-root` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/run-as-non-root.yaml` |
| `run-as-non-root-container-level` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/run-as-non-root-container-level.yaml` |
| `run-as-non-root-container-level-missing-security-context` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/run-as-non-root-container-level-missing-security-context.yaml` |
| `run-as-non-root-security-context-pod-level` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/run-as-non-root-security-context-pod-level.yaml` |
| `run-as-non-root-unsafe-value` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/run-as-non-root-unsafe-value.yaml` |
| `seccomp-confinement-disabled` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/seccomp-confinement-disabled.yaml` |
| `secrets-in-config-file` | `WARNING` | 자격증명/보안 기밀 문자열 누락 여부 점검. | `security/secrets-in-config-file.yaml` |
| `skip-tls-verify-cluster` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/skip-tls-verify-cluster.yaml` |
| `skip-tls-verify-service` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/skip-tls-verify-service.yaml` |
| `writable-filesystem-container` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/writable-filesystem-container.yaml` |

## OPENAPI

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `api-key-in-query-parameter` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/api-key-in-query-parameter.yaml` |
| `openai-consequential-action-false` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `security/openai-consequential-action-false.yaml` |
| `use-of-basic-authentication` | `ERROR` | use-of-basic-authentication 보안 인젝션 및 런타임 버그 전사 예방 점검. | `security/use-of-basic-authentication.yaml` |

## SEMGREP

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `$ID` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `interfile-true-under-metadata-and-no-options.yaml` |
| `$ID` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `interfile-true-under-metadata-and-options-already-present.yaml` |
| `$RULEID` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `metadata-category.yaml` |
| `$RULEID` | `WARNING` | This rule does not have a message. Semgrep requires that rules have a message. I... | `missing-message-field.yaml` |
| `$RULEID` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `missing-language-field.yaml` |
| `$X` | `ERROR` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `duplicate-id.yaml` |
| `duplicate-pattern` | `ERROR` | Semgrep 규칙 저작 메타 데이터 정합성 점검: duplicate-pattern 누락 경보. | `duplicate-pattern.yaml` |
| `empty-message` | `WARNING` | This rule has an empty message field. Consider adding a message field that commu... | `empty-message.yaml` |
| `lang-consistency-bash` | `WARNING` | Found '$X' in language config which diverges from semgrep.dev normalization. | `consistency/lang-consistency-bash.yaml` |
| `lang-consistency-cpp` | `WARNING` | Found '$X' in language config which diverges from semgrep.dev normalization. | `consistency/lang-consistency-cpp.yaml` |
| `lang-consistency-csharp` | `WARNING` | Found '$X' in language config which diverges from semgrep.dev normalization. | `consistency/lang-consistency-csharp.yaml` |
| `lang-consistency-dockerfile` | `WARNING` | Found '$X' in language config which diverges from semgrep.dev normalization. | `consistency/lang-consistency-dockerfile.yaml` |
| `lang-consistency-elixir` | `WARNING` | Found '$X' in language config which diverges from semgrep.dev normalization. | `consistency/lang-consistency-elixir.yaml` |
| `lang-consistency-go` | `WARNING` | Found '$X' in language config which diverges from semgrep.dev normalization. | `consistency/lang-consistency-go.yaml` |
| `lang-consistency-hcl` | `WARNING` | Found '$X' in language config which diverges from semgrep.dev normalization. | `consistency/lang-consistency-hcl.yaml` |
| `lang-consistency-js` | `WARNING` | Found '$X' in language config which diverges from semgrep.dev normalization. | `consistency/lang-consistency-js.yaml` |
| `lang-consistency-kotlin` | `WARNING` | Found '$X' in language config which diverges from semgrep.dev normalization. | `consistency/lang-consistency-kotlin.yaml` |
| `lang-consistency-python` | `WARNING` | Found '$X' in language config which diverges from semgrep.dev normalization. | `consistency/lang-consistency-python.yaml` |
| `lang-consistency-regex` | `WARNING` | Found '$X' in language config which diverges from semgrep.dev normalization. | `consistency/lang-consistency-regex.yaml` |
| `lang-consistency-solidity` | `WARNING` | Found '$X' in language config which diverges from semgrep.dev normalization. | `consistency/lang-consistency-solidity.yaml` |
| `lang-consistency-ts` | `WARNING` | Found '$X' in language config which diverges from semgrep.dev normalization. | `consistency/lang-consistency-ts.yaml` |
| `message-whitespace-check` | `WARNING` | It looks like you have an additional space in your rule message, this can look a... | `message-whitespace.yaml` |
| `metadata-confidence` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `metadata-confidence.yaml` |
| `metadata-confidence-incorrect-value` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `metadata-confidence-incorrect-value.yaml` |
| `metadata-cwe` | `ERROR` | Semgrep 규칙 저작 메타 데이터 정합성 점검: metadata-cwe 누락 경보. | `metadata-cwe.yaml` |
| `metadata-cwe-prohibited-or-discouraged` | `ERROR` | Semgrep 규칙 저작 메타 데이터 정합성 점검: metadata-cwe-prohibited-or-discouraged 누락 경보. | `metadata-cwe-prohibited-or-discouraged.yaml` |
| `metadata-deepsemgrep` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `metadata-deepsemgrep.yaml` |
| `metadata-impact` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `metadata-impact.yaml` |
| `metadata-impact-incorrect-value` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `metadata-impact-incorrect-value.yaml` |
| `metadata-incorrect-option` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `metadata-incorrect-option.yaml` |
| `metadata-license` | `ERROR` | Semgrep 규칙 저작 메타 데이터 정합성 점검: metadata-license 누락 경보. | `metadata-license.yaml` |
| `metadata-likelihood` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `metadata-likelihood.yaml` |
| `metadata-likelihood-incorrect-value` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `metadata-likelihood-incorrect-value.yaml` |
| `metadata-owasp` | `ERROR` | Semgrep 규칙 저작 메타 데이터 정합성 점검: metadata-owasp 누락 경보. | `metadata-owasp.yaml` |
| `metadata-references` | `ERROR` | Semgrep 규칙 저작 메타 데이터 정합성 점검: metadata-references 누락 경보. | `metadata-references.yaml` |
| `metadata-subcategory` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `metadata-subcategory.yaml` |
| `metadata-subcategory-incorrect-value` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `metadata-subcategory-incorrect-value.yaml` |
| `metadata-technology` | `INFO` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `metadata-technology.yaml` |
| `missing-deconstructed-value` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `rule-missing-deconstructed-value.yaml` |
| `multi-line-message` | `WARNING` | This rule has a multi-line message field, which may display poorly in a terminal... | `multi-line-message.yaml` |
| `slow-pattern-general-func` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `slow-pattern-general-function.yaml` |
| `slow-pattern-general-property` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `slow-pattern-general-property.yaml` |
| `slow-pattern-single-metavariable` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `slow-pattern-single-metavariable.yaml` |
| `slow-pattern-top-ellipsis` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `slow-pattern-top-ellipsis.yaml` |
| `unnecessary-parent-operator` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `unnecessary-parent.yaml` |
| `unsatisfiable-rule` | `ERROR` | Semgrep 규칙 저작 메타 데이터 정합성 점검: unsatisfiable-rule 누락 경보. | `unsatisfiable.yaml` |
| `yaml-key-indentation-check` | `WARNING` | 안전하지 않은 코드 패턴이 발견되었습니다. 보안 취약점을 방지하기 위해 코드를 점검하고 수정해 주십시오. | `key-indentation.yaml` |
