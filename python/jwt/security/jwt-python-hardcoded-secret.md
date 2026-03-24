# jwt-python-hardcoded-secret (하드코딩된 JWT 비밀키)
## 개요
코드 내부 소스 문자열에 비밀키가 직접 안착되어 위험 수위가 높습니다.
## 조치 방안
*   환경 변수(`os.getenv`)로 공급 경로를 이전하세요.
