# Test01

```java

public class Test01 {
	public static void main(String[] args) {
		// 컴퓨터가 자동형변환 해주는가 안해주는가는 데이터 손실이 있는가 없는가에 따라 정해짐
		// int a = 3.0; // 에러! 자동형변환 안해줌 // 데이터 손실이 있기에 안해주는 것
		int a = (int)3.0; // (int) : int형으로 강제 형변환
		double b = 3; //3(int)을 3.0(double)으로 '자동형변환' // 데이터 손실이 없음
		              // b에는 형변환된 3.0이 저장됨
		System.out.println("a: " + a);
		System.out.println("b: " + b);
		System.out.println((int)3.9999999); // 결과 : 3 (반올림 안해줌) // 중요!!!!
		
		char ch = 'Y';
		// ch를 소문자로 바꾸자
		// ch = ch + 32; // 에러!  ch는 2byte, Y는 4byte (int 89), 32는 4byte
		ch = (char)(ch + 32); // 혹은 ch += 32; ==> 복합대입연산자 사용할때는 형변환 안해도됨 // 대소문자 간격 32 
		System.out.println(ch);
	}
}

```

