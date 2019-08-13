# Quiz06

```

public class Quiz06 {
	public static void main(String[] args) {
		// 1. 1 ~ 20 중 랜덤한 정수를 5번 출력 (중복 가능)
		
		for(int n = 1; n <= 5; n++) {
			System.out.println((int)(Math.random()*20)+1);
		}
		System.out.println();
		
		// 2. 1 ~ 1000 중 11과 17의 공배수만 출력
		// 2-2. 11과 17의 공배수의 개수 출력
		
		int count = 0;
		
		for (int n = 1; n <= 1000; n++) {
			if (n %11 == 0 && n % 17 == 0) {
				System.out.println(n);
				count++;
			}
		}
		/*
		 * for (int n = 11 * 17; n <= 1000; n++){
		 *     System.out.println(n);
		 *     ++count;
		 * }
		 */
		System.out.println("공배수의 개수: "+count);
		System.out.println();
		
		// 3. 2단 ~ 9단까지 모든 구구단을 출력
		
		for (int n = 2; n <=9; n++) {
			for (int m = 1; m <=9; m++) {
				System.out.println(n +"*"+m+"="+n*m);
			}
			System.out.println();
		}
	}
}

```

