# documentbuilderfactory-disallow-doctype-decl-missing (DOCTYPE 금지 누락 감지)

## 개요
`DocumentBuilderFactory` 선언 시 XXE의 원천 방어막인 `disallow-doctype-decl` 세부 셋이 누락되었음을 보고합니다.

## 위험성
*   기본 XML 처리 스펙에서 DTD 선언을 용인하므로 악성 코드가 서버에서 처리될 공산을 남겨둡니다.

## 조치 방안
*   `factory.setFeature("http://apache.org/xml/features/disallow-doctype-decl", true);` 적용 필수.
