# xmlinputfactory-external-entities-enabled (XXE 취약 설정 감지)

## 개요
XMLInputFactory에 외부 엔티티(External Entities)가 허용되어 있습니다. XML External Entity (XXE) 취약점 발생을 예방하기 위해 이를 비활성화하세요.

## 위험성
*   **XXE (XML External Entity)**: 악성 XML 업로드 유포 시 서버 측 파일 임의 누설(File Read), 내부 시스템 SSRF 피싱 등을 당할 리스크가 극히 큽니다.

## 조치 방안
*   파서 인스턴스 초기화 라인에 아래와 같이 `SUPPORT_DTD` 및 `IS_SUPPORTING_EXTERNAL_ENTITIES` 속성을 `false`로 주입하세요.

```java
xmlInputFactory.setProperty(XMLInputFactory.SUPPORT_DTD, false);
xmlInputFactory.setProperty(XMLInputFactory.IS_SUPPORTING_EXTERNAL_ENTITIES, false);
```
