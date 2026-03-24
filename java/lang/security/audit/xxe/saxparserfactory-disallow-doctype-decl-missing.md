# saxparserfactory-disallow-doctype-decl-missing (SAX Parser DOCTYPE 금지 누락)

## 개요
SAX 방식의 대용량 XML 처리를 담당하는 `SAXParserFactory` 도구에서 DTD 선언 파쇄 방직이 비어있음을 점검합니다.

## 위험성
*   SAX 스트림 처리 특성상 로딩 부하는 적으나 엔티티 전개 시 시스템 파일 누설 등 XXE 타격 범위는 동일하게 받습니다.

## 조치 방안
*   해당 팩토리 `setFeature`에 `disallow-doctype-decl` 옵션을 인위적으로 명시해 주십시오 (`true`).
