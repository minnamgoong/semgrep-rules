# documentbuilderfactory-disallow-doctype-decl-missing (DOCTYPE 금지 누락 감지)

## 개요
DocumentBuilderFactory 초기화 시 DISALLOW_DOCTYPE_DECL 선언이 누락되었습니다. XXE 및 DTD 부하 공격을 방어하기 위해 이를 true로 셋업하세요.

## 위험성
*   기본 XML 처리 스펙에서 DTD 선언을 용인하므로 악성 코드가 서버에서 처리될 공산을 남겨둡니다.

## 조치 방안
*   `factory.setFeature("http://apache.org/xml/features/disallow-doctype-decl", true);` 적용 필수.
