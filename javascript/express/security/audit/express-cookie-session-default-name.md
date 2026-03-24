# express-cookie-session-default-name

## 개요
Don’t use the default session cookie name Using the default session cookie name can open your app to attacks. The security issue posed is similar to X-Powered-By: a potential attacker can use it to fingerprint the server and target attacks accordingly. languages: [javascript, typescript] metadata: cwe: - 'CWE-522: Insufficiently Protected Credentials' owasp: - A02:2017 - Broken Authentication - A04:2021 - Insecure Design - A06:2025 - Insecure Design source-rule-url: https://expressjs.com/en/advanced/best-practice-security.html category: security technology: - express cwe2021-top25: true subcategory: - vuln likelihood: HIGH impact: LOW confidence: MEDIUM references: - https://owasp.org/Top10/A04_2021-Insecure_Design patterns: - pattern-either: - pattern-inside: | $SESSION = require('cookie-session'); ... - pattern-inside: | $SESSION = require('express-session'); ... - pattern: $SESSION(...) - pattern-not-inside: $SESSION(<... {name:...} ...>,...) - pattern-not-inside: | $OPTS = <... {name:...} ...>; ... $SESSION($OPTS,...); - pattern-not-inside: | $OPTS = ...; ... $OPTS.name = ...; ... $SESSION($OPTS,...);

## 취약점 등급
🟡 MEDIUM

## 관련 규칙 파일
`express/security/audit/express-cookie-settings.yaml`
