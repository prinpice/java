# Quiz02

```java
import javax.swing.JOptionPane;

/*
 * 클래스 : MyMath
 *  - 필드 : 없음
 *  - 메소드 
 *    1) getTotal()	: 정수 1개를 인자값으로 받고, 1 부터 그 수까지의 모든 합을 return
 *      e.g. 인자값 : 5 -> 리턴값 : 10
 *           인자값 : 3 -> 리턴값 : 6
 *    2) getGugudan() : 정수 1개를 인자값으로 받고, 해당 단을 String형태로 return 
 *  
 * 메인 클래스 : Quiz02
 * 	메뉴 : 
 *    1. 총합 구하기
 *    2. 구구단 보기
 *    3. 종료하기
 *  - 1번 선택 시 : 정수 1개를 입력 받아 1 ~ 정수까지의 합 출력
 *  - 2번 선택 시 : 정수 1개를 입력 받아 해당 단 출력
 *  - 3번 선택 시 : 프로그램 종료 
 *    (3번을 선택해야 메뉴창 띄우기를 반복 종료함.)
 */
class MyMath {
	int getTotal(int num) {
		int sum = 0;
		for (int i = 1; i <= num; i++) {
			sum += i;
		}
		return sum;
	}

	String getGugudan(int num) {
		String message = null;
		message = num + "*" + 1 + "=" + (1 * num) + "\n";
		for (int i = 2; i <= 9; i++) {
			message += num + "*" + i + "=" + (i * num) + "\n";
		}
		return message;
	}
}

public class Quiz02 {
	public static void main(String[] args) {
		MyMath mm = new MyMath();

		String menu;
		menu = "메뉴:\n";
		menu += "  1. 총합 구하기\n";
		menu += "  2. 구구단 보기\n";
		menu += "  3. 종료하기\n";
		menu += "번호를 입력하세요.";

		while (true) {

			String sSel = JOptionPane.showInputDialog(menu);
			int sel = Integer.parseInt(sSel);
			if (sel == 1) {
				String t_sNum = JOptionPane.showInputDialog("정수를 입력하세요.");
				int t_num = Integer.parseInt(t_sNum);
				int total = mm.getTotal(t_num);
				JOptionPane.showMessageDialog(null, "1 부터 " + t_num + "까지의 총 합은 " + total + "입니다.");
			} else if (sel == 2) {
				String d_sNum = JOptionPane.showInputDialog("정수를 입력하세요");
				int d_num = Integer.parseInt(d_sNum);
				String message = mm.getGugudan(d_num);
				JOptionPane.showMessageDialog(null, d_num + "단\n" + message);
			} else if (sel == 3) {
				JOptionPane.showMessageDialog(null, "종료합니다.");
				break;
			} else {
				JOptionPane.showMessageDialog(null, "잘못 입력하셨습니다.");
			}
		}
	}
}

```

