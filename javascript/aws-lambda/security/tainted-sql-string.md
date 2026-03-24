# tainted-sql-string (Lambda SQL 인젝션 방어)

## 개요
Lambda 가동 연산 스택에 유저 기반 SQL 문자열 조립이 탐지되었습니다. Parameterized Query를 사용하여 인젝션 요인을 차단하십시오.

## 위험성
*   **SQL Injection**: 유입 데이터 규정 한도를 가리지 못할 경우 database 덤핑 및 백엔드 트래픽 정지 유발 리스크를 가중시킵니다.

## 조치 방안
*   바인딩 전용 파라미터형 처리 레이어를 필수로 부착하십시오.
