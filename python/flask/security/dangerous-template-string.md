# dangerous-template-string (동적 템플릿 문자열 인젝션)
## 개요
가변 스트링 합사를 통한 동적 템플릿 생산이 잡혔습니다. SSTI 예방을 위해 객체 렌더링 양식을 쓰세요.
## 조치 방안
*   템플릿에 데이터 바인딩 시 Parameterized 형태를 유지하십시오.
