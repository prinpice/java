# Quiz01

```java
import java.util.Scanner;

// 2단 ~ 9단 중 1개의 문제를 랜덤하게 내고
// 답을 입력받고 정답 여부 출력
// "정답!" / "땡.."
public class Quiz01 {
	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		
		int randf = (int)(Math.random() * 8) + 2;
		int randb = (int)(Math.random() * 9) + 1;
		
		System.out.print(randf +" * "+ randb + " = ");
		int ans = sc.nextInt();
		
		String rw = (ans == randf * randb)? "정답!" : "땡..";
		System.out.println(rw);
		
	}
}

```

