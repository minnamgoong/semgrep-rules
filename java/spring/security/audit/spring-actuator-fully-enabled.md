# spring-actuator-fully-enabled (액츄에이터 전면 개방 경보)

## 개요
Spring Boot Actuator 환경에서 모든 엔드포인트(`include: "*"`)가 외부 및 내부 호출에 제한 없이 무조건 노출되는 구성을 경보합니다.

## 위험성
*   **정보 노출**: `/env`, `/mappings`, `/heapdump` 등 시스템의 핵심 환경설정 및 메모리 스토리가 외부로 노출되어 2차 공격의 유력한 단서를 제공합니다.

## 조치 방안
*   `management.endpoints.web.exposure.include` 속성에 꼭 필요한 엔드포인트(`health`, `info`)만 최소한으로 선별 명시 하십시오.
