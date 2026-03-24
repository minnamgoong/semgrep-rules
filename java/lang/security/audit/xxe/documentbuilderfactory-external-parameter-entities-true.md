# documentbuilderfactory-external-parameter-entities-true (파라미터 엔티티 보안 경보)

## 개요
`DocumentBuilderFactory`에 파생 엔티티(`http://xml.org/sax/features/external-parameter-entities`) 호출 권한이 켜져 있는 현상을 잡습니다.

## 위험성
*   **XXE**: 공격자가 DTD 자체를 동적으로 호출하여 리소스 응답 덤프를 가로채 피싱하는 고단수 XXE 공격에 쉽게 당하게 됩니다.

## 조치 방안
*   Feature 속성을 `false`로 끄십시오.
