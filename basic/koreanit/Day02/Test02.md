# Test02

```java
/*
 * <변수(variable)>
 * - 데이터 1개를 저장하는 그릇 역할의 메모리
 * - 변수 사용 순서
 *     1. 변수 선언(=변수 만들기)
 *     2. 변수 초기화(=변수에 최초로 값을 저장)
 *     3. 변수 호출(=변수 확인)
 *   ( 4. 변수 접근(=변수 값 변경)  )
 *   
 *   1. 변수 선언
 *       형식 : 자료형 변수명
 *   2. 변수 초기화
 *       (최초로) 변수명 = 값
 *   3. 변수 호출
 *       예) sysout(변수명)
 *          변수명 + 100
 *   4. 변수 접근
 *       변수명 = 값
 *       
 */
public class Test02 {
	public static void main(String[] args) {
		String name = "김피카츄";  // string name; ==> name 선언 // name = "김피카츄"; => name 초기화
		int age = 10; // age 선언 및 초기화
		// int age;
		// age = 10;
		
		System.out.println("저의 이름은 " + name + "입니다.");
		System.out.println("저는 " + age + "살 입니다.");
		
		age = 13;
		System.out.println("3년 뒤엔 " + age + "살이 됩니다.");
	}
}

```

