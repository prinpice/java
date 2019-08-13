# Quiz01

```
import java.util.Scanner;

/*
 * 1. Student 클래스 
 *  - 멤버변수(=필드) 선언
 *   이름, 국, 영, 수, 평균, 합격여부(boolean)
 * 
 * 2. Quiz01 메인클래스 
 *  - Student 인스턴스를 3개 생성하여 
 *  - Scanner를 사용해서 학생 3명의 이름, 국, 영, 수를 입력 받는다
 *  - 모든 인스턴스의 평균과 합격 여부(평균 60점 이상이면 합격)이 계산되어 저장
 *  - 3명의 이름, 평균, 합격 여부를 출력 
 *   
 */
public class Quiz01 {
	public static void main(String[] args) {
		Student s1;
		Student s2;
		Student s3;
		
		int n;
		
		Scanner sc = new Scanner(System.in);
		s1 = new Student();
		s2 = new Student();
		s3 = new Student();
		
		System.out.print("학생1의 이름을 입력하세요>> ");
		s1.name = sc.next();
		System.out.print("학생1의 국어성적을 입력하세요>> ");
		s1.korean = sc.nextInt();
		System.out.print("학생1의 수학성적을 입력하세요>> ");
		s1.math = sc.nextInt();
		System.out.print("학생1의 영어성적을 입력하세요>> ");
		s1.english = sc.nextInt();
		s1.sum = s1.korean +s1.math +s1.english;
		s1.ave = s1.sum/3.0;
		s1.PF = (s1.ave >=60)? "합격" : "불합격";
		
		System.out.println();
		
		System.out.print("학생2의 이름을 입력하세요>> ");
		s2.name = sc.next();
		System.out.print("학생2의 국어성적을 입력하세요>> ");
		s2.korean = sc.nextInt();
		System.out.print("학생2의 수학성적을 입력하세요>> ");
		s2.math = sc.nextInt();
		System.out.print("학생2의 영어성적을 입력하세요>> ");
		s2.english = sc.nextInt();
		s2.sum =s2.korean +s2.math +s2.english;
		s2.ave = s2.sum /3.0;
		s2.PF = (s2.ave >=60)? "합격" : "불합격";
		
		System.out.println();
		
		System.out.print("학생3의 이름을 입력하세요>> ");
		s3.name = sc.next();
		System.out.print("학생3의 국어성적을 입력하세요>> ");
		s3.korean = sc.nextInt();
		System.out.print("학생3의 수학성적을 입력하세요>> ");
		s3.math = sc.nextInt();
		System.out.print("학생3의 영어성적을 입력하세요>> ");
		s3.english = sc.nextInt();
		s3.sum = s3.korean +s3.math +s3.english;
		s3.ave = s3.sum /3.0;
		s3.PF = (s3.ave >=60)? "합격" : "불합격";
		
		// s3.pass - s3.avg>=60;
		// System.out.println("결과: "+(s3.pass? "합격" : "불합격"));
		
		s1.showInfo();
		s2.showInfo();
		s3.showInfo();
		
	}
}

```

