# Quiz02

```
import javax.swing.JOptionPane;

public class Quiz02 {
	public static void main(String[] args) {
		/*
		 * < 사칙 연산 계산기 만들기 >
		 * 두 수와 기호(+,-,*,/)를 입력 받고
		 * 결과를 출력하세요.
		 */
		String operator;
		double n1, n2;
		String sN1, sN2;
		
		sN1 = JOptionPane.showInputDialog("연산을 할 첫 번째 수를 입력하세요");
		sN2 = JOptionPane.showInputDialog("연산을 할 두 번째 수를 입력하세요");
		operator = JOptionPane.showInputDialog("연산기호(+, -, *, /)중 하나를 골라주세요");
		n1 = Integer.parseInt(sN1);
		n2 = Integer.parseInt(sN2);
		
		switch(operator) {
		case "+":
			JOptionPane.showMessageDialog(null, n1+"+"+n2+"="+(n1+n2));
			break;
		case "-":
			JOptionPane.showMessageDialog(null, n1+"-"+n2+"="+(n1-n2));
			break;
		case "*":
			JOptionPane.showMessageDialog(null, n1+"*"+n2+"="+(n1*n2));
			break;
		case "/":
			JOptionPane.showMessageDialog(null, n1+"/"+n2+"="+(n1/n2));
			break;
		default:
			JOptionPane.showMessageDialog(null, "잘못 입력하셨습니다.");
		}
		
	}
}

```

