# documentbuilderfactory-disallow-doctype-decl-false (DOCTYPE 허용 위반 경고)

## 개요
DocumentBuilderFactory에서 disallow-doctype-decl 속성이 false로 설정되어 있습니다. XML 파싱 공격(XXE 등) 예방을 위해 반드시 true로 조치하세요.

## 위험성
*   파서가 DTD를 합법적으로 렌더링하려 하기에 XXE 보안 구멍이 실질적으로 다시 열리게 됩니다.

## 조치 방안
*   동일 속성 주입 값을 `true`로 뒤집어 선언하십시오.
