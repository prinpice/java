# Quiz03

```
import java.util.Scanner;

public class Quiz03 {
	public static void main(String[] args) {
		int nums[] = new int[6];
//		1. Scanner를 사용하여 6개의 데이터를 입력 받고, 이들을 nums 배열에 저장
		Scanner sc = new Scanner(System.in);
		
		for (int i = 0; i<6; i++) {
			System.out.print(i+1+"번째 숫자를 입력하세요>> ");
			nums[i] = sc.nextInt();
		}
		
//		2. 입력 받은 값 중, 20 이상 100 이하인 원소만 출력
		for (int i = 0; i < 6; i++) {
			if (nums[i] >= 20 && nums[i] <=100) {
				System.out.println(nums[i]);
			}
		}
		
//		3. 입력 받은 값 중, 최댓값과 최솟값을 출력
//		int max = nums[0];
//		int min = nums[0];
//		(for문 사용)
//		System.out.println("최댓값 : " + max);
//		System.out.println("최댓값 : " + min);
		int max = nums[0];
		int min = nums[0];
		for (int i = 0; i < 6; i++) {
			if (max < nums[i]) {
				max = nums[i];
			}
			if (min > nums[i]) {
				min = nums[i];
			}
		}
		System.out.println("최댓값: " + max);
		System.out.println("최솟값: " + min);
		
//		4. 오름차순(작은->큰)으로 정렬하여 모든 원소를 출력 
		// 선택정렬알고리즘(셀렉션 소트)
		for (int j = 0; j < 6; j++) {
			for (int i = j+1; i < 6; i++) {
				if (nums[j] > nums[i]) {
					int temp = nums[j];
					nums[j] = nums[i];
					nums[i]=temp;
				}
			}
		}
		for (int i = 0; i < 6; i++) {
			System.out.println(nums[i]);
		}
	}
}

```

