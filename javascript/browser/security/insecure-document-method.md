# insecure-document-method (위험한 도큐먼트 메서드 경보)

## 개요
document.write 또는 innerHTML 에 외부 오염 데이터가 탑재되어 DOM-XSS 위험이 보입니다. 안전한 DOM 트리 생성 메서드로 변경하세요.

## 위험성
*   **DOM Based XSS**: 실행 컨텍스트에 악의 성분이 전사되어 스크립트 주입 성사가 수월해집니다.

## 조치 방안
*   `document.createElement()`, `.appendChild()` 등 객체 지향형 정적 렌더링 API 사용 권장.
