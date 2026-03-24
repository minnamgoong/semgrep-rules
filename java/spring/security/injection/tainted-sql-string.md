# tainted-sql-string (Spring SQL 문자열 결합 인젝션 위험)

## 개요
외부 유입 오염 데이터가 직접 SQL 문자열 조립에 사용되었습니다. SQL 인젝션을 막기 위해 검증된 파라미터형 바인딩 양식을 도출하세요.

## 위험성
*   **SQL Injection**: 외부 파라미터 조작으로 데이터베이스 정보 누설 및 쿼러 바이패스 인증 우회가 직효하게 들어올 수 있습니다.

## 조치 방안
*   JpaRepository, Mapper 바인딩 혹은 JDBCTemplate의 `?` 바인더 스타일을 강제로 가동하도록 변경하세요.
