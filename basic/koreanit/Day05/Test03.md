# Test03

```java
import java.util.Scanner;

public class Test03 {
	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		int age;
		boolean result;
		
		System.out.print("나이: ");
		age = sc.nextInt();
		
		//result = (14 <= age <= 16); X
		result = (14 <= age && age <= 16);
		
		System.out.println("중학생? ==> " + result);
		
		char ch = 'G';
		// ch가 대문자인지 확인해보기
		//result = (65 <= ch && ch <= 90); // A: 65/ Z: 90
		result = ('A' <=ch && ch <= 'Z');
		System.out.println(ch + "(은)는 대문자? ==> " + result);
	}
}

```

