# Quiz02

```java
package quiz;

import javax.swing.JOptionPane;

class Shape {
	public double getArea() {
		return 0.0;
	}
}
class Circle extends Shape{
	int radius;
	Circle(int r){
		radius = r;
	}
	// getArea() 오버라이드 : 원의 넓이를 return
}
class Triangle extends Shape {
	int base, height;
	Triangle(int b, int h) {
		base = b;
		height = h;
	}
	// getArea() 오버라이드 : 삼각형의 넓이를 return
}
class Rectangle extends Shape {
	int base, height;
	Rectangle(int b, int h) {
		base = b;
		height = h;
	}
	// getArea() 오버라이드 : 직사각형의 넓이를 return
}
public class Quiz02 {
	public static void main(String[] args) {
		String menu = "1. 시작\n"
					+ "2. 종료하기";
		// 1번 선택 : 원, 삼각형, 사각형 객체 중 1개를 랜덤하게 생성하고
		//           각 객체의 필드(반지름 혹은 밑변/높이)또한 1 ~ 100 중 랜덤하게 설정
		//			 생성된 객체의 넓이를 출력
		// 2번 선택 : 프로그램 종료
		String select;
		while(true) {
			select= JOptionPane.showInputDialog(menu); 
			if("1".equals(select)) {
				double rand = Math.random(); // 0.0 ~ 0.9999999999 중 1개
			} else if("2".equals(select)) {
				JOptionPane.showMessageDialog(null, "프로그램 종료");
				break;
			} else {
				JOptionPane.showMessageDialog(null, "다시 입력");
			}
		}
	}
}










```

