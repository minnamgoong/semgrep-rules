# grpc-nodejs-insecure-connection (안전하지 않은 gRPC 연결 감지)

## 개요
Node.js gRPC 클라이언트 호출 시 암호화 보안층을 마련하지 않는 `createInsecure()` 채널 생성자를 구동하는 코드를 진단합니다.

## 위험성
*   **중간자 공격 (MitM)**: gRPC 메시지에 포함된 개인정보, 토큰, 비즈니스 정보가 평문으로 중계되어 트래픽 스니핑 공격에 전방 노출됩니다.

## 조치 방안
*   보안 인증서(`SslCredentials` 등)를 기반으로 `createSsl()` 채널을 가동해야 합니다.
