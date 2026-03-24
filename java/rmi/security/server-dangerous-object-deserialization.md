# server-dangerous-object-deserialization (RMI 위험 역직렬화)

## 개요
RMI 통신 시 임의 객체 수신으로 인한 안전하지 않은 역직렬화 취약점이 가중될 수 있습니다. 허용 클래스 필터링 등을 적용하세요.

## 위험성
*   **Insecure Deserialization (안전하지 않은 역직렬화)**: 공격자가 악성 직렬화 가젯(Gadget) 바이트를 전사하면 원격 코드 실행(RCE) 타격을 즉시 입습니다.

## 조치 방안
*   Java 9 이상에서 지원되는 `ObjectInputFilter`를 구현하여 신뢰할 수 있는 클래스 명단만 역직렬화를 허용(White List)하십시오.
