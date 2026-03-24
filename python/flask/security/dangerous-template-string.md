# dangerous-template-string (동적 템플릿 문자열 인젝션)
## 개요
Jinja 등 템플릿 구문 생성 전 사용자 유입 데이터가 소스단 문자열에 합산되는 형태를 점검힙니다.
## 조치 방안
*   템플릿에 데이터 바인딩 시 Parameterized 형태를 유지하십시오.
