# Quiz01

```java
import java.util.Scanner;

import javax.swing.JOptionPane;

// 사용 예. System.out.println(s1.getInfo());
	//        JOptionPane.showMessageDialog(null, s1.getInfo());
	
	// 메인메소드에 학생 4개짜리 배열을 생성 후 이름, 국, 영, 수를 입력 받고 정보 출력
	// => setStudnet()와 getInfo()를 사용

public class Quiz01 {
	public static void main(String[] args) {
		Student[] st = new Student[4];
		for (int i = 0 ; i < st.length; ++i) {
			String tmpName = JOptionPane.showInputDialog(i+1 +"번 학생 이름");
			int tmpKr = Integer.parseInt(JOptionPane.showInputDialog("국어"));
			int tmpEn = Integer.parseInt(JOptionPane.showInputDialog("영어"));
			int tmpMa = Integer.parseInt(JOptionPane.showInputDialog("수학"));
			
			st[i] = new Student();
			st[i].setStudent(tmpName, tmpKr, tmpEn, tmpMa);
			JOptionPane.showMessageDialog(null, tmpName + "학생 저장 완료!");
			
		}
		
		String message = "-----------학생 리스트----------\n";
		for (Student s : st) {
			message += s.getInfo() + "\n"
					+  "-------------------------------------\n";
		}
		JOptionPane.showMessageDialog(null, message);
	}
	
	
	
}

```

