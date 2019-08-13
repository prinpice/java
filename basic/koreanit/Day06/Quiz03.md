# Quiz03

```java
import javax.swing.JOptionPane;

public class Quiz03 {
	public static void main(String[] args) {
		// 이름, 나이를 입력받고,
		// xx님은 @@살이시군요! 를 출력
		// => JOP사용
		
		String name = JOptionPane.showInputDialog("이름을 입력하세요>>");
		String sage = JOptionPane.showInputDialog("나이를 입력하세요>>");
		JOptionPane.showMessageDialog(null, name+"님은 " + sage+"살이시군요!");
		
		// int age = (int)sage; // 사용안됨
		int age = Integer.parseInt(sage);
		System.out.println(age >= 20 ? "성인" : "미성년자");
		
	}
}

```

