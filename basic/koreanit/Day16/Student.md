# Student

```java

public class Student {
	String name; // 멤버변수(필드)
	int kor, eng, mat;
	double avg;
	char grade;
	
	// 선언을 제외한 모든 명령은
	// 메소드 안에서만 작성할 수 있음
	
	// name = "김피카츄"; (X) 
	
	
	// 이름, 국, 영, 수를 인자값(재료)으로 넣었을 때
	// 각 데이터들이 필드에 저장되고
	// 평균, 등급(A, B, C, D, F) 자동으로 계산되어 필드에 저장됨
	
	
	// <메소드 쉽게 만드는 법>
	// 1. 제목 + () + {}
	// 2. 입력값(input) 정하기( ()소괄호 안에 들어가는)
	// 3. 본문 작성
	
	void setStudent(String iname, int ikor, int ieng, int imat){ 
		name = iname;
		kor = ikor;
		eng = ieng;
		mat = imat;
		avg = (kor + eng + mat) / 3.0;
		grade = avg >= 90 ? 'A': ((avg >=80)? 'B': ((avg >= 70)? 'C': ((avg >= 60)? 'D': 'F')));
		return; // 생략가능
	}
	
	// 이름, 평균, 등급을 String형태로 return함
	String getInfo(){
		String info = "이름 : " + name + "\n"
				    + "평균 : " + avg + "점\n"
				    + "등급 : " + grade + "\n";
		return info;
	}
	
	// 사용 예. System.out.println(s1.getInfo());
	//        JOptionPane.showMessageDialog(null, s1.getInfo());
	
	// 메인메소드에 학생 4개짜리 배열을 생성 후 이름, 국, 영, 수를 입력 받고 정보 출력
	// => setStudnet()와 getInfo()를 사용
}

```

