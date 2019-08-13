# Test02

```
import javax.swing.JOptionPane;

public class Test02 {
	public static void main(String[] args) {
		String menu = "1. 입력\n2. 출력\n3. 종료";
		String input = "(없음)";
		String select; // 번호 선택용
		while(true) {
			select = JOptionPane.showInputDialog(menu);
			if (select.equals("1")) { // select == "1" (X)
				input = JOptionPane.showInputDialog("아무거나 입력하셈.");
			}
			else if (select.equals("2")) {
				JOptionPane.showMessageDialog(null, "현재 값:"+input);
			}
			else if (select.equals("3")) {
				JOptionPane.showMessageDialog(null, "프로그램 종료");
				break; // while문 종료
			}
			else {
				JOptionPane.showMessageDialog(null, "다시 입력하세요.");
			}
		}
	}
}

```

