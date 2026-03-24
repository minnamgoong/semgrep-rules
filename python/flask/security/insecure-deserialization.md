# insecure-deserialization (취약한 역직렬화)
## 개요
Pickle 등 악성 탑재를 허용하는 역직렬화 가동을 경보합니다.
## 조치 방안
*   가변 오브젝트 가공 전담이 아닌 JSON 전용 파서를 사용하십시오.
