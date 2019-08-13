# Test01

```java
import javax.swing.JOptionPane;

/*
 * < static >  // 안드로이드, JSP하려면 알아야함(특징은 암기!)
 * - 정적인, 고정된
 * - 멤버변수/멤버메소드에 붙일 수 있는 키워드
 * -특징
 *  1. 객체명 대신 클래스명으로 접근한다.
 *  2. 프로그램 실행 직전에 무조건 생성된다. (or 미리 생성된다.)
 *      => new (객체 생성) 안해도 사용할 수 있다.
 *  3. 1개만 생성된다. (공유폴더의 개념)    ex) 정수기
 *     => 상태를 공유한다.
 */
class A{
	static void aa() {
		System.out.println("나는 static 메소드 aa()~");
	}
}
public class Test01 {
	public static void main(String[] args) {
		// 우리가 만든 메소드는 여태 객체생성(new)해야지 사용할 수 있었다.
		// 여태 객체생성 없이도 사용할 수 있는 메소드, 변수가 있었다.
		
		System.out.println(); // new System() (X) // System이 클래스
		Math.random(); // new Math()  (X)         // Math가 클래스
		JOptionPane.showMessageDialog(null, "ㅋㅋㅋ");
		System.out.println(Math.PI);
		Integer.parseInt("10");
		
		// 우리가 만든 static 메소드를 사용해보자
		A aInstance = new A();
		aInstance.aa(); // The static method aa() from the type A should be accessed in a static way
		A.aa();  // a static way
	}
}

```

