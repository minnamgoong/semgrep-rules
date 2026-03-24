# unverified-jwt-decode (JWT 검증 누락)
## 개요
디코드 호출 시 비밀키 검증을 스킵하도록 선언된 상황을 경보합니다.
## 조치 방안
*   `verify=True` 또는 검증 메서드를 정적 사용하십시오.
