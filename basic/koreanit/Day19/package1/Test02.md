# Test02

```java
package package1;
import java.util.Scanner;

class Sample2{
	static int Level;
	
	
	
	// static 초기화 블럭 ( ==> {})
	static { // 이 클래스에 선언된 static 멤버를 초기화할 때 사용한다.
		Scanner sc = new Scanner(System.in);
		System.out.println("레벨 : ");
		Level = sc.nextInt();
	}
}
public class Test02 {
	public static void main(String[] args) {
		System.out.println(Sample2.Level);
	}
}

```

