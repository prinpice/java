# Nation 문제 예시 코드

```java
package quiz;

import java.util.ArrayList;

import javax.swing.JOptionPane;

class Nation {
	String nation; // 국가명
	String capital; // 수도
	int pop; // 인구
	// 1. 생성자 만들기 
	Nation(String nation, String capital, int pop){
		this.nation = nation;
		this.capital = capital;
		this.pop = pop;
	}
	
	// 2. toString() 오버라이드 : 국가이름, 수도, 인구수를 보여줌
	@Override
	public String toString() {
		return nation + "/" + capital + "/약" + pop + "명";
	}
}

public class Quiz02 {
	public static void main(String[] args) {
		String menu = "1. 국가 추가\n"
					+ "2. 모든 국가 보기\n"
				//  + "3. 국가 검색 \n" 
				//      ==> 국가명을 입력 받고 해당 국가 정보 출력, 없으면 "미등록 국가"
					+ "0. 종료 \n";
		// ArrayList를 활용하여 프로그램을 작성하세요.
		String select;
		String tmpNation;
		String tmpCapital;
		int tmpPop;
		ArrayList<Nation> list = new ArrayList<Nation>();
		while(true) {
			select = JOptionPane.showInputDialog(menu); 
			if("1".equals(select)) { // 국가 등록
				tmpNation = JOptionPane.showInputDialog("새 국가명"); 
				tmpCapital = JOptionPane.showInputDialog(tmpNation + "의 수도");
				tmpPop = Integer.parseInt(JOptionPane.showInputDialog(tmpNation+ "의 인구수"));
				list.add(new Nation(tmpNation, tmpCapital, tmpPop));
				JOptionPane.showMessageDialog(null, "국가 등록 완료!");
			} else if("2".equals(select)) { // 모든 국가 보기 
				String message = "===== 국가 리스트 =====\n";
//				for(Nation n : list) {
//					message += n.toString() + "\n"; 
//				}
				for(int i = 0; i<list.size(); ++i) {
					message += (i+1) + ". " + list.get(i).toString() + "\n";
				}
				JOptionPane.showMessageDialog(null, message);
			} else if("3".equals(select)) { // 국가 검색 
				tmpNation = JOptionPane.showInputDialog(null, "찾으시는 국가명");
				boolean check = false;
				for(Nation n : list) {
					if(n.nation.equals(tmpNation)) {
						JOptionPane.showMessageDialog(null, n);
						check = true;
						break;
					}
				}
				if(!check ) {
					JOptionPane.showMessageDialog(null, "미등록 국가");
				}
			} else if("0".equals(select)) {
				JOptionPane.showMessageDialog(null, "프로그램을 종료합니다.");
				return;
			} else {
				JOptionPane.showMessageDialog(null, "다시 입력하세요.");
			}
					
		}
		
	}
}

```

