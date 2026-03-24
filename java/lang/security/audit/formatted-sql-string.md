# formatted-sql-string (서식 SQL 쿼리 경고)

## 개요
`String.format()` 혹은 `%s` 같은 형식의 서식 마크업을 동원해 SQL 전체를 동적 구성해 사용하는 패턴을 경고합니다.

## 위험성
*   구조적으로 문자열 조립 형식과 일맥상통하여, 변수가 직접 대입될 때 조작된 SQL 문법의 영향을 배제하지 못해 전형적 SQL Injection 창구가 됩니다.

## 조치 방안
*   기재된 포매터 연산을 중단하고 표준 Parameterized Query 객체를 고용해 값을 바인딩하십시오.
