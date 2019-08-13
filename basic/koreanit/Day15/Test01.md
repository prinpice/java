# Test01

```java
import javax.swing.JOptionPane;

/*
 * <메소드 장점>
 * 1. 재사용이 가능함
 * 2. 똑같은 코드를 또 쓸 필요가 없음
 * 3. 다른 프로그램을 만들때도 또 쓸 수 있음
 *   => 개발기간이 짧아지고, 유지보수가 용이, 팀 작업이 수월
 */
public class Test01 {
	public static void main(String[] args) {
		
		// 메소드를 사용하려면 객체생성부터!
		// 객체생성을 해야 메소드가 준비된다.
		MyMethods my = new MyMethods();
		
		// 메소드 호출 : 메소드 실행!
		// 형식 : 객체명.메소드명(넣고 싶은 인자값)
		String s = my.randomPokemon(); // 추가적으로 넣을 값이 없으면 소괄호 안에 빈 공간으로 남겨둠
		System.out.println(s); // 필요한 매개변수가 1개(매개변수가 1개 선언된 메소드)이므로 1개의 인자값을 소괄호 안에 넣어준다.
		
		System.out.println(my.randomPokemon());
		
		my.printEvenOrOdd(10);
		my.printEvenOrOdd(0);
		
		// 반지름이 7인 원의 넓이를 sysout
		System.out.println("반지름이 7인 원의 넓이 : " + my.circleArea(7));
		
		// 반지름이 13.3인 원의 넓이를 jop으로 출력
		// => circleArea() 사용           // = circleArea 메소드 사용
		JOptionPane.showMessageDialog(null, "반지름이 13.3인 원의 넓이 : " + my.circleArea(13.3));
		
	}
}

```

