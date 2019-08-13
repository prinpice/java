# Quiz01

```java
import java.util.Scanner;
public class Quiz01 {
	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		// 문제 1. 나이를 입력받고, 3년 뒤 나이를 출력
		int age;
		
		System.out.print("나이: ");
		age = sc.nextInt();
		// int age = sc.nextInt(); 도 가능
		
		System.out.println("3년 뒤 나이 : " + (age + 3) + "세");
		
		// 문제 2. 밑변, 높이를 입력 받고, 삼각형의 넓이를 출력
		double base;
		double height;
		
		System.out.print("밑변 : ");
		base = sc.nextDouble();
		System.out.print("높이: ");
		height = sc.nextDouble();
		// double area = base * height /2;
		
		System.out.println("삼각형의 넓이: " + (base * height / 2));
		
		// 문제 3. 정수를 1개 입력 받고, 해당 구구단을 출력
		//    예) 3 => 3 * 1 = 3
		//            3 * 2 = 6
		//            ...
		//            3 * 9 = 27
		int num;
		
		System.out.print("정수를 입력하세요>> ");
		num = sc.nextInt();
		
		System.out.println(num + "단");
		System.out.println(num + " * 1 = " +(num*1));
		System.out.println(num + " * 2 = " +(num*2));
		System.out.println(num + " * 3 = " +(num*3));
		System.out.println(num + " * 4 = " +(num*4));
		System.out.println(num + " * 5 = " +(num*5));
		System.out.println(num + " * 6 = " +(num*6));
		System.out.println(num + " * 7 = " +(num*7));
		System.out.println(num + " * 8 = " +(num*8));
		System.out.println(num + " * 9 = " +(num*9));
	}
}

```

