# Test01

```java

public class Test01 {
	public static void main(String[] args) {
		int[] arr = {10, 20, 30, 40, 50};
		
		for (int tmp : arr) {
			System.out.println("확장 for문: " + tmp);
		}
		/*
		 * tmp에 arr[0] 저장 => System.out.println("확장 for문: " + tmp);
		 * tmp에 arr[1] 저장 => System.out.println("확장 for문: " + tmp);
		 * tmp에 arr[2] 저장 => System.out.println("확장 for문: " + tmp);
		 * tmp에 arr[3] 저장 => System.out.println("확장 for문: " + tmp);
		 * tmp에 arr[4] 저장 => System.out.println("확장 for문: " + tmp);
		 */
		
		// 확장 for문의 주의사항: 확장 for문은 원소를 직접적으로 수정할 수 없다.(원소 읽기 전용)
		for (int tmp2 : arr) {
			tmp2 = 0;
		}
		
		System.out.println(arr[0]);
		System.out.println(arr[1]);
		System.out.println(arr[2]);
		System.out.println(arr[3]);
		System.out.println(arr[4]);
	}
}

```

