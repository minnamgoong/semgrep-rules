# servletresponse-writer-xss (출력 응답 XSS 위험)

## 개요
서블릿 응답 Stream으로 전달되는 동적 문자열(파라미터 등)이 HTML 문법이나 스크립트 특수문자를 인코딩 없이 전달하는 코드 상태를 탐지합니다.

## 위험성
*   **Stored/Reflected XSS**: 브라우저 로딩 시 불법 세션 하이재킹 Script, 피싱 유도가 가동되어 클라이언트 단 보안이 영구적으로 무력화됩니다.

## 조치 방안
*   출력 전 반드시 `StringEscapeUtils.escapeHtml4()` 등의 안전한 보안 인코더를 둘러싸서 응답 스트림으로 발행하는 버퍼를 두어야 합니다.
