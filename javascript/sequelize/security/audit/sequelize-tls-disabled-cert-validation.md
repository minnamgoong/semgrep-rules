# sequelize-tls-disabled-cert-validation (인증서 검증 우회 위험)

## 개요
Sequelize ORM 설정 객체의 TLS/SSL 연결 옵션에서 `rejectUnauthorized: false`를 사용하는 국면을 적축합니다.

## 위험성
*   **MitM 공격**: 데이터베이스와의 통신 구간에서 위조된 SSL 인증서를 수용하게 되어 패킷 도청 사고 확률을 높입니다.

## 조치 방안
*   테스트 단계가 아니라면 옵션을 `true`로 돌리거나 지워서 정적 무결성을 강화하세요.
