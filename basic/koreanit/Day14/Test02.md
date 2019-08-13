# Test02

```java
class Person{
	String name;
	int age;
}
public class Test02 {
	public static void main(String[] args) {
		Person[] pArr = new Person[3];
		
		pArr[0] = new Person();
		pArr[0].name = "홍길동";
		pArr[0].age = 10;
		
		pArr[1] = new Person();
		pArr[1].name = "이푸린";
		pArr[1].age = 12;
		
		pArr[2] = new Person();
		pArr[2].name = "김피카츄";
		pArr[2].age = 30;
		
		// 확장 for문을 사용하여 3개 인스턴스의 정보를 출력
		
		for (Person tmp1 : pArr) { // 모든 객체가 Person형으로 저장되기 때문   // 확장 for문으로 선언되는 변수의 자료형과 배열의 자료형이 동일해야 한다.
			System.out.println("확장 for문: "+tmp1.name);
			System.out.println("확장 for문: "+tmp1.age+ "세");
		}
		
		// 객체배열 + 확장 for문 주의 사항
		for(Person tmp2 : pArr) {
			tmp2.name = "없음";
		}
		System.out.println("===변경 후 name===");
		System.out.println(pArr[0].name);
		System.out.println(pArr[1].name);
		System.out.println(pArr[2].name);
	}
}

```

