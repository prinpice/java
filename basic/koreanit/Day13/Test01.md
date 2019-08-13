# Test01

```
/*
 * <레퍼런스 배열>
 * -> 객체의 배열
 * -> 레퍼런스변수의 배열 (주소의 배열)
 */

class Person{
	String name;
	int age;
}
public class Test01 {
	public static void main(String[] args) {
		Person[] pArr = new Person[4];
		
		for (int i = 0; i < pArr.length;++i) {
			pArr[i] = new Person();
		}
		
		// pArr[0] = new Person();
		// pArr[1] = new Person();
		// pArr[2] = new Person();
		// pArr[3] = new Person();
		
		//Person[] pArr2 = {new Person(), new Person(), new Person(), new Person()}; 
		
		
		pArr[0].name = "홍길동";
		// null.name
		pArr[0].age = 14;
		pArr[1].name = "이푸린";
		pArr[1].age = 10;
		pArr[2].name = "최뚜벅초";
		pArr[2].age = 25;
		pArr[3].name = "황라이츄";
		pArr[3].age = 11;
		
		for (int i = 0; i < pArr.length; ++i) {
			System.out.println("======"+(i +1));
		}
	}
}

```

