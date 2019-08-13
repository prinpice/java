# Quiz02

```java
import java.util.Scanner;

class Pokemon{
	String name;
	int lv;
	
	void greet() {
		// 안녕하세요, 저는 xx입니다! 를 출력(sysout)
		System.out.println("안녕하세요, 저는 " + name + "입니다!");
	}
	
	void greet(int yourLevel) {
		// 인자값으로 들어온 yourLevel이 이 포켓몬의 레벨보다 크면 존댓말
		// 안녕하세요, 저는 xx입니다! 를 출력(sysout)
		// 작으면 반말
		// 안녕? 나는 xx야~
		System.out.println(yourLevel > lv ? "안녕하세요, 저는 " + name + "입니다!" : "안녕? 나는 " + name + "야~"); 
//		if (yourLevel > lv) {
//			greet();
//		}else {
//			System.out.println("\"안녕? 나는 \" + name + \"야~\"");
//		}
	}
	
	void greet(Pokemon another) {
		// 인자값으로 들어온 another포켓몬의 레벨보다 크면 존댓말
		// 안녕하세요, 저는 xx입니다! oo님 반갑습니다.  // (oo이 another포켓몬)
		// 작으면 반말
		// 안녕? 나는 xx야~ oo야 반가워~
		System.out.println(another.lv > lv ? "안녕하세요, 저는 " + name + "입니다! " + another.name +"님 반갑습니다." : "안녕? 나는 " + name + "야~ "+ another.name +"야 반가워~"); 
	}
}
public class Quiz02 {
	public static void main(String[] args) {
		Pokemon p1 = new Pokemon();
		Pokemon p2 = new Pokemon();
		
		Scanner sc = new Scanner(System.in);
		
		System.out.print("포켓몬의 이름을 입력하세요>>");
		p1.name = sc.next();
		System.out.print("포켓몬의 레벨을 입력하세요>>");
		p1.lv = sc.nextInt();
		
		System.out.print("포켓몬의 이름을 입력하세요>>");
		p2.name = sc.next();
		System.out.print("포켓몬의 레벨을 입력하세요>>");
		p2.lv = sc.nextInt();
		
		p1.greet();
		
		p1.greet(25); // yourLevel
		
		p1.greet(p2);
		p2.greet(p1);
		
		
		
	}
}

```

