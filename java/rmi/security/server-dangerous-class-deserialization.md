# server-dangerous-class-deserialization (Java WARNING 경보)

## 개요
안전하지 않은 역직렬화 가동이 포착되었습니다. RCE 공격 차단을 위해 직렬화 파서를 격수하십시오.

## 조치 방안
*   해당 메서드 호출 인자를 화이트리스트 고정하거나 규격화 하십시오.
