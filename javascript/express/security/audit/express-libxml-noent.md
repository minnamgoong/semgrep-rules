# express-libxml-noent (Libxml noent 활성화 위험)

## 개요
`libxmljs` 등의 모듈에서 `noent: true` 옵션을 인위적으로 켜 엔티티 확산 권한을 부여한 국면을 진단합니다.

## 위험성
*   **XXE**: 파서가 DTD 내부 엔티티를 자동 전개하게 만들어 공격자의 내부 자산 탈취 피싱에 영구 개방되는 보안 구멍이 열립니다.

## 조치 방안
*   `noent` 옵션을 아예 명시하지 않거나 `false`로 격리하십시오.
