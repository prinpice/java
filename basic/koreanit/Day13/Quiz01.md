# Quiz01

```
/*
 * 
Quiz05 < 로또 생성기 만들기 >
1 ~ 45 중 6개의 정수를 Math.random()을 사용하여 생성하고, 
이들을 출력하세요. 
중복되는 수가 나오지 않도록 해야합니다.
 */
public class Quiz01 {
	public static void main(String[] args) {
		int[] arr = new int[6];
		
		arr[0] = (int)(Math.random()*45)+1;
	
		
		int i = 1;
		int count;
		
		while (true) {
			arr[i] =(int)(Math.random()*45) + 1;
			
			
			count = 0;
			
			for (int j = 0; j < i; j++) {
				if ( arr[i] != arr[j]) {
					count++;
				}
				else if (arr[i] == arr[j]) {
					break;
				}
			}

			if (count == i) {
				i++;
			}
			if (count == 5) {
				for (int j = 0; j < arr.length; j++) {
					System.out.print(arr[j]+ "\t");
				}
				break;
			}
			
			
		}
	}
}

```

