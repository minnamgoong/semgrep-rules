# unverified-jwt-decode (JWT 검증 누락)
## 개요
JWT 디코딩 시 verify=False 플래그가 발견되었습니다. 무결성 검증을 위해 누출 옵션을 활성화하십시오.
## 조치 방안
*   `verify=True` 또는 검증 메서드를 정적 사용하십시오.
