# jwt-none-alg (jsonwebtoken 'none' 알고리즘 위험)

## 개요
Node.js 진영 대표 라이브러리인 `jsonwebtoken` 검증 통로에 `none` 알고리즘 서명 방식을 사용하는 국면을 감지합니다.

## 위험성
*   **인증 무력화**: 사용자가 로컬에서 헤더 토큰을 조작해 관리자 흉내를 내도 보안 필터가 패싱될 위험이 존재합니다.

## 조치 방안
*   `jwt.verify(token, secret, { algorithms: ['HS256'] })` 등 허용 가능한 알고리즘 목록을 고정 명시하는 것을 적극 권합니다.
