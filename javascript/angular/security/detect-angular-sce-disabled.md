# detect-angular-sce-disabled (AngularSCE 비활성화 경고)

## 개요
$sceProvider가 false로 설정되어 엄격한 컨텍스트 이스케이프가 비활성화되었습니다. XSS 공격 방어를 위해 SCE를 활성화해야 합니다.

## 위험성
*   **XSS**: HTML, 스타일, 리소스 바인딩 시 자동 클렌징이 작동하지 않아 악성 로드 탑재 스크립트 구동 피해가 빈발할 수 있습니다.

## 조치 방안
*   `$sceProvider.enabled(false);` 호출 라인을 삭제하거나 값을 `true`로 보강 하세요.
