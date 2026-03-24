# tainted-sql-string (Express SQL 인젝션 경보)

## 개요
동적 SQL 문자열 결합이 탐지되었습니다. SQL Injection 예방을 위해 객체 모델 바인딩 및 Parameterized Query 기법을 사용하세요.

## 위험성
*   **SQL Injection**: 외부 변수 조작으로 데이터베이스 정보 누설 및 쿼리 우회 인증 파훼가 성사될 심각한 리스크가 탑재됩니다.

## 조치 방안
*   ORM(Sequelize, TypeORM 등)의 규격화된 바인딩 형태나 드라이버 파라미터형 바인더를 이용하십시오.
