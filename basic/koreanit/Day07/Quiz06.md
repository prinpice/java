# Quiz06

```
import javax.swing.JOptionPane;

public class Quiz06 {
	/*
	 * Math.random()을 사용하여 구구단 퀴즈를 랜덤하게 내고,
	 * 답을 입력 받은 후 맞으면 "정답!", 틀리면 "땡!"을 출력하세요.
	 * (랜덤하게 2개 수를 뽑아야 합니다.) 
	 */
	public static void main(String[] args) {
		int rand1, rand2;
		int answer;
		
		rand1 = (int)(Math.random() * 9) + 1;
		rand2 = (int)(Math.random() * 9) + 1;
		
		String sAnswer = JOptionPane.showInputDialog(null, rand1+"*"+rand2+"=");
		answer = Integer.parseInt(sAnswer);
		
		if (answer == rand1 * rand2) {
			JOptionPane.showMessageDialog(null, "정답!");
		}
		else {
			JOptionPane.showMessageDialog(null, "땡!");
		}
		
		
	}
}

```

