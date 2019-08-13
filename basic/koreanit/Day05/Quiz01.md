# Quiz01

```java
import java.util.Scanner;

public class Quiz01 {
	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		
		int age;
		
		System.out.print("나이를 입력하세요>> ");
		age = sc.nextInt();
		
		System.out.println("당신의 나이는 " + age + "세 입니다.");
		
		String message = "당신은 ";
		message += (age >= 14) ? "성인" : "미성년자"; // 조건연산자가 if문보다 빠름
		message += " 입니다.";
		
		System.out.println(message);
	}
}

```

