# cookie-missing-httponly (Java WARNING 경보)

## 개요
쿠키에 보안 속성(Secure/HttpOnly)이 누락되어 세션 탈취(XSS/MitM)에 노출될 수 있습니다.

## 조치 방안
*   해당 메서드 호출 인자를 화이트리스트 고정하거나 규격화 하십시오.
