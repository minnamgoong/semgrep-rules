# insecure-document-method (위험한 도큐먼트 메서드 경보)

## 개요
`document.write()`, `document.writeln()`을 통해 동적 문자열을 브라우저 뷰 버퍼로 직접 미는 행위를 감지합니다.

## 위험성
*   **DOM Based XSS**: 실행 컨텍스트에 악의 성분이 전사되어 스크립트 주입 성사가 수월해집니다.

## 조치 방안
*   `document.createElement()`, `.appendChild()` 등 객체 지향형 정적 렌더링 API 사용 권장.
