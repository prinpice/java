# Test04

```java
package package1; // 이 소스파일(Test03.java)의 소속 패키지 선언
/*
 * < 패키지(package)>
 * - 클래스들이 소속된 디렉토리(폴더)의 개념 ===> 클래스들이 사는 동네
 * - 클래스 은닉화를 구현
 * - 클래스 이름 중복을 피할 수 있음
 * - 클래스는 반드시 패키지안에 있어야 함
 * - 모두 소문자로 짓는다
 */
import package2.Person; // 마지막 단어가 클래스여야 함
// import package2; // (x)
import package2.*; // pakage2의 모든 클래스를 import하겠다! // * : all
public class Test04 {
	public static void main(String[] args) {
		Person p = new Person(); // 에러!
		// 다른 패키지의 클래스는 일반적으로 선언 불가
		
		// 방법1. 클래스의 전체이름(풀네임)을 쓴느 방법
		package2.Person p1 = new package2.Person();
		java.util.Scanner sc = new java.util.Scanner(System.in);
		
		// 방법2. 소스파일 상단에 import 선언
		Person p2 = new Person(); // package2. Person으로 인식함
		
		// 새로운 문제점....
		// p1.name = "김피카츄";
		// p2.name = "장라이츄";
		// ==> name이 보이지 않는다?? ==> 객체의 은닉화 (접근제어자)
		// Person2 클래스로 이동!
		
	}
}

```

