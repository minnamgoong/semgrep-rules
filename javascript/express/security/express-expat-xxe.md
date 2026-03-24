# express-expat-xxe (Expat 파서 XXE 위험 점검)

## 개요
expat XML 파서 구동 시 외부 입력에 검증이 부실합니다. XML External Entity (XXE) 취약점 격출을 무마하기 위해 보안 옵션을 비활성화 처리하십시오.

## 위험성
*   **XXE 유출**: 서버 로컬 패스워드나 설정 파일 등의 정보를 해커 피싱 서버로 역발신시키는 XML 구현 사보타주가 우려됩니다.

## 조치 방안
*   파서 `setFeature` 유닛을 동원해 DTD 전개를 명시적으로 막으세요.
