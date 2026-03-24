# insecure-innerhtml (innerHtml XSS 위험)

## 개요
$EL.innerHTML에 사용자 제어 데이터가 대입되고 있습니다. XSS 취약점을 유발하는 안티 패턴이므로 textContent 대체 사용 등을 고려하세요.

## 위험성
*   **Stored/Reflected XSS**: 공격자가 `<script>` 또는 `<iframe>` 태그를 주입해 브라우저 렌더링 시 악성 자바스크립트를 실행시켜 세션 탈취 및 피싱을 유도합니다.

## 조치 방안
*   단순 텍스트 주입 시에는 `.textContent` 또는 `.innerText`를 고용하여 자동 이스케이프 되도록 유도하세요.
