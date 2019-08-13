# Test02

```java
// 파일이름 = 클래스명 같아야 한다!
// 이름 수정: 파일 클릭 + F2
public class Test02 {
	public static void main(String[] args) {
		System.out.println(10);
		System.out.println(10 + 20);
		System.out.println("ABC"); // 여러 글자 데이터(문자열)는 ""
		System.out.println('가'); // 한 글자 데이터(단일문자)는 ''
		System.out.println("ABC" + 10);
		System.out.println(10 + 20 + "ABC"); // 문자열 등장 전까지 덧셈
		System.out.println("ABC" + 10 + 20); // 문자열 등장 후부터 붙임
		
		//                    "ABC10" + 20  ==> "ABC1020"
		System.out.println(10 + 20 + "ABC" + 10 + 20);
		System.out.println(10 + 20 + "ABC" + (10 + 20)); // 문자열이 아닌 숫자, 산술연산하려면 소괄호
        //      "ABC" + 10 + 20 ==> "ABC30"
		System.out.println(3.14 + 10);
		//sysout(System out 줄인말) : 소괄호 안의 데이터를 consol(cmd)창에 출력하는 명령
		
	}

}

```

