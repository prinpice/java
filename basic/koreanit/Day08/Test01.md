# Test02

```
import java.util.Scanner;

public class Test01 {
	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		int num;
		System.out.println("정수 1개: ");
		num = sc.nextInt();
		
		switch(num){
		case 1: // ~~: ==> 레이블(label), 책갈피 역할
			System.out.println("1이네염");
			break; //switch문을 종료하라! // break;가 입력되지 않으면 계속 다음 case가 실행된다.
		case 2: // case옆에는 고정값만 들어갈 수 있음. 변수(x)
			System.out.println("2가 입력됨!");
			break;
		case 3:
			System.out.println("3이군요!");
			break;
		case 4: case 5:
			System.out.println("4 혹은 5를 입력하셨습니다.");
			break;
		default:
			System.out.println("1 ~ 5 이외의 숫자입니다!");
		}
		System.out.println("당신이 입력한 정수는 " + num +"입니다.");
	}
}

```

