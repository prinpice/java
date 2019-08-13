# Test02

```java
/*
 * static으로 선언된 멤버는 모든 객체들이 공유한다.
 * => 프로그램 통틀어 1개만 만들어짐
 */
class Player {
	String name;
	static boolean win;
}
// 참고.. class는 설계도
public class Test02 {
	public static void main(String[] args) {
		Player p1 = new Player();
		p1.name = "피카츄";
		Player p2 = new Player();
		p2.name = "라이츄";
		Player p3 = new Player();
		p3.name = "꼬부기";
		
		System.out.println("====현재 win의 상황====");
		System.out.println("p1.win : " + p1.win); // p1.win으로 써도 되지만 static한 접근방식이 아니기 떄문에 Player.win으로 써주는 것이 좋다. 
		// Player.win이 가장 가까운 길이라면 p1.win은 돌아가는 길과 같음
		System.out.println("p2.win : " + p2.win);
		System.out.println("p3.win : " + p3.win);
		
		System.out.println("===> 꼬부기가 캐리했다! ");
		p3.win = true; // win이 static이기 때문에 class의 win에 저장이 되며(p3 뿐만 아니라) 모든 win(p1, p2에도)에 공유가 된다. // static한 접근방식이 아님, 비효율적
		// Player.win  = false; // win이 어디 class인지 구분이 되야 하기 때문에 앞에 class이름을 붙여줌 // static한 접근방식
		
		System.out.println("====변경 후 win의 상황====");
		System.out.println("p1.win : " + p1.win);
		System.out.println("p2.win : " + p2.win);
		System.out.println("p3.win : " + p3.win);
	}
}

```

