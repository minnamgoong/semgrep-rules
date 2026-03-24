# documentbuilderfactory-disallow-doctype-decl-false (DOCTYPE 허용 위반 경고)

## 개요
`DocumentBuilderFactory` 설정 시 보안 기능인 `disallow-doctype-decl` 속성이 명시적으로 `false`로 비활성 구동 설정된 상태를 적출합니다.

## 위험성
*   파서가 DTD를 합법적으로 렌더링하려 하기에 XXE 보안 구멍이 실질적으로 다시 열리게 됩니다.

## 조치 방안
*   동일 속성 주입 값을 `true`로 뒤집어 선언하십시오.
