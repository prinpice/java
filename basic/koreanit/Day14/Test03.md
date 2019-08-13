# Test03

```java

public class Test03 {
	public static void main(String[] args) {
		// 2차원 배열
		int[][] arr = new int[4][3];
		                 //  [행의 개수][열의 개수]
		                 //  행 : 가로줄 (row)
		                 //  열 : 세로줄 (column)
		arr[0] = new int[] {1, 2, 3}; // 0번 행에 1, 2, 3 저장
		arr[1] = new int[] {4, 5, 6}; // 1번 행에 4, 5, 6 저장
		arr[2] = new int[] {7, 8, 9};
		arr[3] = new int[] {10, 11, 12};
		
		for (int i = 0; i < arr.length; ++i) { // 이차원 배열.length :행의 개수 (4)
			for(int j = 0; j < arr[i].length; ++j) { // 이차원배열[i].length : i 번째 행의 칸개수 (3)
				System.out.print(arr[i][j]+"\t");
			}
			System.out.println();
		}
		
		System.out.println(arr[2][0]); // 7
		
		int[][] arr2 = new int[4][]; // 열의 개수 미정
		arr2[0] = new int[3]; // 0번 행의 열 개수를 지정
		arr2[1] = new int[5]; // 1번 행의 열 개수를 지정
		arr2[2] = new int[2];
		arr2[3] = new int[4];
		
	}
}

```

