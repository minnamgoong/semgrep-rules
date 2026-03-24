# server-dangerous-object-deserialization (RMI 위험 역직렬화)

## 개요
Java RMI(Remote Method Invocation) 통신 엔드포인트에서 객체 역직렬화를 통해 임의 입력값을 유입받는 코드가 포착되었습니다.

## 위험성
*   **Insecure Deserialization (안전하지 않은 역직렬화)**: 공격자가 악성 직렬화 가젯(Gadget) 바이트를 전사하면 원격 코드 실행(RCE) 타격을 즉시 입습니다.

## 조치 방안
*   Java 9 이상에서 지원되는 `ObjectInputFilter`를 구현하여 신뢰할 수 있는 클래스 명단만 역직렬화를 허용(White List)하십시오.
