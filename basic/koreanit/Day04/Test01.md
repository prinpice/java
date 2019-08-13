# Test01

```java
import java.util.Scanner;
public class Test01 {
	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		// 입력 받은 데이터를 가져다 줄 심부름꾼 sc 선언
		String name;
		int age;
		double height;
		String tel;
		
		System.out.print("이름: ");
		name = sc.next(); // 입력받은 데이터를 문자열 형태로 가져와라 + name에 저장하라
		System.out.print("나이: "); 
		age = sc.nextInt(); // 입력받은 데이터를 int형태로 가져와라 + age에 저장하라
		System.out.print("키: ");
		height = sc.nextDouble(); // 입력받은 데이터를 double형태로 가져와라 + height에 저장하라
		System.out.print("연락처: ");
		tel = sc.next(); // 입력받은 데이터를 문자열 형태로 가져와라 + tel에 저장하라
		
		System.out.println("====" + name + "님의 정보====");
		System.out.println("나이: " + age + "세");
		System.out.println("키:" + height + "cm");
		System.out.println("연락처: " + tel);
	}
}

```

