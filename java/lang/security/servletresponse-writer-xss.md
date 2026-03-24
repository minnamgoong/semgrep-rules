# servletresponse-writer-xss (출력 응답 XSS 위험)

## 개요
HttpServletResponse writer에 사용자 입력이 그대로 출력돼 XSS가 우려됩니다. 출력 전 HTML 인코딩을 적용하거나 보안 전용 API를 사용하세요.

## 위험성
*   **Stored/Reflected XSS**: 브라우저 로딩 시 불법 세션 하이재킹 Script, 피싱 유도가 가동되어 클라이언트 단 보안이 영구적으로 무력화됩니다.

## 조치 방안
*   출력 전 반드시 `StringEscapeUtils.escapeHtml4()` 등의 안전한 보안 인코더를 둘러싸서 응답 스트림으로 발행하는 버퍼를 두어야 합니다.
