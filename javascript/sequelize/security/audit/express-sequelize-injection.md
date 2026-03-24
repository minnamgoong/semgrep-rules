# express-sequelize-injection (Sequelize SQL 인젝션 경보)

## 개요
Sequelize의 Raw Queries 가동 시 가변 문자열 인자를 백엔드 대입하는 현상을 잡습니다.

## 위험성
*   ORM 기용 목적에 상반되는 직접 인젝션 창구가 열리게 됩니다.

## 조치 방안
*   `sequelize.query(..., { replacements: { id: input } })` 체제를 고수하세요.
