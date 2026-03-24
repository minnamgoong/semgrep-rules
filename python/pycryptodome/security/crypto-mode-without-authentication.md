# crypto-mode-without-authentication (인증 없는 암호화 모드 위험)
## 개요
CBC, CTR 등 단순 대칭키 암호화 사용 시 메시지 변조 감지 기능이 부재함을 경보합니다.
## 조치 방안
*   `AES.MODE_GCM` 등 AEAD 계열로 전환하십시오.
