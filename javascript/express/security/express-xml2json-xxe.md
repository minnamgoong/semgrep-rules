# express-xml2json-xxe (XML2JSON XXE 위험 감지)

## 개요
동적 XML 문자열 처리용 라이브러리 연산 단계에 사용자 통제 데이터가 전개 전에 주입되는 국면을 적축합니다.

## 위험성
*   **XXE (XML External Entity)**: 악의적 DTD 전개 시 서버 임의 파일 누설(File Read), SSRF 등이 발생하여 심대한 피싱 타격을 받습니다.

## 조치 방안
*   파싱 연산 전 단계에서 외부 DTD 참조 기능(`SUPPORT_DTD` 등)을 명시적으로 디스에이블 처리하도록 객체 레이어를 구정하세요.
