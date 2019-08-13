# Test03

```java
import javax.swing.JOptionPane;

// 입출력의 또다른방법: JOptionPane
public class Test03 {
	public static void main(String[] args) {
		// 메세지만!
		JOptionPane.showMessageDialog(null, "메롱메롱!");
		// 메세지 + 입력!
		JOptionPane.showInputDialog("이름을 입력하세요>> ");
		String name = JOptionPane.showInputDialog("이름");
		// 입력된 데이터는 무조건 String으로 인식됨
		// 10 입력 ==> "10"
		
		// System.out.println(name);
		// int age = JOptionPane.showInternalConfirmDialog(null, "나이를 입력하세요>"); //에러 발생
		JOptionPane.showMessageDialog(null, name+"님 안녕하세요!!!!");
		
	}
}

```

