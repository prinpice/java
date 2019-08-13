# Test01

```java

public class Test01 {
	public static void main(String[] args) {
		/*
		 * ++, --가 변수 앞에 : 전위연산(=전치연산)
		 * ++, --가 변수 뒤에 : 후위연산(=후치연산)
		 * 
		 * ** 한 명령어(....;)에 여러 명령이 복합적으로 존재할 때
		 * 1. 전치연산 : 가장 먼저 증/감하고 나머지 연산을 수행
		 * 2. 후치연산 : 나머지 연산을 먼저 수행하고 마지막에 증/감
		 * 
		 * ** 컴퓨터는 연산을 1개씩만 수행할 수 있음
		 *    연산 수행 후 그 결과를 식이 있던 그 자리에 반환함
		 *    a = 1 + 2 * (4 - 5) / 3;
		 *    a = 1 + 2 * (-1) / 3;
		 *    a = 1 -2 / 3;
		 *    a = 1 + 0;
		 *    a = 1;
		 *    a;
		 *    => 연산자 우선순위가 존재함
		 */
		int a = 10;
		int b;
		//b = ++a; // a:11 / b:11 // 증가 후 저장
		b = a++; // a:11 / b:10 // 저장 후 증가
		System.out.println("a: " + a);
		System.out.println("b: " + b);
		
		int n = 1;
		System.out.println(++n); // 증가 후 출력 // 2   
		System.out.println(n++); // 출력 후 증가 // 2    1. SYSOUT 2. ++
		System.out.println(n++); // 출력 후 증가 // 3
		System.out.println(++n); // 증가 후 출력 // 5
		System.out.println(n);
		
	}
}

```

