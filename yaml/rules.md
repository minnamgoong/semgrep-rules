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
| `exposing-docker-socket-volume` | `WARNING` | exposing-docker-socket-volume 잠재적 결함 및 보안 이격율 정비 요망. | `security/exposing-docker-socket-volume.yaml` |
| `no-new-privileges` | `WARNING` | no-new-privileges 잠재적 결함 및 보안 이격율 정비 요망. | `security/no-new-privileges.yaml` |
| `privileged-service` | `WARNING` | privileged-service 잠재적 결함 및 보안 이격율 정비 요망. | `security/privileged-service.yaml` |
| `seccomp-confinement-disabled` | `WARNING` | seccomp-confinement-disabled 잠재적 결함 및 보안 이격율 정비 요망. | `security/seccomp-confinement-disabled.yaml` |
| `selinux-separation-disabled` | `WARNING` | selinux-separation-disabled 잠재적 결함 및 보안 이격율 정비 요망. | `security/selinux-separation-disabled.yaml` |
| `writable-filesystem-service` | `WARNING` | writable-filesystem-service 잠재적 결함 및 보안 이격율 정비 요망. | `security/writable-filesystem-service.yaml` |

## GITHUB-ACTIONS

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `allowed-unsecure-commands` | `WARNING` | 설정(YAML) 파이프라인 및 가변 인젝션 옵션 단속 점검. | `security/allowed-unsecure-commands.yaml` |
| `curl-eval` | `ERROR` | curl-eval 보안 인젝션 및 런타임 버그 전사 예방 점검. | `security/curl-eval.yaml` |
| `detect-shai-hulud-backdoor` | `ERROR` | detect-shai-hulud-backdoor 보안 인젝션 및 런타임 버그 전사 예방 점검. | `security/detect-shai-hulud-backdoor.yaml` |
| `github-script-injection` | `ERROR` | github-script-injection 보안 인젝션 및 런타임 버그 전사 예방 점검. | `security/github-script-injection.yaml` |
| `pull-request-target-code-checkout` | `WARNING` | pull-request-target-code-checkout 잠재적 결함 및 보안 이격율 정비 요망. | `security/pull-request-target-code-checkout.yaml` |
| `run-shell-injection` | `ERROR` | run-shell-injection 보안 인젝션 및 런타임 버그 전사 예방 점검. | `security/run-shell-injection.yaml` |
| `semgrep-github-action-push-without-branches` | `WARNING` | semgrep-github-action-push-without-branches 잠재적 결함 및 보안 이격율 정비 요망. | `semgrep-configuration/semgrep-github-action-push-without-branches.yml` |
| `third-party-action-not-pinned-to-commit-sha` | `WARNING` | third-party-action-not-pinned-to-commit-sha 잠재적 결함 및 보안 이격율 정비 요망. | `security/third-party-action-not-pinned-to-commit-sha.yml` |
| `unsafe-add-mask-workflow-command` | `WARNING` | 설정(YAML) 파이프라인 및 가변 인젝션 옵션 단속 점검. | `security/audit/unsafe-add-mask-workflow-command.yaml` |
| `workflow-run-target-code-checkout` | `WARNING` | workflow-run-target-code-checkout 잠재적 결함 및 보안 이격율 정비 요망. | `security/workflow-run-target-code-checkout.yaml` |

## GITLAB

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `changes-with-when-never` | `WARNING` | changes-with-when-never 잠재적 결함 및 보안 이격율 정비 요망. | `correctness/changes-with-when-never.yaml` |

## KUBERNETES

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `allow-privilege-escalation` | `WARNING` | allow-privilege-escalation 잠재적 결함 및 보안 이격율 정비 요망. | `security/allow-privilege-escalation.yaml` |
| `allow-privilege-escalation-no-securitycontext` | `WARNING` | allow-privilege-escalation-no-securitycontext 잠재적 결함 및 보안 이격율 정비 요망. | `security/allow-privilege-escalation-no-securitycontext.yaml` |
| `allow-privilege-escalation-true` | `WARNING` | allow-privilege-escalation-true 잠재적 결함 및 보안 이격율 정비 요망. | `security/allow-privilege-escalation-true.yaml` |
| `exposing-docker-socket-hostpath` | `WARNING` | exposing-docker-socket-hostpath 잠재적 결함 및 보안 이격율 정비 요망. | `security/exposing-docker-socket-hostpath.yaml` |
| `flask-debugging-enabled` | `WARNING` | 설정(YAML) 파이프라인 및 가변 인젝션 옵션 단속 점검. | `security/env/flask-debugging-enabled.yaml` |
| `hostipc-pod` | `WARNING` | hostipc-pod 잠재적 결함 및 보안 이격율 정비 요망. | `security/hostipc-pod.yaml` |
| `hostnetwork-pod` | `WARNING` | hostnetwork-pod 잠재적 결함 및 보안 이격율 정비 요망. | `security/hostnetwork-pod.yaml` |
| `hostpid-pod` | `WARNING` | hostpid-pod 잠재적 결함 및 보안 이격율 정비 요망. | `security/hostpid-pod.yaml` |
| `legacy-api-clusterrole-excessive-permissions` | `WARNING` | legacy-api-clusterrole-excessive-permissions 잠재적 결함 및 보안 이격율 정비 요망. | `security/legacy-api-clusterrole-excessive-permissions.yaml` |
| `no-fractional-cpu-limits` | `WARNING` | no-fractional-cpu-limits 잠재적 결함 및 보안 이격율 정비 요망. | `best-practice/no-fractional-cpu-limits.yaml` |
| `privileged-container` | `WARNING` | privileged-container 잠재적 결함 및 보안 이격율 정비 요망. | `security/privileged-container.yaml` |
| `run-as-non-root` | `INFO` | run-as-non-root 잠재적 결함 및 보안 이격율 정비 요망. | `security/run-as-non-root.yaml` |
| `run-as-non-root-container-level` | `INFO` | run-as-non-root-container-level 잠재적 결함 및 보안 이격율 정비 요망. | `security/run-as-non-root-container-level.yaml` |
| `run-as-non-root-container-level-missing-security-context` | `INFO` | run-as-non-root-container-level-missing-security-context 잠재적 결함 및 보안 이격율 정비 요망. | `security/run-as-non-root-container-level-missing-security-context.yaml` |
| `run-as-non-root-security-context-pod-level` | `INFO` | run-as-non-root-security-context-pod-level 잠재적 결함 및 보안 이격율 정비 요망. | `security/run-as-non-root-security-context-pod-level.yaml` |
| `run-as-non-root-unsafe-value` | `INFO` | run-as-non-root-unsafe-value 잠재적 결함 및 보안 이격율 정비 요망. | `security/run-as-non-root-unsafe-value.yaml` |
| `seccomp-confinement-disabled` | `WARNING` | seccomp-confinement-disabled 잠재적 결함 및 보안 이격율 정비 요망. | `security/seccomp-confinement-disabled.yaml` |
| `secrets-in-config-file` | `WARNING` | 자격증명/보안 기밀 문자열 누사 점검. | `security/secrets-in-config-file.yaml` |
| `skip-tls-verify-cluster` | `WARNING` | skip-tls-verify-cluster 잠재적 결함 및 보안 이격율 정비 요망. | `security/skip-tls-verify-cluster.yaml` |
| `skip-tls-verify-service` | `WARNING` | skip-tls-verify-service 잠재적 결함 및 보안 이격율 정비 요망. | `security/skip-tls-verify-service.yaml` |
| `writable-filesystem-container` | `WARNING` | writable-filesystem-container 잠재적 결함 및 보안 이격율 정비 요망. | `security/writable-filesystem-container.yaml` |

## OPENAPI

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `api-key-in-query-parameter` | `WARNING` | api-key-in-query-parameter 잠재적 결함 및 보안 이격율 정비 요망. | `security/api-key-in-query-parameter.yaml` |
| `openai-consequential-action-false` | `WARNING` | openai-consequential-action-false 잠재적 결함 및 보안 이격율 정비 요망. | `security/openai-consequential-action-false.yaml` |
| `use-of-basic-authentication` | `ERROR` | use-of-basic-authentication 보안 인젝션 및 런타임 버그 전사 예방 점검. | `security/use-of-basic-authentication.yaml` |

## SEMGREP

| Rule ID | Severity | Summary | Path |
| :--- | :---: | :--- | :--- |
| `$ID` | `WARNING` | $ID 잠재적 결함 및 보안 이격율 정비 요망. | `interfile-true-under-metadata-and-no-options.yaml` |
| `$ID` | `WARNING` | $ID 잠재적 결함 및 보안 이격율 정비 요망. | `interfile-true-under-metadata-and-options-already-present.yaml` |
| `$RULEID` | `INFO` | metadata-category 잠재적 결함 및 보안 이격율 정비 요망. | `metadata-category.yaml` |
| `$RULEID` | `WARNING` | This rule does not have a message. Semgrep requires that rules have a message. I... | `missing-message-field.yaml` |
| `$RULEID` | `WARNING` | missing-language-field 잠재적 결함 및 보안 이격율 정비 요망. | `missing-language-field.yaml` |
| `$X` | `ERROR` | $X 잠재적 결함 및 보안 이격율 정비 요망. | `duplicate-id.yaml` |
| `duplicate-pattern` | `ERROR` | Semgrep 규칙 저작 메타 데이터 정합성 점검: duplicate-pattern 누사 경보. | `duplicate-pattern.yaml` |
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
| `metadata-confidence` | `WARNING` | metadata-confidence 잠재적 결함 및 보안 이격율 정비 요망. | `metadata-confidence.yaml` |
| `metadata-confidence-incorrect-value` | `WARNING` | metadata-confidence-incorrect-value 잠재적 결함 및 보안 이격율 정비 요망. | `metadata-confidence-incorrect-value.yaml` |
| `metadata-cwe` | `ERROR` | Semgrep 규칙 저작 메타 데이터 정합성 점검: metadata-cwe 누사 경보. | `metadata-cwe.yaml` |
| `metadata-cwe-prohibited-or-discouraged` | `ERROR` | Semgrep 규칙 저작 메타 데이터 정합성 점검: metadata-cwe-prohibited-or-discouraged 누사 경보. | `metadata-cwe-prohibited-or-discouraged.yaml` |
| `metadata-deepsemgrep` | `WARNING` | metadata-deepsemgrep 잠재적 결함 및 보안 이격율 정비 요망. | `metadata-deepsemgrep.yaml` |
| `metadata-impact` | `WARNING` | metadata-impact 잠재적 결함 및 보안 이격율 정비 요망. | `metadata-impact.yaml` |
| `metadata-impact-incorrect-value` | `WARNING` | metadata-impact-incorrect-value 잠재적 결함 및 보안 이격율 정비 요망. | `metadata-impact-incorrect-value.yaml` |
| `metadata-incorrect-option` | `INFO` | metadata-incorrect-option 잠재적 결함 및 보안 이격율 정비 요망. | `metadata-incorrect-option.yaml` |
| `metadata-license` | `ERROR` | Semgrep 규칙 저작 메타 데이터 정합성 점검: metadata-license 누사 경보. | `metadata-license.yaml` |
| `metadata-likelihood` | `WARNING` | metadata-likelihood 잠재적 결함 및 보안 이격율 정비 요망. | `metadata-likelihood.yaml` |
| `metadata-likelihood-incorrect-value` | `WARNING` | metadata-likelihood-incorrect-value 잠재적 결함 및 보안 이격율 정비 요망. | `metadata-likelihood-incorrect-value.yaml` |
| `metadata-owasp` | `ERROR` | Semgrep 규칙 저작 메타 데이터 정합성 점검: metadata-owasp 누사 경보. | `metadata-owasp.yaml` |
| `metadata-references` | `ERROR` | Semgrep 규칙 저작 메타 데이터 정합성 점검: metadata-references 누사 경보. | `metadata-references.yaml` |
| `metadata-subcategory` | `WARNING` | metadata-subcategory 잠재적 결함 및 보안 이격율 정비 요망. | `metadata-subcategory.yaml` |
| `metadata-subcategory-incorrect-value` | `WARNING` | metadata-subcategory-incorrect-value 잠재적 결함 및 보안 이격율 정비 요망. | `metadata-subcategory-incorrect-value.yaml` |
| `metadata-technology` | `INFO` | metadata-technology 잠재적 결함 및 보안 이격율 정비 요망. | `metadata-technology.yaml` |
| `missing-deconstructed-value` | `WARNING` | missing-deconstructed-value 잠재적 결함 및 보안 이격율 정비 요망. | `rule-missing-deconstructed-value.yaml` |
| `multi-line-message` | `WARNING` | This rule has a multi-line message field, which may display poorly in a terminal... | `multi-line-message.yaml` |
| `slow-pattern-general-func` | `WARNING` | slow-pattern-general-func 잠재적 결함 및 보안 이격율 정비 요망. | `slow-pattern-general-function.yaml` |
| `slow-pattern-general-property` | `WARNING` | slow-pattern-general-property 잠재적 결함 및 보안 이격율 정비 요망. | `slow-pattern-general-property.yaml` |
| `slow-pattern-single-metavariable` | `WARNING` | slow-pattern-single-metavariable 잠재적 결함 및 보안 이격율 정비 요망. | `slow-pattern-single-metavariable.yaml` |
| `slow-pattern-top-ellipsis` | `WARNING` | slow-pattern-top-ellipsis 잠재적 결함 및 보안 이격율 정비 요망. | `slow-pattern-top-ellipsis.yaml` |
| `unnecessary-parent-operator` | `WARNING` | unnecessary-parent-operator 잠재적 결함 및 보안 이격율 정비 요망. | `unnecessary-parent.yaml` |
| `unsatisfiable-rule` | `ERROR` | Semgrep 규칙 저작 메타 데이터 정합성 점검: unsatisfiable-rule 누사 경보. | `unsatisfiable.yaml` |
| `yaml-key-indentation-check` | `WARNING` | yaml-key-indentation-check 잠재적 결함 및 보안 이격율 정비 요망. | `key-indentation.yaml` |
