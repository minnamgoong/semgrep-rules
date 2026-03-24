# documentbuilderfactory-external-parameter-entities-true (파라미터 엔티티 보안 경보)

## 개요
DocumentBuilderFactory에서 파라미터형 외부 엔티티 전개 허용이 감지되었습니다. XXE 정보 탈취 피해를 막기 위해 해당 파라미터 허용을 금지하십시오.

## 위험성
*   **XXE**: 공격자가 DTD 자체를 동적으로 호출하여 리소스 응답 덤프를 가로채 피싱하는 고단수 XXE 공격에 쉽게 당하게 됩니다.

## 조치 방안
*   Feature 속성을 `false`로 끄십시오.
