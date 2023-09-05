# DBConnection
DB를 연결하여 쇼핑몰 회원가입 하기
# DB 연결문
``` java
  package db;

import java.sql.Connection;
import java.sql.DriverManager;

public class DBConnect {
	
	public static Connection getConnection() {
		
		Connection conn = null;
		
		String url = "jdbc:oracle:thin:@localhost:1521:xe";
		String id = "system";
		String pw = "1234";
		try {
			Class.forName("oracle.jdbc.OracleDriver");
			conn = DriverManager.getConnection(url, id, pw);
			System.out.println("dd");	
		} catch (Exception e){
			e.printStackTrace();
		}
		return conn;
	}
}
```
