# find-sql-string-concatenation (SQL 문자열 결합 감지)

## 개요
이 규칙은 SQL 쿼리를 구성할 때 문자열 결합(예: `+` 연산자)을 사용하는 보안 비권장 패턴을 감지합니다.

## 위험성
*   **SQL Injection (SQL 인젝션)**: 공격자가 입력값에 악의적인 SQL 문법을 주입하여 데이터베이스를 조작하거나 비공개 데이터를 탈취할 수 있습니다.

## 조치 방안
*   문자열 결합 방식 대신 **Parameterized Query** (`PreparedStatement` 등)를 사용하여 데이터와 쿼리 구조를 분리하세요.

```java
// ❌ 취약한 코드 (문자열 결합)
String query = "SELECT * FROM users WHERE name = '" + name + "'";
Statement stmt = conn.createStatement();
ResultSet rs = stmt.executeQuery(query);

// ✅ 안전한 코드 (Parameterized Query)
String query = "SELECT * FROM users WHERE name = ?";
PreparedStatement pstmt = conn.prepareStatement(query);
pstmt.setString(1, name);
ResultSet rs = pstmt.executeQuery();
```
