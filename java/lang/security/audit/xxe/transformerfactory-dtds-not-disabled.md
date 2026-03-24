# transformerfactory-dtds-not-disabled (Transformer DTD 비활성화 누락 점검)

## 개요
XSLT 변환 등을 수행하는 `TransformerFactory` 인스턴스에 외부 DTD 로딩 및 전개 보안 방어가 누락된 국면을 진단합니다.

## 위험성
*   **XML Bomb / XXE**: 악성 XML의 DTD 전개 공격 시 서버 메모리 고갈 및 중요 리소스 외유가 유발됩니다.

## 조치 방안
*   `setAttribute` 메서드로 `XMLConstants.ACCESS_EXTERNAL_DTD`를 빈 문자열(`""`)로 주입 차단하십시오.
