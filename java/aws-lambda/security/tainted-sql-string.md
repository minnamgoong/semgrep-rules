# tainted-sql-string (Lambda SQL 인젝션 위험)

## 개요
AWS Lambda 핸들러 등의 외부 사용자 입력이 직접 SQL 문자열 조립에 사용되었습니다. Parameterized Query를 사용하여 SQL 인젝션을 예방하세요.

## 위험성
*   역사적으로 가벼운 스크립팅이나 마이크로서비스에서 자주 간과되는 보안 허점으로, 주입 시 Database 파기와 시스템 덤프를 초래할 수 있습니다.

## 조치 방안
*   바인딩 전용 파라미터형 바인딩 처리(예: `Statement` 대신 `PreparedStatement`)를 필수 설계하십시오.
