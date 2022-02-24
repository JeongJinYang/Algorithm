# 자릿수 더하기

```java
/*문제 설명
자연수 N이 주어지면, N의 각 자릿수의 합을 구해서 return 하는 solution 함수를 만들어 주세요.
예를들어 N = 123이면 1 + 2 + 3 = 6을 return 하면 됩니다.

제한사항
N의 범위 : 100,000,000 이하의 자연수*/

public class AddDigit {

	public static void main(String[] args) {
		
		int n = 987; 
		int sum = 0;
		int temp = n;
		
		for (int i = 0; i < (int)( Math.log10(n)+1) ; i++) {
			sum += temp%10;
			temp = temp/10;
		}

		System.out.println("sum : " + sum);
	}

}

```
