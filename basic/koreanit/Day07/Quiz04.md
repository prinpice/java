# Quiz04

```

public class Quiz04 {
	public static void main(String[] args) {
		// Math.random()을 사용하여 1 ~ 45의 수 중 하나의 정수를 랜덤하게 뽑고
		// 뽑힌 정수를 출력하고 짝수 혹은 홀수를 판별하세요.
		
		System.out.println("정수 하나를 랜덤으로 뽑습니다.");
		int num = (int)(Math.random() * 45) + 1;
		System.out.println(num);
		
		if (num % 2 == 0) {
			System.out.println("짝수입니다.");
		}
		else if (num % 2 == 1) {
			System.out.println("홀수입니다.");
		}
		
		
		// 3의 배수, 4의 배수, 5의 배수, 7의 배수인지 출력
		// 12 => 3의 배수, 4의 배수
		// 30 => 3의 배수, 5의 배수
		// 14 => 7의 배수
		// 13 => 3, 4, 5, 7의 배수 모두 아님
				
		if (num % 3 == 0) {
			System.out.println("3의배수 입니다.");
		}
		if (num % 4 == 0) {
			System.out.println("4의배수 입니다.");
		}
		if (num % 5 == 0) {
			System.out.println("5의배수 입니다.");
		}
		if (num % 7 == 0) {
			System.out.println("7의배수 입니다.");
		}
		if (num % 3 != 0 && num % 4 != 0 && num % 5 != 0 && num % 7 != 0) {
			System.out.println("3, 4, 5, 7의 배수가 모두 아닙니다.");
		}
	}
}

```

