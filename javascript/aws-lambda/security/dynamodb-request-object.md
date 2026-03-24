# dynamodb-request-object (DynamoDB NoSQL 인젝션 위험)

## 개요
Lambda의 유입 이벤트 객체(`$EVENT`) 내용물이 통과 여과 없이 DynamoDB의 `query()`, `scan()` 조건문 필터 객체 안으로 직유입되는 것을 경보합니다.

## 위험성
*   **NoSQL Injection**: 공격자가 비교 연산자(`$gt`, `$ne` 등)를 JSON 형태로 밀어 넣어 인증을 바이패스하거나 허용되지 않은 모든 세트 데이터를 유출시킬 수 있습니다.

## 조치 방안
*   유입 객체를 통째로 넣지 마시고 필요한 키(`id` 등)의 밸류 타입만 명시적으로 꺼내서 적용 규칙을 정립하십시오.
