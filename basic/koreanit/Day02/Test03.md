# Test03

```java
/*
 * 자바의 원시자료형
 * 1. 정수형
 *  1) byte
 *   -1byte 크기의 정수
 *   
 *  2) short
 *   -2byte 크기의 정수
 *   
 *  3) int(<- 핵 중요!)
 *   -4byte 크기의 정수
 *   -자바의 기본 정수 자료형
 *   
 *  4) long
 *   -8byte 크기의 정수
 *   
 *  
 * 2. 실수형
 *  1) float
 *   -4byte 크기의 실수
 *   
 *  2) double(<- 핵 중요!)
 *   -8byte 크기의 실수
 *   
 *  
 * 3. 논리형 :boolean
 *  -1byte 크기의 참/거짓형 (true, false)
 *  
 * 4. 단일문자형 :char
 *  -2byte 크기의 문자 1개
 *  -아스키코드, 유니코드 문자
 *  
 * 5. 문자열형 (원시자료형x) :String
 * 
 */
/*
 * 1 bit 한칸 (1 or 0)
 * 1byte = 8bit
 */
public class Test03 {
	public static void main(String[] args) {
		System.out.println(1000000000); // 10억
		// System.out.println(10000000000); // 100억 ==> error =>out of range(int 범위 넘었음)
		System.out.println(10000000000L);  // L ==> long 형
		byte n1 = 100;
		// byte n1 = 1000; // => error
	}
}

```

