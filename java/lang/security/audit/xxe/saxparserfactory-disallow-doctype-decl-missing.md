# saxparserfactory-disallow-doctype-decl-missing (SAX Parser DOCTYPE 금지 누락)

## 개요
SAXParserFactory 초기화 시 disallow-doctype-decl 선언 설정이 누락되었습니다. XXE 공격 창구를 원천 차단하기 위해 이 특성을 활성화하십시오.

## 위험성
*   SAX 스트림 처리 특성상 로딩 부하는 적으나 엔티티 전개 시 시스템 파일 누설 등 XXE 타격 범위는 동일하게 받습니다.

## 조치 방안
*   해당 팩토리 `setFeature`에 `disallow-doctype-decl` 옵션을 인위적으로 명시해 주십시오 (`true`).
