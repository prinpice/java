# Quiz

```java
import java.util.Scanner;

class Pokemon{
	String name;
	int lv;
	
	// 현재 전체 Pokemon 객체 중 최대 레벨을 저장할 currentmaxLevel
	static int currentmaxLevel;
	// 현재 전체 Pokemon 객체의 수를 저장할 currentPokemonCount
	static int currentPokemonCount;
	
	Pokemon(){
		this("없음", 0);
	}
	
	Pokemon(String name, int lv){
		++currentPokemonCount; // 현재 포켓몬 수 1 증가
		this.name = name;
		this.lv = lv;
		setCurrentMaxLevel(); // 레벨 검사
	}
	
	void setCurrentMaxLevel() {
		if (this.lv > currentmaxLevel) {
			currentmaxLevel = this.lv;
		}
	}
}
public class Quiz01 {
	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		// 원하는 수만큼 포켓몬 객체를 생성, (가능하면 배열사용해도 됨)
		Pokemon[] parr = new Pokemon[100];
		// 자동으로 객체 수, 최대레벨이 기록되게 프로그래밍
		
		
		// 메뉴
		// 1. 포켓몬 추가
		// 2. 포켓몬 모두 보기
		// 3. 최대 레벨 보기
		// 4. 현재 포켓몬 수 보기
		//    => 배열이 있어야 함 (Pokemon[] arr = new Pokemon[10];)
		
		String message = "====== 메 뉴 ======\n" + "1. 포켓몬 추가\n" + "2. 포켓몬 모두 보기\n" + "3. 최대 레벨 보기\n" + "4. 현재 포켓몬 수 보기\n" + "5. 종료";
		
		
		// 현재 포켓몬 수 : XXX개
		
		// 최대 레벨 : XXXX
		
		while (true) {
			System.out.println(message);
			System.out.println("번호를 입력하세요>> ");
			int sel = sc.nextInt();
			System.out.println();
			
			if (sel == 1) {
				System.out.print("추가 할 포켓몬의 이름을 입력하세요 >> ");
				String name = sc.next();
				System.out.print("추가 할 포켓몬의 레벨을 입력하세요 >> ");
				int lv = sc.nextInt();
				parr[Pokemon.currentPokemonCount] = new Pokemon(name, lv);
				System.out.println();
			}
			else if (sel == 2) {
				for (int i = 0; i < Pokemon.currentPokemonCount; ++i) {
					System.out.println("이름 : " + parr[i].name);
					System.out.println("lv : " + parr[i].lv);
					System.out.println();
					System.out.println();
				}
			}
			else if (sel == 3) {
				
			}
			
			
		}
		
		
//		Pokemon.currentPokemonCount =0;
//		
//		
//		while (true) {
//			System.out.println(message);
//			System.out.print("번호를 입력하세요>> ");
//			int sel = sc.nextInt();
//			System.out.println();
//			
//			if (sel == 1) {
//				parr[Pokemon.currentPokemonCount] = new Pokemon();
//				System.out.print("추가 할 포켓몬의 이름을 입력하세요 >> ");
//				parr[Pokemon.currentPokemonCount].name = sc.next();
//				System.out.print("추가 할 포켓몬의 레벨을 입력하세요 >> ");
//				parr[Pokemon.currentPokemonCount].lv = sc.nextInt();
//				Pokemon.currentPokemonCount++;
//				System.out.println();
//			}
//			else if (sel == 2) {
//				for (int i = 0; i < Pokemon.currentPokemonCount; ++i) {
//					System.out.println("이름 : " + parr[i].name);
//					System.out.println("lv : " + parr[i].lv);
//					System.out.println();
//					System.out.println();
//				}
//			}
//			else if (sel == 3) {
//				for (int i = 0 ; i < Pokemon.currentPokemonCount; ++i) {
//					if (Pokemon.currentmaxLevel < parr[i].lv) {
//						Pokemon.currentmaxLevel = parr[i].lv;
//					}
//				}
//				System.out.println("포켓몬 중 최대 레벨은 " + Pokemon.currentmaxLevel + " 입니다.");
//				System.out.println();
//			}
//			else if (sel == 4) {
//				System.out.println("현재 포켓몬의 수는 " + Pokemon.currentPokemonCount +" 입니다.");
//				System.out.println();
//			}
//			else if (sel == 5) {
//				System.out.println("종료합니다.");
//				break;
//			}else {
//				System.out.println("잘못 입력하셨습니다.");
//				System.out.println();
//			}
//			
//		}
		
		// else 를 남발하면 안됨  ==> coutinue사용
		
		
		// 수용할 최대 포켓몬의 수도 입력받기
		// 포켓몬 레벨 바꾸기 추가
		// maxlevel이 아닌 maxlevel을 가진 포켓몬을 저장
	}
}

```

