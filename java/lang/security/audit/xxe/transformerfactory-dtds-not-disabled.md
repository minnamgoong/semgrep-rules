# transformerfactory-dtds-not-disabled (Transformer DTD 비활성화 누락 점검)

## 개요
TransformerFactory에서 DTD 문서 선언 금지 설정이 누락되어 XXE 위험에 노출됩니다. 안전한 XML 가공을 위해 ACCESS_EXTERNAL_DTD 등 비허용 속성을 적용하세요.

## 위험성
*   **XML Bomb / XXE**: 악성 XML의 DTD 전개 공격 시 서버 메모리 고갈 및 중요 리소스 외유가 유발됩니다.

## 조치 방안
*   `setAttribute` 메서드로 `XMLConstants.ACCESS_EXTERNAL_DTD`를 빈 문자열(`""`)로 주입 차단하십시오.
