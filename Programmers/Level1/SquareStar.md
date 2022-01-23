# 프로그래머스 직사각형 별찍기 

```java
import java.util.Scanner;

//직사각형 별찍기
public class SquareStar {

	public static void main(String[] args) {
     Scanner sc = new Scanner(System.in);
     int a = sc.nextInt();
     int b = sc.nextInt();

     for (int j = 0; j < b; j++) {
        if(j!=0){
            System.out.println();    
        }
        for (int i = 0; i < a; i++) {
            System.out.print('*');
        }
     }
	}
}
```

