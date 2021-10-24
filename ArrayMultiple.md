# x만큼 간격이 있는 n개의 숫자

숫자가 커짐에 따라 int*int는 담을 수 있는 범위의 한계가 있다.
그러므로 long으로 강제 형변환이 필요하다. 

```java
import java.util.Arrays;

//x만큼 간격이 있는 n개의 숫자
public class ArrayMultiple {

	public static void main(String[] args) {
	
	solution(5,2);
		
	System.out.println(Arrays.toString(solution(10000000,1000)));
		    
	}
	
	public static long[] solution(int x, int n) { 
	       long[] answer = new long[n]; // 배열 생성
	       
	       for (int i = 1; i < n+1; i++) {
	    	   answer[i-1] = (long)x * i; 
	    	   //숫자가 커짐에 따라 int*int는 담을 수 있는 범위가 한계가 있다. 
	    	   //그러므로 long으로 강제 형변환이 필요하다.
	       }
	       
	       return answer;
	}

}

```

