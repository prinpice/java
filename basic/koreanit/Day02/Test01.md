# Test01

```java

public class Test01 {
	// sysout의 여러 종류
	// System.out.println() : 한 줄 출력 (=마지막에 자동 엔터)
	// System.out.print()   : 한 줄 출력 (=마지막에 자동 엔터x)
	// System.out.printf()  : 서식 출력 (%d, %f, %s, %c 등의 서식문자 사용) => 안쓸듯
	public static void main(String[] args) {
		System.out.println("ABC");
		System.out.println("DEF");
		System.out.println("GHI");
		System.out.println("\n"); // \n : 엔터(제어문자)
		
		System.out.print("ABC");
		System.out.print("DEF");
		System.out.print("GHI");
		System.out.print("\n");
		
		System.out.printf("\n");
		System.out.printf("%s", "ABC");
		System.out.printf("%s", "DEF");
	}
}

```

