# Quiz

```java
class Student{
	String name;
	int kr, en, ma;
	double avg;
	char grade;
	
	// 프로그램에서 같은 문장 반복하는것 선호하지 않음
	
	
	// 생성자1 : 기본생성자 (매개변수 X)
	Student(){
		this("없음", 0, 0, 0);
	}
	// 생성자2 : 이름 초기화 (매개변수 : name)
	Student(String name){
		// this.name = name;
		this(name, 0, 0, 0);
	}
	// 생성자3 : 이름, 국, 영, 수 초기화 (매개변수 : name, kr, en, ma)
	//        => avg, grade 자동 저장
	Student(String name, int kr, int en, int ma){
	 // this(name);
		this.name = name;
		this.kr = kr;
		this.en = en;
		this.ma = ma;
		this.avg = (this.kr + this.en + this.ma)/3.0;
		this.grade = this.avg >= 90? 'A' : ((this.avg >=80)? 'B' : ((this.avg >= 70)? 'C' : ((this.avg >= 60)? 'D' : 'F')));
	}
	// 메소드1 : getInfo()
	//        => 이름, 국, 영, 수, 평균, 학점을 String 형태로 return
	//        => 예. System.out.println(s1.getInfo());
	String getInfo() {
//		String message = "이름 : " + this.name + "\n"
//	                   + "국어 : " + this.kr + "점\n"
//	                   + "영어 : " + this.en + "점\n"
//	                   + "수학 : " + this.ma + "점\n"
//	                   + "평균 : " + this.avg + "점\n"
//	                   + "등급 : " + this.grade;
//		return message;
		return "이름 : " + name + "\n"
                + "국/영/수 : " + kr + "/" + en + "/" + ma + "\n"
                + "평균 : " + avg + "\n"
                + "학점 : " + grade;
	}
	
}
public class Quiz01 {
	public static void main(String[] args) {
//		Student s1 = new Student();
//		
//		Student s2 = new Student("김피카츄");
//		System.out.println(s2.getInfo());
//		
//		Student s3 = new Student("이푸린", 80, 90, 99);
//		System.out.println(s3.getInfo());
		
		Student s1 = new Student();
		Student s2 = new Student("김피카츄");
		Student s3 = new Student("김피카츄", 100, 80, 85);
		System.out.println(s1.getInfo());
		System.out.println();
		System.out.println(s2.getInfo());
		System.out.println();
		System.out.println(s3.getInfo());
		System.out.println();
		
		
	}
	
}

```

