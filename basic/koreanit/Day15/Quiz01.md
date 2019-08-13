# Quiz01

```java
import javax.swing.JOptionPane;

/*
 * 클래스 : Rectangle
 *  - 필드(멤버변수) : base, height
 *  - 메소드 
 *    1) setData() : 두 정수를 인자값으로 받아, 객체의 base, height에 각각 저장
 *    2) getArea() : 넓이를 리턴
 *    3) getCircum() : 둘레를 리턴
 * 
 * 메인 클래스 : Quiz01
 *  - Rectangle 객체 1개 생성 
 *  - JOptionPane을 사용하여 밑변, 높이를 입력 받고, 
 *    Rectangle 객체에 저장 (setData() 사용)
 *  - 이 사각형 객체의 넓이와 둘레를 메소드를 사용하여 출력 (getArea(), getCircum())
 */	
class Rectangle {
	double base;
	double height;
	
	void setData(double inBase, double inHeight) {
		base = inBase;
		height = inHeight;
	}
	
	double getArea() {
		double area = base * height;
		return area;
	}
	
	double getCircum() {
		double circum = 2*(base + height);
		return circum;
	}
	
}
public class Quiz01 {
	public static void main(String[] args) {
		Rectangle rc = new Rectangle();
		
		String sBase = JOptionPane.showInputDialog("밑변을 입력하세요.");
		String sHeight = JOptionPane.showInputDialog("높이를 입력하세요.");
		
		double base = Double.parseDouble(sBase);
		double height = Double.parseDouble(sHeight);
		
		rc.setData(base, height);
		JOptionPane.showMessageDialog(null, "사각형의 넓이는 "+rc.getArea()+"입니다.\n사각형의 둘레는 "+rc.getCircum()+"입니다.");
		
	}
}

```

