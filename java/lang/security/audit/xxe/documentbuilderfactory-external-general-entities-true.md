# documentbuilderfactory-external-general-entities-true (일반 외부 엔티티 활성 경고)

## 개요
DocumentBuilderFactory에서 일반 외부 엔티티 호출이 허용되어 XXE 공격에 취약합니다. 가용 가능한 setFeature로 해당 기능을 비활성화 처리하세요.

## 위험성
*   **XXE**: 파싱 시 외부 파일 인클루드 또는 서버 SSRF 호출 시도로 이어져 심각한 정보 노출을 격발할 수 있습니다.

## 조치 방안
*   해당 Feature 속성을 `false`로 꺼야 합니다.
