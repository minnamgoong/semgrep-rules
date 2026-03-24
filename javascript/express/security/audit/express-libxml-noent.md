# express-libxml-noent (Libxml noent 활성화 위험)

## 개요
libxml 라이브러리 처리 시 noent(Entity expansion) 속성이 true 로 인가되었습니다. XXE 취약점에 전방 노출되므로 이를 비활성화 처리하세요.

## 위험성
*   **XXE**: 파서가 DTD 내부 엔티티를 자동 전개하게 만들어 공격자의 내부 자산 탈취 피싱에 영구 개방되는 보안 구멍이 열립니다.

## 조치 방안
*   `noent` 옵션을 아예 명시하지 않거나 `false`로 격리하십시오.
