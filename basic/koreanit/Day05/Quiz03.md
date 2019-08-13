# Quiz03

```java
import java.util.Scanner;

/*
 * 조건연산자 문제(3)
 * - 우리는 딸기를 팔고 있습니다. 딸기의 가격은 2000원입니다.
 *   우리의 유일한 VIP 고객이 한명 있습니다.
 *   VIP 고객의 아이디와 비밀번호는 각각 "pika"와 "pika1234"입니다.
 *   
 *   아이디, 비밀번호를 입력 받았을 때, 
 *   VIP 고객이라면 20% 할인해서 판매하세요.
 *   
 *   e.g. 
 *    
 *    ID: (콘솔창 클릭 후 입력)
 *    PW: (콘솔창 클릭 후 입력)
 *    
 *    ( VIP라면 )
 *    현재 고객님은 VIP이십니다. 20% 할인 적용하여 1600원입니다. 
 *    
 *    ( VIP가 아니라면 )
 *    현재 고객님은 일반 고객이십니다. 2000원입니다.
 *   
 */
public class Quiz03 {
	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		
		System.out.print("ID: ");
		String ID = sc.next();
		System.out.print("PW: ");
		String PW = sc.next();
		
		String message = (ID.equals("pika") && PW.equals("pika1234")) ? "현재 고객님은 VIP이십니다. 20% 할인 적용하여 1600원입니다." : "현재 고객님은 일반 고객이십니다. 2000원입니다.";
		System.out.println(message);
	}
}

```

