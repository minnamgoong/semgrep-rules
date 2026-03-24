# spring-actuator-fully-enabled (액츄에이터 전면 개방 경보)

## 개요
Spring Boot Actuator의 모든 엔드포인트가 완전 개방되어 민감 정보가 노출될 수 있습니다. 필요한 엔티티만 인가하여 사용하세요.

## 위험성
*   **정보 노출**: `/env`, `/mappings`, `/heapdump` 등 시스템의 핵심 환경설정 및 메모리 스토리가 외부로 노출되어 2차 공격의 유력한 단서를 제공합니다.

## 조치 방안
*   `management.endpoints.web.exposure.include` 속성에 꼭 필요한 엔드포인트(`health`, `info`)만 최소한으로 선별 명시 하십시오.
