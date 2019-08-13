# Test03

```java
package package1;
/*
 * <final>
 * - 최후의, 변경되지 않는
 * - 변수 앞에 : 값 변경 불가
 *   클래스 앞에서 : 상속 불가
 *   메소드 앞에 : 오버라이드 불가(오버로드는 가능..)
 *   
 *   < 사용자 정의 상수 : static final >  // static이 들어가는 이유는 하나만 만들어도 되기 떄문
 *   - 개발자가 정의하는 값 변경 안되는 데이터
 *   - 원주율, 황금비, 프로그램 내부의 규칙(지뢰찾기 칸은 세로 5칸, 가로 5칸) 등
 *   - 주로 인터페이스에 선언한다.
 *   - 이름 작명 시, All대문자 + 띄어쓰기 대신 '_'
 *     예) MAX_LEVEL 
 */
public class Test03 {
	
	static final double PI = 3.1415;
	
	public static void main(String[] args) {
		final int a = 10;
		// a = 20; // 변경 불가
		
		System.out.println(PI*4*4);
		System.out.println(Test03.PI); // <== 우리가 만든 원주율
		System.out.println(Math.PI); // <== 자바에서 약속한 원주율
	}
}

```

