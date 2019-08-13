# Test03

```
/*
 * <분기문>
 * 1. break
 *  - 자신이 속한 반복문(while, do-while, for), switch문을 종료한다.
 * 2. continue
 *  - 자신이 속한 반복문에 남아있는 종속문장을 건너 뛴다.
 *  - 반복 유지
 * 3. return
 *  - 자신이 속한 메소드를 종료한다.
 *  - 예) 메인메소드의 return => 메인메소드 종료 == 프로그램 종료
 */
public class Test03 {
	public static void main(String[] args) {
		System.out.println("---break test----");
		for (int n= 10; n > 0; --n) {
			if (n %4 == 0) {
				break;
			}
			System.out.println(n); 
		}
		// for문만 종료하기 때문에 아래의 프로그램으로 넘어가서 실행한다.
		
		System.out.println("---continue test----");
		for (int n= 10; n > 0; --n) {
			if (n %4 == 0) {
				continue; // 밑에 남아있는 종속문장(sysout)을 건너뛰어라
			}
			System.out.println(n); // 4의 배수 제외하고 출력
		}
		
		System.out.println("---return test----");
		for (int n= 10; n > 0; --n) {
			if (n %4 == 0) {
				return; // 메인메소드 종료
			}
			System.out.println(n); 
		}
		
		// return을 통해 메인메소드가 종료되어 아래의 프로그램은 실행되지 않는다.
		
		System.out.println("---break test----");
		for (int n= 10; n > 0; --n) {
			if (n %4 == 0) {
				break;
			}
			System.out.println(n); 
		}
	}
	
}

```

