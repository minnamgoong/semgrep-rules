# tainted-sql-string (Spring SQL 문자열 결합 인젝션 위험)

## 개요
Spring 계층(Controller 등)에서 주입받은 유저 파라미터가 DAO/Repository 단의 네이티브 SQL 쿼리 문자열 조립에 그대로 끼어드는 것을 경보합니다.

## 위험성
*   **SQL Injection**: 외부 파라미터 조작으로 데이터베이스 정보 누설 및 쿼러 바이패스 인증 우회가 직효하게 들어올 수 있습니다.

## 조치 방안
*   JpaRepository, Mapper 바인딩 혹은 JDBCTemplate의 `?` 바인더 스타일을 강제로 가동하도록 변경하세요.
