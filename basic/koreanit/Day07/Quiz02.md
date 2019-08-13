# Quiz02

```
import javax.swing.JOptionPane;

public class Quiz02 {
	public static void main(String[] args) {
//		JOptionPane을 사용하여 이름과 키, 체중을 입력 받고
//		BMI(체질량) 지수를 출력하세요.
//		w: 체중
//		t: 키 (*단위 : 미터)
//		BMI = w/(t^2) 
		String name = JOptionPane.showInputDialog("이름을 입력하세요");
		String sHeight = JOptionPane.showInputDialog("키를 입력하세요");
		String sWeight = JOptionPane.showInputDialog("체중을 입력하세요");
		int t = Integer.parseInt(sHeight)/100;
		int w = Integer.parseInt(sWeight);
		double BMI = w/(t*t);
		System.out.println(t*t);
		JOptionPane.showMessageDialog(null, name + "님의 BMI는 " + BMI + " 입니다.");
	}
}

```

