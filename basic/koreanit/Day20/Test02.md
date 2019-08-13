# Test02

```java
/*
 * < 상속(inheritance)>
 * = 확장 (extend)
 * : 기존 클래스를 확장하여 새 클래스를 만드는 작업
 *   - 유지보수 용이
 *   - 개발기간이 짧아짐
 *   - 무한한 확장성 (기능 추가를 계속할 수 있다.)
 *   
 * 예.
 *   원본 Person : 이름, 나이, 연락처
 *   새 클래스
 *      Student 클래스 : 이름, 나이, 연락처, 학년, 반, 점수
 *      Teacher 클래스 : 이름, 나이, 연락처, 담당과목
 *      Employee 클래스 : 이름, 나이, 연락처, 부서, 직급, 월급
 * 원본클래스(Person) : 부모클래스 = 슈퍼클래스 = 상위클래스
 * 확장클래스(Teacher) : 자식클래스 = 서브클래스 = 하위클래스
 */
class Person{
	String name;
	int age;
	String tel;
	
	void showInfo() {
		System.out.println("이름 : " + name);
		System.out.println("나이 : " + age);
		System.out.println("연락처 : " + tel);
	}
}
class Student2 extends Person{ // 같은 package에 같은 이름의 클래스 못만듬... 
	int grade; // 학년
	int score;
}
class Teacher extends Person{ // Person 클래스를 확장하는 Teacher 클래스
	String subject;
}
class Employee extends Person {
	String department;
	String position;
	int salary;
}
public class Test02 {
	public static void main(String[] args) {
		Teacher t = new Teacher();
		t.name = "이푸린";
		t.age = 25;
		t.tel = "010-1111-1111";
		t.subject = "JAVA";
		
		t.showInfo();
		System.out.println("담당과목 : " + t.subject);
		// Teacher는 Person의 모든 필드를 사용할 수 있다. ==> 확장
	}
}

```

