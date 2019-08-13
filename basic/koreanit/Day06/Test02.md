# Test02

```java

public class Test02 {
	public static void main(String[] args) {
		double rand = Math.random(); // 0 ~ 0.9999 (1 미만)인 실수를 돌려줌
		System.out.println(rand);
		
		System.out.println(Math.random()); // 빨리 실행하면 렉먹음
		
		// 0 ~ 9 중 1개의 랜덤수 생성
		/* 
		 * int rand1 = (int)(10*Math.random());
		 * System.out.println(rand1);
		 */
		System.out.println((int)(rand*10));
		// 1 ~ 10 중 1개
		System.out.println((int)(rand*10)+1); // 1부터 10개의 숫자를 뽑아라
		// 1 ~ 6 중 1개
		System.out.println((int)(rand*6)+1); // 1부터 6개의 숫자를 뽑아라
		// 3 ~ 5 중 1개
		System.out.println((int)(rand*3)+3); // 3부터 3개의 숫자를 뽑아라
		
		// 공식 : (int)(Math.random() * 개수) + 시작수
		// 1.  2~9중 1개 출력
		System.out.println((int)((Math.random() * 8)+2));
		
		// 2.  1~45 중 1개 출력
		System.out.println((int)(Math.random() * 45) + 1);
	}
}

```

