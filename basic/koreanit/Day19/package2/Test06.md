# Test06

```java
package package2;

public class Test06 { // Test05입장에서는 같은 동네에 있는 친구임
	public static void main(String[] args) {
		// 동네친구 (같은패키지의 타 클래스)
		Test05 t = new Test05();
		System.out.println(t.pubStr);
		System.out.println(t.proStr);
		System.out.println(t.defStr);
		// System.out.println(t.priStr);
		// private뺴고 모두 사용 가능!
	}
}

```

