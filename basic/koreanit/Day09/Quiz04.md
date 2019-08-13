# Quiz04

```


public class Quiz04 {
	public static void main(String[] args) {
		// 500 이하까지 피보나치 수열을 출력하라 (1부터 시작한 앞 두 수의 합이 다음 수)
		// 1 1 2 3 5 8 13 21 34 .. 
		
		int num = 0;
		int num1 = 0;
		int num2 = 1;
		
		System.out.println(num2);
		while (num < 500) {
			num = num1 + num2;
			num1 = num2;
			num2 = num;
			if (num > 500) {
				break;
			}
			System.out.println(num);
		}
	}
}

```

