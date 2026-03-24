# grpc-nodejs-insecure-connection (안전하지 않은 gRPC 연결 감지)

## 개요
gRPC 연결 생성 시 암호화되지 않은 안전하지 않은 채널(createInsecure())이 사용되었습니다. 중간자 공격(MitM) 등에 무방비하므로 SSL/TLS 보완책을 적용하십시오.

## 위험성
*   **중간자 공격 (MitM)**: gRPC 메시지에 포함된 개인정보, 토큰, 비즈니스 정보가 평문으로 중계되어 트래픽 스니핑 공격에 전방 노출됩니다.

## 조치 방안
*   보안 인증서(`SslCredentials` 등)를 기반으로 `createSsl()` 채널을 가동해야 합니다.
