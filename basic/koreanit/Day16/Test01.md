# Test01

```java
/*
 * < 메소드 오버로드(overload) >
 * - 메소드 호출(실행)시 그 메소드의 매개변수에 맞게
 *   인자값을 넣어야 한다.
 * - 메소드 오버로드란?
 *   : 똑같은 이름의 메소드를 여러 버전으로 만들어 두는 것
 *    => 이 메소드를 사용할 다른 개발자들의 편의를 위해서
 *   : 매개변수의 자료형 혹은 개수에 차이를 두어 여러 개를 만든다.
 */
class Test { // 하나의 소스파일(.java)에는 여러 클래스를 만들 수 있음
	         //  대신, public class는 1개만 만들 수 있다.
	         // 클래스 간의 연관관계는 없다.
	void aa() {
		System.out.println("매개변수 없는 aa()");
	}

	/*
	 * 아래와 같이 사용할 수는 있지만 사용안함
	 * int aa() {
	       System.out.println("매개변수 없는 aa()");
		   return 1;
	   }
	   boolean aa(){
	       System.out.println("매개변수 없는 aa()");
	       return true;
	   }
	 */
	
	void aa(int a) {
		System.out.println("정수 1개가 들어온 aa(), 인자값: " + a);
	}
	void aa(String s) {
		System.out.println("문자열 1개가 들어온 aa(), 인자값: " + s);
	}
	void aa(int a, int b) {
		System.out.println("정수 2개가 들어온 aa(), 인자값: " + a + ", " +b);		
	}
}
public class Test01 {
	public static void main(String[] args) {
		Test t = new Test();
		
		// 오버로드된 메소드는, 메소드 호출할 때 뭘 실행할 지 결정함
		t.aa();
		t.aa(10);
		t.aa("ABC");
		t.aa(1, 10);
		// t.aa(3.14); // 사용하려면 메소드를 하나 더 만들어야함 => 실수형 aa
		
		System.out.println();
		System.out.println(10);
		System.out.println("ABC");
	}
}

```

