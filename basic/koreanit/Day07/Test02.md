# Test02

```
import java.util.Scanner;

public class Test02 {
	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		int age;
		System.out.print("나이를 입력하세요..:");
		age = sc.nextInt();
		
		if(age >= 20) {
			System.out.println("성인이군요!");
		}
		else { // 그렇지않으면 (위에 있는 짝꿍 if의 ()가 false면 무조건 실행됨)
			System.out.println("미성년이군요!");
		}
		
		if (age <= 7) {
			System.out.println("미취학 아동");
		}
		else if (age <=13) {
			System.out.println("초등학생");
		}
		else if (age <= 16) {
			System.out.println("중학생");
		}
		else if (age <= 19) {
			System.out.println("고등학생");
		}
		else {
			System.out.println("대학생 혹은 성인");
		}
		
		System.out.println("당신의 나이는 " + age + "세 입니다.");
	}
}

```

