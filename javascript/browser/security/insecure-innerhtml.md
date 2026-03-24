# insecure-innerhtml (innerHtml XSS 위험)

## 개요
DOM 객체의 `.innerHTML` 속성에 외부 사용자 입력 가변 문자열을 직접 대입하는 형태를 경보합니다.

## 위험성
*   **Stored/Reflected XSS**: 공격자가 `<script>` 또는 `<iframe>` 태그를 주입해 브라우저 렌더링 시 악성 자바스크립트를 실행시켜 세션 탈취 및 피싱을 유도합니다.

## 조치 방안
*   단순 텍스트 주입 시에는 `.textContent` 또는 `.innerText`를 고용하여 자동 이스케이프 되도록 유도하세요.
