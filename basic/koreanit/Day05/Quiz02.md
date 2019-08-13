# Quiz02

```java
import java.util.Scanner;

public class Quiz02 {
	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		
		System.out.print("정수 한개를 입력하세요>> ");
		int num = sc.nextInt();
		
		String message = num + "(은)는 ";
		message += (num % 2 == 0) ? "짝수" : "홀수";
		message += " 입니다.";
		
		System.out.println(message);
				
		sc.close(); // 노란 줄 없애줌 // 심부름 꾼 퇴장
	}
}

```

