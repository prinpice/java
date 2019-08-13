# Quiz03

```
import java.util.Scanner;

public class Quiz03 {
	public static void main(String[] args) {
		/*
		 * 1. 국, 영, 수 점수를 입력 받아
		 *    평균을 산출하여 A,B,C,D,F 학점을 판별하세요.
		 * 
		 *    A 학점 : 평균 90점 이상
		 *    B 학점 : 평균 80점 이상 ~ 90점 미만
		 *    C 학점 : 평균 70점 이상 ~ 80점 미만
		 *    D 학점 : 평균 60점 이상 ~ 70점 미만
		 *    F 학점 : 60점 미만
		 *    
		 * 2. 위에서 산출한 평균이 60.5 이상이면 "합격"을, 아니면 "불합격"을 출력하세요.
		 *    60, 61, 61 점일 경우 평균 60.666으로 "합격"이 나와야 합니다.
		 */
		Scanner sc = new Scanner(System.in);
  		System.out.print("국어 점수를 입력하세요>> ");
  		int korean = sc.nextInt(); 
  		System.out.print("수학점수를 입력하세요>> ");
  		int math = sc.nextInt();
  		System.out.print("영어 점수를 입력하세요>> ");
  		int english = sc.nextInt();
  		
  		int score = korean + math + english;
  		double ave = score / 3.0;
  		
  		if (ave >= 90) {
  			System.out.println("A학점입니다.");
  		}
  		else if (ave >= 80) {
  			System.out.println("B학점입니다.");
  		}
  		else if (ave >= 70) {
  			System.out.println("C학점입니다.");
  		}
  		else if (ave >= 60) {
  			System.out.println("D학점입니다.");
  		}
  		else {
  			System.out.println("F학점입니다.");
  		}
  		
  		if (ave >= 60.5) {
  			System.out.println("합격입니다.");
  		}
  		else {
  			System.out.println("불합격입니다.");
  		}
  		System.out.println(ave);

	}
}
```

