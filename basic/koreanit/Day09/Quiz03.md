# Quiz03

```
import java.util.Scanner;

public class Quiz03 {
	// Math.random()을 사용하여 구구단 문제를 랜덤하게 내고(2~9단),
	// 답을 입력 받아 "정답!" 혹은 "땡.."을 출력
	// 정답이 5번 나올 때까지 반복
	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		int count = 0;

		// java는 공백이 상관없음 // 보기 편하게
		int num1;
		int num2;
		int answer;
		
		while(count<= 4) {
			num1 = (int)(Math.random() * 8) + 2;
			num2 = (int)(Math.random() * 9) + 1;
			System.out.println(num1);
			System.out.println(num2);
			System.out.print(num1 +"*"+ num2+"=");
			answer = sc.nextInt();
			if (answer == num1 * num2) {
				System.out.println("정답!");
				++count;
			}	
			else {
				System.out.println("땡..");
			}
			System.out.println("종료!");
		}

	}
}
// Quiz04.java
```

