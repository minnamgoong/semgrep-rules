# formatted-sql-string (서식 SQL 쿼리 경고)

## 개요
SQL 쿼리 내에서 Formatted String(서식 문자열)이 발견되었습니다. SQL 인젝션 요인을 막기 위해 PreparedStatement 스타일을 적용하세요.

## 위험성
*   구조적으로 문자열 조립 형식과 일맥상통하여, 변수가 직접 대입될 때 조작된 SQL 문법의 영향을 배제하지 못해 전형적 SQL Injection 창구가 됩니다.

## 조치 방안
*   기재된 포매터 연산을 중단하고 표준 Parameterized Query 객체를 고용해 값을 바인딩하십시오.
