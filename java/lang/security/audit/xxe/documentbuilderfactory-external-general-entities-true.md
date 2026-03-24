# documentbuilderfactory-external-general-entities-true (일반 외부 엔티티 활성 경고)

## 개요
XML Parser 제작 전용 팩토리 객체에서 구조적 일반 엔티티 허용 속성(`http://xml.org/sax/features/external-general-entities`)이 켜진 상황을 포착합니다.

## 위험성
*   **XXE**: 파싱 시 외부 파일 인클루드 또는 서버 SSRF 호출 시도로 이어져 심각한 정보 노출을 격발할 수 있습니다.

## 조치 방안
*   해당 Feature 속성을 `false`로 꺼야 합니다.
