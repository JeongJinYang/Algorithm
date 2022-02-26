# 소수 만들기

```java
package level1;

import java.util.Iterator;

/*문제 설명
주어진 숫자 중 3개의 수를 더했을 때 소수가 되는 경우의 개수를 구하려고 합니다. 숫자들이 들어있는 배열 nums가 매개변수로 주어질 때, nums에 있는 숫자들 중 서로 다른 3개를 골라 더했을 때 소수가 되는 경우의 개수를 return 하도록 solution 함수를 완성해주세요.

제한사항
nums에 들어있는 숫자의 개수는 3개 이상 50개 이하입니다.
nums의 각 원소는 1 이상 1,000 이하의 자연수이며, 중복된 숫자가 들어있지 않습니다.
입출력 예
nums	result
[1,2,3,4]	1
[1,2,7,6,4]	4
입출력 예 설명
입출력 예 #1
[1,2,4]를 이용해서 7을 만들 수 있습니다.

입출력 예 #2
[1,2,4]를 이용해서 7을 만들 수 있습니다.
[1,4,6]을 이용해서 11을 만들 수 있습니다.
[2,4,7]을 이용해서 13을 만들 수 있습니다.
[4,6,7]을 이용해서 17을 만들 수 있습니다.*/
public class MakeSosu {
	static int cnt=0;  
	public static void main(String[] args) {

		//int [] nums = {1,2,3,4};
		int [] nums2 = {1,2,7,6,4};
		//int length = 0;
		
		//4가지 중 3가지를 추출한다. 123, 124, 234
		//5가지 중 3가지를 추출한다. 
		//123, 124, 125,134,135,145, 234, 235 ,245, 345
		/*nCr = n! / (n-r)! r!
	    5C3 = 5! / 2! 3! = 10개
	    5*4*3*2*1 / 2*1*3*2*1
	    
	    1, 2 - 3,4,5
	    1, 3 - 4,5
	    1, 4 - 5
	    
	    2, 3 - 4,5
	    2, 4 - 5
	    
	    3, 4 - 5*/
		//나올 수 있는 경우의 수(조합 공식)
		//length = fact(nums2.length) / (fact(nums2.length-3)*fact(3));
	    
		int sum = 0;
		
		
	    for (int i = 0; i < nums2.length; i++) {
	    	for (int j = i+1; j < nums2.length; j++) {
	    		for (int k = nums2.length-1; j < k; k--) {
	    			//System.out.println(i+""+j+""+k);
	    			System.out.println(nums2[i] + nums2[j] + nums2[k]);
	    			sum = nums2[i] + nums2[j] + nums2[k];
	    			
	    			sosu(sum);
				}
			}
		}
	    
	    System.out.println("CNT  : "+ cnt);
	}
	
	
	//팩토리얼 함수
	/*
	 * public static int fact(int n) { if (n <= 1) return n; else return fact(n-1) *
	 * n; }
	 */

	//소수 판별 함수
	public static void sosu(int sum) {
		boolean sosuCheck = true;
		for(int i = 2; i < sum; i++) {
			if(sum % i == 0) {
				sosuCheck = false;
				break;
			}else {
				sosuCheck = true;
			}
		}
		
		if(sosuCheck) {
			cnt++;
		}
		
	}

}


```
