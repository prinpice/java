# Quiz04

```java


import java.util.Scanner;

public class Quiz04 {
	public static void main(String[] args) {
		// 1. 국,영,수 세 과목의 점수를 입력 받고
		// 2. 세 과목의 평균을 출력하세요.
		// 3. 평균이 85.5 이상이면 "합격!", 아니면 "불합격!"을 출력하세요.
		// 주의 : 85, 86, 86를 입력했을 때 합격이 출력되어야 합니다. 
		int kr, en, ma; // 국, 영, 수 점수를 저장할 변수
		double avg;     // 평균 저장할 변수
		Scanner sc = new Scanner(System.in);
		
		System.out.print("국어 점수를 입력하세요 >> ");
		kr = sc.nextInt();
		System.out.print("영어 점수를 입력하세요 >> ");
		en = sc.nextInt();
		System.out.print("수학 점수를 입력하세요 >> ");
		ma = sc.nextInt();
		
		avg = (kr + en + ma) / 3;
		
		String message = (avg >= 85.5) ? "합격!" : "불합격!";
		System.out.println("평균: " + avg);
		System.out.println(message);
		
	}
}
	
```

