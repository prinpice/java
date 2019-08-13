# Test02

```java
import java.util.Scanner;

public class Test02 {
	public static void main(String[] args) {
		// 두 문자열이 같냐/다르냐 비교할 때는
		// '=='쓰면 안됨!
		Scanner sc = new Scanner(System.in);
		
		String s;
		
		System.out.print("피카츄를 입력하세요! : ");
		s = sc.next();
		
		System.out.println("입력된 단어: " + s);
		System.out.println("s == 피카츄: " + (s == "피카츄")); // s == 피카츄: false
		System.out.println("s.equals(피카츄): " + (s.equals("피카츄"))); // s.equals(피카츄): true // 문자열.equals(문자열) // "피카츄".equals(s)도 가능
		// 사용방법: 문자열1.equals(문자열2)
		// 결과: true 혹은 false (boolean형 데이터)
	}
}

```

