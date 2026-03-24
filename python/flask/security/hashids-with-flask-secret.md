# hashids-with-flask-secret (HashIDs Salt 유출 위험)
## 개요
Flask SECRET_KEY를 HashIDs Salt로 오용했습니다. 해시 파싱 중 무력화 위협이 있으니 전용 값을 할당하세요.
## 조치 방안
*   고정된 보조 Salt 상수를 새로 정의하십시오.
