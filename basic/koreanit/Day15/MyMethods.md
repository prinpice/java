# MyMethods

```java
/*
 * <메소드 정의>
 * -기계 설계(메소드 만들기)
 * -형식 :
 *   리턴자료형 메소드명 (매개변수 선언){
 *   // 할 일
 *   return; 혹은 return 리턴값;
 *   }
 *   
 *   1. 리턴자료형
 *     - 리턴값(결과물)의 자료형을 미리 명시하는 부분
 *     - 리턴값이 없을 때는 void라고 쓴다. (**void : 빈공간 ==> 자료형이 없다)
 *     
 *   2. 메소드명
 *     - 맨 앞글자 소문자  (카멜표기법)   // 암묵적인룰(대문자로 해도 에러는 없음)
 *       예. myFirstMethod
 *       
 *   3. 매개변수 선언
 *     - 소괄호 안에 선언한다.
 *     - 여러 개 선언이면 ',' 를 사용한다.
 *       예. ~~~ (int a, String b)
 *     - 매개변수는 메소드 안에서만 사용가능한 변수이다.
 *       다른 메소드의 변수와 이름이 중복되어도 된다.
 *     - 재료(인자값)가 메소드 내부에 들어올 수 있는 통로 역할을 한다.
 *     - 매개변수가 없으면 재료가 들어올 수 없다.
 *     - ** 중요! 매개변수 개수만큼 재료(인자값)도 그에 맞게 넣어주어야 한다.
 *     
 *   4. {} : body
 *     - body 안에 선언된 변수는 '지역변수'라고 한다.
 *     - 메소드가 끝나면 매개변수와 함께 자동으로 사라진다.
 *     
 *   5. return
 *     - 메소드를 종료하라
 *       리턴값(최종결과물)을 반환하라 (어디로? 메소드가 실행(호출)된 코드 자리로)
 *       돌아가라 (어디로? 메소드가 호출되었던 자리로)
 *     - 리턴값은 return 옆에 쓴다
 *     - 리턴값이 없으면 return 단어는 생략할 수 있다.
 *     - 리턴할 수 있는 값은 1개 뿐이다
 *       => 실행 1번 당 돌려주는 값은 1개
 */
public class MyMethods {
	
	// 실수 1개(반지름)을 넣으면 원의 넓이가 나오는
	double circleArea(double radius) {
		double area = radius * radius * 3.14;
		return area;
	}
	
	// 랜덤하게 포켓몬의 이름이 나오는
	String randomPokemon() {
		String[] pokemon = {"피카츄", "라이츄", "파이리", "꼬부기", "버터풀"};
		// int random = (int)(Math.random()*5); // 0 ~ 4
		// String rPokemon = pokemon[random];
		// return rPokemon;
		return pokemon[(int)(Math.random()*5)];
	}
	
	// 정수를 1개 넣으면 짝/홀수인지 sysout해주는
	void printEvenOrOdd(int num) {
		System.out.print("인자값: " + num + ", ");
		if(num==0) {
			System.out.println("0 입니다.");
		}else if (num % 2 == 0) {
			System.out.println("짝수입니다.");
		}else {
			System.out.println("홀수입니다.");
		}
	}
}

```

