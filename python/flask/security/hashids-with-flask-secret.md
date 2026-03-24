# hashids-with-flask-secret (HashIDs Salt 유출 위험)
## 개요
중요 비밀키를 Salt로 쓸 경우 인코딩 정합 시 대형 스니핑 단서로 잡힙니다.
## 조치 방안
*   고정된 보조 Salt 상수를 새로 정의하십시오.
