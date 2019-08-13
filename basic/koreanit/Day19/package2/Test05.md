# Test05

```java
package package2;

public class Test05 {
	public String pubStr    = "나는 public~";
	protected String proStr = "나는 Protect~";
	String defStr           = "나는 default~";
	private String priStr   = "나는 private~";
	
	public static void main(String[] args) {
		// 클래스 내부
		Test05 t = new Test05();
		System.out.println(t.pubStr);
		System.out.println(t.proStr);
		System.out.println(t.defStr);
		System.out.println(t.priStr);
		// 모두 사용 가능!
	}
}

```

