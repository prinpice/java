# Test

```java
class Person{
	String name;
	int age;
	
//	void setData(String n, int a) {
//		name = n;
//		age = a;
//	}
	
	void setData(String name, int age) {
		this.name = name;
		this.age = age;
	}
	// this. : 이 객체의 멤버(변수, 메소드)
	
	// 기본생성자 : 우리가 따로 생성자를 만들지 않으면 자동으로 만들어지는 생성자
	// (=Default 생성자)
	
	// 기본생성자 형식 : 
    //		Person(){
	//		
	//		}
	
	Person(){
		System.out.println("Person 객체 생성 완료!");
	}
	Person(String n, int a){
		name = n;
		age = a;
		System.out.println("Person 객체 생성 + 값 저장 완료!");
	}
	/*
	 * <생성자 형식>
	 * (접근제어자) 클래스명(){
	 * 
	 * }
	 * 
	 * -이름은 클래스 이름과 동일해야 한다.
	 * -리턴자료형이 없다 (void 쓰면 안됨!!)
	 * 
	 * <생성자 주의사항>
	 * - 객체 생성 시에만 사용할 수 있다. (new할 때만 사용할 수 있음)
	 * - 생성자끼리는 서로를 호출할 수 있다. ===> this()
	 */
	Person(String n){
		this(n, 0); // 객체중에서 string과 int의 인자를 가지고 있는 생성자를 사용하겠다. => Person(n, a)사용
	}
}
public class Test01 {
	public static void main(String[] args) {
		Person p1 = new Person(); // Person생성자가 없으면 에러발생 
		Person p2 = new Person("홍길동", 7);
		System.out.println(p2.name);
		System.out.println(p2.age);
	}
}

```

