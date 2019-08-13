# Test01

```java
package package1;
class Sample{
	String str = "나는 일반 인스턴스 멤버~"; // static이 아닌 멤버 : 인스턴스 멤버(인스턴스 생성될 때 만들어짐)
	static String sStr = "나는 클래스 멤버~"; // static 멤버 : 클래스 멤버(클래스로드될 때 만들어짐)
	
	void aa() { // 인스턴스 멤버메소드    // new Sample으로 클래스가 만들어져야 만들어짐 ==> 메인메소드 후에 만들어짐
		System.out.println(str);
		System.out.println(sStr);
	}
	
	static void bb() { // 클래스 멤버메소드  // 클래스 로드로 메인메소드보다 먼저 생성됨  sample 클래스보다 먼저 생성
		// System.out.println(str); // 에러! // sample클래스가 만들어져야 생성되기 때문에 그 전에 생성되는 bb메소드에서 사용불가
		System.out.println(sStr);
	} // static 메소드는 static멤버만 사용 가능
	// 이유 : static 메소드 ===> 프로그램 시작 전에 '미리' 만들어져야 함
	//      str 변수           ===> 프로그램 진행 중, new Sample()을 해야 만들어짐
	//     ====> bb()(static)가 str(non-static)보다 먼저 만들어져야하기 때문에,
	//           아직 만들어지지 않은 str을 사용할 수 없다.
}
public class Test01 {
	static void cc() {
		System.out.println("ㅋㅋㅋㅋㅋㅋ");
	}
	public static void main(String[] args) {
		cc();
		
	}
}

```

