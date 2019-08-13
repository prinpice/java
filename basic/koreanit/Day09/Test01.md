# Test01

```

public class Test01 {
	public static void main(String[] args) {
		// 1 ~ 10까지 do-while로 출력
		int n = 1;
		do {
			System.out.println(n);
			++n;
		}while(n<=10);
		
		// while과 do while의 차이? => 실행 순서의 차이!
		// while : () => {} => ()
		// do-while : {} => () => {}
		// do-while은 조건식 결과와 상관없이 최소 1회 종속문장 실행
		while (n == 20 ) { // 애초에 false
			System.out.println("while문 실행될까?");
		}
		do {
			System.out.println("while문 실행될까?");
		} while (n == 20); // 애초에 false
	}
}

```

