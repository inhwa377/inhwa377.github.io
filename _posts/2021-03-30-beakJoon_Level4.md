---
title: 백준 단계별 4 - while문 - 10952 / 10951 / 1110
categories: [beakJoon]
comments: true
---

## 10952번 A+B-5

![A+B-5](https://user-images.githubusercontent.com/75457050/112956632-a29af000-917b-11eb-9159-c205568d1838.JPG)

<br><br>

```java
public class A_Plus_B_5 {
	public static void main(String[] args) {
		String[] input;
		String end1 = "0";
		String end2 = "0";
		int A;
		int B;
		
		BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
		BufferedWriter bw = new BufferedWriter(new OutputStreamWriter(System.out));
		
		try {
			
			while(true) {
				input = br.readLine().split(" ");
				A = Integer.parseInt(input[0]);
				B = Integer.parseInt(input[1]);

				if(input[0].equals(end1) && input[1].equals(end2)) {
					break;
				}
				
				bw.write(String.valueOf(A+B));
				bw.newLine();
			}
			
			bw.flush();
			bw.close();
			
		} catch (Exception e) {
			e.printStackTrace();
			System.out.println("에러 = " + e.getMessage());
		}
	}
}
```
<br><br>

## 10951번 A+B-4

![A+B-4](https://user-images.githubusercontent.com/75457050/112956649-a595e080-917b-11eb-97ca-86ae1bfd74a4.JPG)

<br><br>

```java
public class A_Plus_B_4 {
	public static void main(String[] args) {
		int A;
		int B;
		
		Scanner sc = new Scanner(System.in);
		
		while(sc.hasNextInt()) {
			A = sc.nextInt();
			B = sc.nextInt();
			
			System.out.println(A+B);
		}
	}
}

```
<br><br>


## 1110번 더하기 사이클

![더하기 사이클](https://user-images.githubusercontent.com/75457050/112956665-a890d100-917b-11eb-80bc-1379e45369e2.JPG)

<br><br>

```java
public class PlusCycle {
	public static void main(String[] args) {
		
		BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
		BufferedWriter bw = new BufferedWriter(new OutputStreamWriter(System.out));
		
		int N; //시작하는 숫자
		int count = 0; //횟수 
		int copy; //더한 새로운 숫자

		try {
			N = Integer.parseInt(br.readLine());
			copy = N;
			
			do {
				N = ((N%10)*10) + ((N/10 + N%10)%10);
				count++;

			} while (N != copy);
			
				bw.write(String.valueOf(count));
				bw.flush();
				bw.close();
				
		} catch (Exception e) {
			e.printStackTrace();
			System.out.println("에러 = " + e.getMessage());
		}
	}
```
<br><br>


