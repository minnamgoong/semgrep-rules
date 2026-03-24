# create-de-cipher-no-iv (createCipher 사용 위험)

## 개요
지원 중단된 createCipher 기용이 잡혔습니다. 암호화 해독 위험이 크므로 createCipheriv 로 고유 IV를 주입하여 보강하세요.

## 위험성
*   자동으로 키와 정적 IV를 주입 생성해 다수의 데이터 암호화 버퍼에 동일 논스가 가미되는 결정적 암호화 위험을 받습니다.

## 조치 방안
*   `crypto.createCipheriv(algorithm, key, iv)`를 고용해 고유 논스 버퍼를 대입하세요.
