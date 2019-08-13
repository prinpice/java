# Quiz01

```java
package quiz;

interface Transfer {
	int KID_CHARGE = 1000;
	int ADULT_CHARGE = 1500;
	int getCharge(int distance, int age);
}
/*
 * < Transfer 구현클래스 >
 * 1. Bus 클래스 
 * 	int getCharge(int distance, int age) 오버라이드 
 * 		=> 거리(distancem, 단위 km), 나이를 가지고 요금을 int로 return
 *  	=> 거리 20km가 넘었다면 기본요금 2배 
 *  	=> 기본 요금 : 미성년 => KID_CHARGE
 *    	     		   성년 => ADULT_CHARGE
 *    
 * 2. Taxi 클래스 
 * int getCharge(int distance, int age) 오버라이드 
 * 		=> 거리(distance, 단위 km), 나이를 가지고 요금을 int로 return
 *  	=> 기본 요금 3000원 + 5km 이상부터는 km당 1000원씩 추가
 *  	=> 미성년인 경우 20% 할인
 *  
 * 3. Subway 클래스 
 * int getCharge(int distance, int age) 오버라이드 
 * 		=> 거리(distance, 단위 km), 나이를 가지고 요금을 int로 return
 *  	=> 기본 요금 + km당 10원씩 추가
 *  	=> 기본 요금 : 미성년 => KID_CHARGE
 *    	     		   성년 => ADULT_CHARGE
 *    
 * 4. Train 클래스 
 * int getCharge(int distance, int age) 오버라이드 
 * 		=> 거리(distance, 단위 km), 나이를 가지고 요금을 int로 return
 *  	=> 10km 당 기본요금의 20% 추가
 *  	=> 기본 요금 : 미성년 => KID_CHARGE
 *    	     		   성년 => ADULT_CHARGE
 */
public class Quiz01 {

	public static void main(String[] args) {
		/*
		 *  1. 나이 입력 
		 *  2. 현재 돈 입력
		 *  2. 교통 수단 선택
		 *  	1) 버스
		 *  	2) 택시
		 *  	3) 지하철
		 *  	4) 기차
		 *  3. 키로 수(km) 입력
		 *  4. "요금은 XXXX입니다." 출력
		 *  5. 결제 가능 여부 출력 
		 *  	"현재 금액 XXX원으로 결제 가능합니다."
		 *  	"현재 금액 XXX원으로 XXX원 부족합니다."
		 * 
		 */
	}
}

```

