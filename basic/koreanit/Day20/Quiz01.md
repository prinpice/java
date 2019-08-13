# Quiz01

```java
// 설계 관점에서 철저하고, 사용자 입장에서 편하게 사용할 수 있도록 만들어야 함
class Student {
	private String name;
	private int kr, en, ma;
	private double avg;
	private boolean pass;
	private char grade;

	// 1. 생성자 (여러분 마음대로 여러 개 만들기)
	public Student() {}
	public Student(String name) {
		setName(name); // this.name = name; 둘 중 아무거나 사용해도 상관없음
	}
	public Student(String name, int kr, int en, int ma) {
		setName(name); // this.name = name;
		setKr(kr); //  this.kr = kr;  => 이 상황에서는 setter활용이 더 좋음 : this를 사용하면 avg를 다시 구해야 하며 잘못 입력하였을 때의 오류를 잡지 못하여 무결성을 지켜주지 못함
		setEn(en); // this.en = en;
		setMa(ma); // this.ma = ma;
	}
	// 2. getters (형식에 맞게)
	public String getName() {
		return name;
	}

	public int getKr() {
		return kr;
	}

	public int getEn() {
		return en;
	}

	public int getMa() {
		return ma;
	}

	public double getAvg() {
		return avg;
	}

	public boolean isPass() {
		return pass;
	}

	public char getGrade() {
		return grade;
	}

		// 3. setters (재료를 넣으면 검열을 거쳐 올바른 데이터만 들어감)
		// 0) name : 이름
		public void setName(String name) {
			this.name = name;
		}

		// 1) kr, en, ma : 0 점 이상 100점 이하만 저장 가능, 그 외 0점
		public void setKr(int kr) {
			this.kr = kr >= 0 && kr <= 100? kr : 0;
			setAvg();
		}
		
		public void setEn(int en) {
			this.en = en >= 0 && en <= 100? en : 0;
			setAvg();
		}
		
		public void setMa(int ma) {
			this.ma = ma >= 0 && ma<= 100? ma : 0;
			setAvg();
		}
		// 2) avg : (인자값 받지 않고 kr, en, ma만 가지고 계산되도록)
		private void setAvg() { // 외부에서 부를 필요가 없으며 내부에서 자동으로 실행되기 때문에 굳이 밖에 보여줄 필요없음 => 은닉화 ==> public -> private
			avg = (kr + en + ma)/3.0;
			setPass(); 
			setGrade();
		}
		// 3) pass : 60점 이상이면 true
		private void setPass() { 
			pass = avg >= 60;

		}

		// 4) grade : ABCDF 중 1개로
		private void setGrade() {
			grade = avg >= 90 ? 'A' : avg >= 80 ? 'B' : avg >= 70 ? 'C' : avg >= 60 ? 'D' : 'F'; // 필드 이름과 고유변수가 이름이 달라서 this 생략가능
		}
		
	}

public class Quiz01 {
	public static void main(String[] args) {
		// Student 테스트 (마음대로)
		Student st = new Student();
		st.setName("김피카츄");
		st.setKr(100);
		st.setEn(85);
		st.setMa(80);
		// st.setAvg();
		// st.setPass(); // 여기서 굳이 선언해줄 필요 없는 내용
		// st.setGrade();
		
		System.out.println("이름 : " + st.getName());
		System.out.println("국어 : " + st.getKr());
		System.out.println("수학 : " + st.getMa());
		System.out.println("영어 : " + st.getEn());
		System.out.println("평균 : " + st.getAvg());
		System.out.println("패스 : " + st.isPass());
		System.out.println("등급 : " + st.getGrade());
	}
}


```

