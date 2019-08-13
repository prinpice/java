# Quiz05

```
import javax.swing.JOptionPane;

public class Quiz05 {
	public static void main(String[] args) {
		/*
		 * 정수 1개를 입력 받고,
		 * 입력 받은 정수가 5의 배수인지 판별하세요.
		 */
		
		String sNum = JOptionPane.showInputDialog("정수 1개를 입력하세요");
		int num = Integer.parseInt(sNum);
		if (num % 5 == 0) {
			JOptionPane.showMessageDialog(null, "5의 배수입니다.");
		}
		else {
			JOptionPane.showMessageDialog(null,	"5의 배수가 아닙니다.");
		}
		
	}
}

```

