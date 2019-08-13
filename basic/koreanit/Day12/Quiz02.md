# Quiz02

```


public class Quiz02 {
	public static void main(String[] args) {
		char[] chArr = { 'p','o','k','E','M','o','N' };
		
		System.out.println(chArr); // pokEMoN
		System.out.println();
		
		for (int i = 0; i < chArr.length;i++) {
			if (chArr[i] >= 'a' && chArr[i] <= 'z') {
				chArr[i] -= 32;
			}
		}
		System.out.println(chArr); // POKEMON
		System.out.println();
		
		for (int i = 0; i < chArr.length; i++) {
			chArr[i] += 32;
		}
		System.out.println(chArr); // pokemon
		
//		위 세 단어가 잘 출력되도록 sysout 중간 중간에 for문을 사용하여 코드를 완성하세요.
		
	}
}

```

