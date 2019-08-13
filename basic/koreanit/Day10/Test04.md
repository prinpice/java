# Test04

```
// 절차적 방법(c언어): 순서대로 만듬 ,   단점: 유지보수가 어려움, 동시에 여러명 작업 불가
// 객체지향: 부품을 따로 다 만들어 조립 , 유지보수가 쉬움(각각 업그레이드 가능), 팀프로젝트 가능 (협업),  단점: 섬세한 코딩 불가능, 메모리가 비효율적으로 사용

/*
 * 1. 클래스
 *  - 객체 설계도 역할
 *  - 메인메소드가 없다.
 *  
 * 2. 메인클래스
 *  - 메인메소드가 있는 클래스 (프로그램이 될 클래스)
 *  - 자바는 class-based 언어 (모든 코드는 클래스 안에 있어야 함)
 *    메인메소드도 특정 클래스 안에 있어야 함 => 메인클래스
 *    
 * 3. 인스턴스(=객체)
 *  - 프로그램의 부품 역할
 *  - 데이터 저장용도, 메소드 실행(행위)
 *  
 * 4. 레퍼런스(=참조)
 *  - 인스턴스의 메모리 주소
 *  
 * 5. 레퍼런스 타입(=참조 자료형)
 *  - 인스턴스의 자료형 (~~모양 객체)
 *  - '이 주소를 찾아가면 ~~모양 객체가 나온다'라는 의미
 *  
 * 6. 레퍼런스 변수(=참조변수)
 *  - 주소를 저장하는 메모장 역할의 변수
 *  - 주소의 길이는 32bit길이라서, 참조변수도 크기가 32bit(4byte)
 */
public class Test04 {
	public static void main(String[] args) {
		Person p1; //참조변수 선언
		// Person : 참조 자료형 (= 이 주소를 찾아가면 ~~ 모양 객체가 있다!)
		// p1 : 참조 변수의 이름
		// => p1 변수에 저장될 주소를 찾아가면 Person모양객첵 있다!라고 미리 얘기하는 것  // 여기까지는 아직 아무것도 저장이 안되어 있어 쓰레기값이 있음
		p1 = new Person();
		// new :새 객체를 생성하고 (동적할당하고) + 그 객체의 주소를 알려줘!
		// Person() : Person 모양으로 
		Person p2 = new Person();
		Person p3 = null; // 없다 ==> 객체는 없고 빈 메모장이다.
		
		// 참고) 객체가 생성되면 객체의 멤버 변수는 자동으로 
		// 문자열 => null
		// 정수/ 실수 => 0
		// boolean => false
		// 로 초기화 됨
		
		
		p1.name = "홍길동"; // '.' : ~의
		// 1004.name = "홍길동";
		p1.age = 10;
		p1.tel = "010-1111-1111";
		
		p2.name = "이푸린";
		p2.age = 7;
		p2.tel = "없음";
		
		System.out.println("p1의 이름: " + p1.name);
		System.out.println("p1의 나이: " + p1.age);
		System.out.println("p1의 연락처 : " + p1.tel);
		
		p2.showInfo();
		
		p2 = p1;
		System.out.println("p2의 이름: " + p2.name);
		System.out.println("p2의 나이: " + p2.age);
		System.out.println("p2의 연락처 : " + p2.tel);
		
		// 주의!
		// p3.name = "김뚜벅초"; // Exception in thread "main" java.lang.NullPointerException
		// null.name = "김뚜벅초";와 같음 
	}
}

```

