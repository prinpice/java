# Test01

```
/*
 * <Parsing이란?>
 * : 구문분석
 * : 문자열(String)을 다른 자료형(정수, 실수, boolean)으로 변환하는 것
 * casting과 다름
 */
public class Test01 {
	public static void main(String[] args) {
		String sAge = "10"; 
		int age = Integer.parseInt(sAge);
		// int 변수 = Integer.parseInt("변환할 문자열"); // int로 변환
		// double 변수 = Double.parseInt("변환할 문자열"); // double로 변환
		// boolean 변수 = Boolean.parseInt(변환할 문자열"); 
		// 등이 있다.
		
		// age = (int)sAge; casting 사용 못하는 이유
		/*
		 * 문자가 컴퓨터에 저장될 때 아스키코드로 변환되어 저장된다. 1은 아스키코드 49에 해당된다.
		 * 숫자 10은 정수형으로 4byte이다
		 * 00000000 00000000 00000000 00001010
		 * 
		 * "10" => '1' + '0' => char, char => 4byte
		 *      => 49    48 // 아스키코드 값
		 * 00000000 00110001 00000000 00110000
		 *        '1'               '0'
		 */
		boolean bool = Boolean.parseBoolean("true");
		
	}
}

```

