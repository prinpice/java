# Test02

```java

public class Test02 {
	public static void main(String[] args) {
		/*
		 * < 복합 대입 연산자 >
		 * a += b ==> a = a + b
		 * a -= b ==> a = a - b
		 * a *= b ==> a = a * b
		 * a /= b ==> a = a / b
		 * a %= b ==> a = a % b
		 * 
		 * ** 주의!
		 *  += (O) ==> a += 10 ==> a = a + 10
		 *  =+ (X) ==> a =+ 10 ==> a = +10으로 인식됨
		 */
		
		int score = 0;
		
		// 쿠키 1개 먹음
		score += 10;
		
		// 또 먹음
		score += 10;
		
		System.out.println(("점수 : "+score));
		
		int a = 10;
		a += a; // a = a + a;
		a -= 3; // a = a - 3;
		a *= 2; // a = a * 2;
		a %= 7; // a = a % 7;
		a *= a; // a = a * a;
		System.out.println("a: " + a);
	}
}

```

