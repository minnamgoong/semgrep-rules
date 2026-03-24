# detect-angular-open-redirect (Angular 오픈 리디렉션 경보)

## 개요
Angular 컨트롤러단에서 사용자 파라미터를 `$window.location.href` 및 `$location.url()` 에 직접 적용하는 형태를 적발합니다.

## 위험성
*   **Open Redirect**: 해커가 자사 피싱 유도 페이지 주소를 유도하여 클라이언트 브라우저 도약을 임의 조장시키는 보안 부적격 스탠스입니다.

## 조치 방안
*   리다이렉션 직전 주소가 내부 도메인 규격인지 검증 함수를 필수 적용 하십시오.
