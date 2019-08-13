# Test02

```java
/*
 * < 오버로드 주의사항>
 * 1. 매개변수 이름이 다르다고 해서 무조건 오버로드 되는 것은 아님
 * 2. 리턴자료형이 다르다고 해서 무조건 오버로드 되는 것은 아님
 *   => 매개변수 '자료형'만 본다.
 */
class Person{
	String name;
	int age;
	String tel;
	
	void setData() {
		name = "없음";
		age = 1;
		tel = "없음";
	}
	void setData(String n) {
		name = n;
		age = 1;
		tel = "없음";
	}
	void setData(String n, int a) {
		name = n;
		age = a;
		tel = "없음";
	}
	void setData(String n, int a, String t) {
		name = n;
		age = a;
		tel = t;
	}
	void printData() {
		System.out.println("이름 : " + name);
		System.out.println("나이 : " + age);
		System.out.println("연락처 : " + tel);
	}
	
//	void setData(String t){ // 매개변수 이름이 달라도 input자료형이 같기때문에 중첩이 됨(오버로드 X)
//		tel = t;
//	}
	
//	int setData() { // 리턴 자료형이 달라도 무조건 오버로드되지 않음
//		
//		return age;
//		
//		// 또는 
//		
//		name = "없음";
//		age = 1;
//		tel = "없음";
//		return 0;
//	}
}


public class Test02 {
	public static void main(String[] args) {
		Person p1 = new Person();
		Person p2 = new Person();
		Person p3 = new Person();
		Person p4 = new Person();
		
		p1.setData();
		p2.setData("김피카츄");
		p3.setData("최뚜벅초", 10);
		p4.setData("이푸린", 25, "010-1111-1111");
		
		p1.printData();
		System.out.println();
		p2.printData();
		System.out.println();
		p3.printData();
		System.out.println();
		p4.printData();
		System.out.println();
		
	}
}

```

