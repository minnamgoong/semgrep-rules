# calling-set-state-on-current-state (무의미한 setState 호출 경고)

## 개요
React `useState` 가동 시 `setCount(count)` 같은 형태로 원래 상태를 무위 연산 갱신하려는 로직을 적발합니다.

## 위험성
*   **논리 버그**: 가독성 낙후 및 실제 의도한 갱신 동작이 누락되어 렌더링 주기가 낭비되거나 버그가 날 공산이 큽니다.

## 조치 방안
*   연산 타겟 변수 및 로직 세부 흐름을 바정하십시오.
