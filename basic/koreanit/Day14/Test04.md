# Test04

```java
import javax.swing.JOptionPane;
/*
 * <메소드(Method)>
 * - 함수(기능)
 * - == 기계 (재료를 넣으면.. 결과물이 나온다)
 */
class Pokemon{
	String name;
	int level;
	int hp;
	
	void setPokemon(String n, int l) {
		name = n;
		level = l;
		hp = level * 10;
	}
	
	String getInfo() {
		String info = "이름: " +name + "\n"
				    + "레벨: " +level+"\n"
				    + "체력: " +hp;
		return info;
	}
	
	void greet(String master) {
		System.out.println(master + "님, 안녕하세요!");
		System.out.println("저는 " + name + "입니다!");
	}
}
public class Test04 {
	public static void main(String[] args) {
		Pokemon p1 = new Pokemon();
		Pokemon p2 = new Pokemon();
		Pokemon p3 = new Pokemon();
		
		p1.setPokemon("피카츄", 10); // 단어 끝에 소괄호가 붙으면 메소드(Method)이다.
		p2.setPokemon("라이츄", 20);
		p3.setPokemon("푸린", 2);
		
		p1.greet("지우");
		p2.greet("이슬이");
		p3.greet("웅이");
		
		String message = "=========== 포켓몬 정보 ===========\n"
				       + p1.getInfo() + "\n"
				       + p2.getInfo() + "\n"
				       + p3.getInfo() + "\n";
		JOptionPane.showMessageDialog(null, message);
		
	}
}

```

