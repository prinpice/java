# Pokemon

```java

public class Pokemon {
	String name;
	int lv;
	
	// 자기가 알아서 자기소개를 하는 메소드
	void introduce() {
		System.out.println("저는 " +name+"입니다. 레벨은 " +lv+"이죠.");
	}
	
	// 값이 두 개 들어오면 자기가 알아서 name, lv로 세팅하는 메소드
	void setData(String s, int num) {
		name = s;
		lv = num;
	}
}

```

