# Test01

```

public class Test01 {
	public static void main(String[] args) {
		int n;
		for(n = 0; n <= 10; ++n) {
			int a = 10;
			System.out.println(a);
			++a;
		}
		// 반복문(for, while, do-while)의 {} 안에 선언된 변수의 수명
		// => 태어났다 죽는 것 자체를 반복
		
		// for문의 초기식에 선언된 변수의 수명
		for(int a= 0; a<= 10; ++a) {
			System.out.println(a);
		}
	}
}

```

