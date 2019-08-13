# Person2

```java
package package2;
/*
 * <접근제어자 (= 접근제한자, access modifiers)>
 * - 대상의 노출 범위를 지정하는 키워드 4개
 * - 클래스, 멤버메소드, 멤버변수, 생성자에 붙일 수 있음
 * 
 * 
 * 
 *                     클래스내             패키지내부                   외부패키지                
 * 1. public    :        O            O              O
 * 2. protected :        O            O              X(단, 자식클래스에게는 보여줌)
 * 3.           :        O            O              X
 * 4. private   :        O            X              X
 * 
 * ** public    : 모두에게 보여주겠다
 * ** protected : 같은 패키지의 클래스들에게는 보여줌, 외부패키지의 클래스들에게는 안보여줌
 * **           : 같은 패키지의 클래스들에게만 보여줌
 * ** private   : 나만 볼거야!(클래스 안에서만 사용, 외부에게는 절대 노출 X)
 * 
 * < 객체의 은닉화>
 * - 보여줄 것만 보여준다.
 * - 객체 무결성을 위해
 *  ** 객체 무결성 : 객체의 데이터가 오염되지 않는 것
 *  <객체의 캡슐화>
 *  -은닉화를 구현하기 위한 보호막치기
 *  -getter, setter를 통해서 캡슐화를 구현
 */
public class Person2 {
	
//	String name;
//	int age;
//	String tel;
	
	// 필드 (멤버변수)는 private으로
	private String name;
	private int age;
	private String tel;
	
	// 보호막 메소드 (중간다리 역할)는 public으로
	public void setName(String name) {
		if(name == null) {
			this.name = "없음";
		}else {
			this.name = name;
		}
	}
	public void setAge(int age) {
		if (age >=0 && age <= 180) {
			this.age = age;
		}else {
			this.age = 0;
		}
	}
	public void setTel(String tel) {
		if (tel == null) {
			this.tel = "없음";
		}else {
			this.tel = tel;
		}
	}
	
	// 간접적으로 노출하는 '보여주기용 메소드' ==> getters
	public String getName() {
		return name;
	}
	public int getAge() {
		return age;
	}
	public String getTel() {
		return tel;
	}
}

```

