# Quiz01

```
import java.util.Scanner;

public class Quiz01 {
	public static void main(String[] args) {
		/*
		 * 태어난 달을 입력 받고,
		 * 그 달의 최대 일수를 출력하세요.
		 * 또한 계절도 출력하세요.
		 * 
		 * < 출력 예 >
		 * 태어난 달 : 11
		 * 11월은 30일까지 있습니다!
		 * 겨울에 태어나셨네요!
		 * 
		 * 태어난 달 : 5
		 * 5월은 31일까지 있습니다!
		 * 봄에 태어나셨네요!
		 */
		
		Scanner sc = new Scanner(System.in);
		
		System.out.println("태어난 달을 입력하세요: ");
		int month = sc.nextInt();
		System.out.println("태어난 달 : " + month);
		
		switch(month) {
		case 1: case 3: case 5: case 7: case 8: case 10: case 12:
			System.out.println(month + "월은 31일까지 있습니다!");
			break;
		case 2:
			System.out.println(month + "월은 28일까지 있습니다!");
			break;
		case 4: case 6: case 9: case 11:
			System.out.println(month + "월은 30일까지 있습니다!");
			break;
		default:
			System.out.println("잘못 입력하셨습니다.");
		}
		switch(month) {
		case 3: case 4: case 5:
			System.out.println("봄에 태어나셨네요!");
			break;
		case 6: case 7: case 8:
			System.out.println("여름에 태어나셨네요!");
			break;
		case 9: case 10: case 11:
			System.out.println("가을에 태어나셨네요!");
			break;
		case 12: case 1: case 2:
			System.out.println("겨울에 태어나셨네요!");
			break;
		default:
			System.out.println("잘못 입력하셨습니다.");
		}
		
		
	}
}
// Quiz02.java

```

