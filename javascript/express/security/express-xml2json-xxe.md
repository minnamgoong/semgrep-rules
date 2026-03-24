# express-xml2json-xxe (XML2JSON XXE 위험 감지)

## 개요
XML Parser로 입력되는 데이터 가공 시 외부 사용자 입력이 유출됩니다. XXE(XML External Entity) 공격 취약점을 유발하므로 파서에 DTD 로딩 및 외부 엔티티 호출을 차단하세요.

## 위험성
*   **XXE (XML External Entity)**: 악의적 DTD 전개 시 서버 임의 파일 누설(File Read), SSRF 등이 발생하여 심대한 피싱 타격을 받습니다.

## 조치 방안
*   파싱 연산 전 단계에서 외부 DTD 참조 기능(`SUPPORT_DTD` 등)을 명시적으로 디스에이블 처리하도록 객체 레이어를 구정하세요.
