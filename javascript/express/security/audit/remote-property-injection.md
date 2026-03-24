# remote-property-injection (원격 프로퍼티 인젝션 감지)

## 개요
`object[userInput]` 와 같이 배열 대괄호 표기법을 통해 객체의 동적 키에 접근하는 연산에 외부 오염 데이터가 소모되는 것을 경보합니다.

## 위험성
*   **Prototype Pollution (프로토타입 오염)**: 공격자가 `__proto__` 또는 `constructor` 키를 주입해 하위 기반 객체를 오염시키고 전체 애플리케이션의 동작을 마비시키거나 변수 삽입을 유도할 수 있습니다.

## 조치 방안
*   키 접근 전 유저 입력이 `__proto__`, `constructor`, `prototype` 같은 특키인지 검사하는 Validation을 장착해야 합니다.
