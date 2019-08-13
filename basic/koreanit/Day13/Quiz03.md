# Quiz03

```
import java.util.Scanner;

/*
 
 *  - Student 인스턴스를 3개 생성하여 
 *  - Scanner를 사용해서 학생 3명의 이름, 국, 영, 수를 입력 받는다
 *  - 모든 인스턴스의 평균과 합격 여부(평균 60점 이상이면 합격)이 계산되어 저장
 *  - 3명의 이름, 평균, 합격 여부를 출력 
 *  => Student[]로 구현
 *   
 */
class Student{
	String name;
	int kr;
	int ma;
	int en;
	double avg;
	String pf;
}
public class Quiz03 {
	public static void main(String[] args) {
		Student[] sArr = new Student[3];
		
		Scanner sc = new Scanner(System.in);
		
		for ( int j = 0; j < sArr.length; j++) {
			sArr[j] = new Student();
			System.out.print("학생의 이름을 입력해주세요>> ");
			sArr[j].name = sc.next();
			System.out.print("학생의 국어점수를 입력하세요>> ");
			sArr[j].kr = sc.nextInt();
			System.out.print("학생의 수학점수를 입력하세요>> ");
			sArr[j].ma = sc.nextInt();
			System.out.print("학생의 영어점수를 입력하세요>> ");
			sArr[j].en = sc.nextInt();
			sArr[j].avg = (double)(sArr[j].kr + sArr[j].ma + sArr[j].en)/3.0;
			sArr[j].pf = (sArr[j].avg >= 60)? "합격": "불합격";
		}
		
		// [0] => [i] 바꾸는 방법: 바꿀 범위 드래그-> ctrl + f -> Find: 바꿀내용, Replace with: 바꾸고싶은내용
		
		for (int i = 0; i < sArr.length; i++) {
			System.out.println("이름 : " + sArr[i].name);
			System.out.println("국어점수 : " + sArr[i].kr + "점");
			System.out.println("수학점수 : " + sArr[i].ma+"점");
			System.out.println("영어점수 : " + sArr[i].en+"점");
			System.out.println("평균 : " + sArr[i].avg+"점");
			System.out.println("결과:" + sArr[i].pf);
		}
		
	}
}

```

