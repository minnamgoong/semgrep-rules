# gcm-nonce-reuse (AES-GCM Nonce 재사용 위험)

## 개요
`AES/GCM/NoPadding` 같은 블록 암호화 운용 시, 다수가 동일한 Initial Vector (IV / Nonce) 상수를 하드코딩해 재사용하는 점을 감지합니다.

## 위험성
*   **암호 해독**: GCM 모드에서 키(Key)와 논스(Nonce)가 동일하게 재사용되면 XOR 연산 취약점으로 인해 암호문이 공격자에 의해 쉽게 복원 및 완전 무력화 됩니다.

## 조치 방안
*   암호화 개시 시점에 랜덤 바이트 생성기(`SecureRandom`)를 통해 논스 공간을 매번 고유하게 분기시켜 적용하세요.
