
# 핸드폰 번호 가리기

```java
//전화번호 뒤의 4자리를 제외한 나머지는 *표처리
//주어지는 값의 자릿수는 4~20자리 범위인 경우
public class HidePhone {

	public static void main(String[] args) {
		
		String str = "01012349946";
		
		String lastPhoneNum = str.substring(str.length()-4, str.length());
		
		String star="";
		for (int i = 0; i < str.length()-4; i++) {
			star+="*";
		}
		
		String result = star + lastPhoneNum;
		System.out.println("result : " + result);
	}

}
```
