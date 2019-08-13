# Test01

```

public class Test01 {
	public static void main(String[] args) {
		// 포켓몬이름 5개를 저장할 수 있는 5칸짜리 String형 배열 1개 생성
		
		// 방법1.
		String[] arr1 = {"피카츄", "라이츄", "파이리", "꼬부기", "또도가스"};
		
		// 방법2.
		String[] arr2;
		arr2 = new String[] {"피카츄", "라이츄", "파이리", "꼬부기", "또도가스"};
		
		// 방법3.
		String[] arr3;
		arr3 = new String[5]; // [5] : 5칸
		arr3[0] = "피카츄"; // 0번째 칸
		arr3[1] = "라이츄"; // 1번째 칸
		arr3[2] = "파이리";
		arr3[3] = "꼬부기";
		arr3[4] = "또도가스";
		// 방법1, 2는 원소들의 개수를 자동으로 세서 알만은 개수의 칸을 생성한다.
		//  => 뭘 저장할 지 알고 있을 때 사용한다.
		// 방법3은 칸들을 미리 생성해두고 이후에 원소를 추가한다.
		// => 뭘 저장할 지 모를 때 사용한다.
		
		// int   , double   , char   : 원시자료형
		// int[] , double[] , char[] : 참조자료형 (주소의 자료형!)
		
		System.out.println(arr1[0]);
		System.out.println(arr1[1]);
		System.out.println(arr1[2]);
		System.out.println(arr1[3]);
		System.out.println(arr1[4]);
		// System.out.println(arr1[5]); // 에러!
		
		for (int i = 0; i <arr1.length; ++i) { // arr1.length : arr1의 칸 개수(=5)
			System.out.println("일반 for문 사용: "+arr1[i]);
					}
		// 확장 for문 (extended-for = foreach문)
		for (String str : arr1) {
			System.out.println("확장 for문 사용: "+ str);
		}
	}
}

```

