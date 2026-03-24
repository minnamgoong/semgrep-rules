# create-de-cipher-no-iv (createCipher 사용 위험)

## 개요
Node.js 내장 `crypto` 모듈 중 레거시 드라이버 버전인 `createCipher` 호출을 포착합니다.

## 위험성
*   자동으로 키와 정적 IV를 주입 생성해 다수의 데이터 암호화 버퍼에 동일 논스가 가미되는 결정적 암호화 위험을 받습니다.

## 조치 방안
*   `crypto.createCipheriv(algorithm, key, iv)`를 고용해 고유 논스 버퍼를 대입하세요.
