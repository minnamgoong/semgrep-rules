# sequelize-tls-disabled-cert-validation (인증서 검증 우회 위험)

## 개요
Sequelize 설정 중 인증서 검증을 우회(rejectUnauthorized: false)하는 상태가 감지되었습니다. 중간자 공격에 도출되므로 프로덕션 배포 시 철회하십시오.

## 위험성
*   **MitM 공격**: 데이터베이스와의 통신 구간에서 위조된 SSL 인증서를 수용하게 되어 패킷 도청 사고 확률을 높입니다.

## 조치 방안
*   테스트 단계가 아니라면 옵션을 `true`로 돌리거나 지워서 정적 무결성을 강화하세요.
