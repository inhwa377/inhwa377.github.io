---
title: 백준 단계별 3 - for문 - 2739 / 10950 / 8393 / 15552 / 2741 / 2742 / 11021 / 11022 / 2438 / 2439 / 10871
categories: [beakJoon]
comments: true
---

## 2739번 구구단

![구구단](https://user-images.githubusercontent.com/75457050/112951616-8052a380-9176-11eb-9068-efc79d5b061f.JPG)

<br><br>

```java
public class timesTable {
	public static void main(String[] args) {
		int N;
		
		Scanner sc = new Scanner(System.in);
		
		N = sc.nextInt();
		
		for(int i = 1; i <= 9; i++) {
			System.out.println( N + " * " + i + " = "  + (N*i) );
		}
	}
}
```
<br><br>

## 10950번 A+B-3

![A+B-3](https://user-images.githubusercontent.com/75457050/112952076-0f5fbb80-9177-11eb-9523-c53dfe16c20f.JPG)

<br><br>

```java
public class A_Plus_B_3 {
	public static void main(String[] args) {
		int A;
		int B;
		int C;
		
		Scanner sc = new Scanner(System.in);
		
		C = sc.nextInt();
		
		for(int i=0; i < C; i++) {
			A = sc.nextInt();
			B = sc.nextInt();
			System.out.println(A+B);
		}
	}
}
```
<br><br>

## 8393번 합

![합](https://user-images.githubusercontent.com/75457050/112952106-1981ba00-9177-11eb-9fca-ff9f5800a28b.JPG)

<br><br>

```java
public class sum {
	public static void main(String[] args) {
		int n;
		int i;
		int j=0;
		
		Scanner sc = new Scanner(System.in);
		
		n = sc.nextInt();
		
		for(i=1; i<=n; i++) {
			j = j+i;
		}
		System.out.println(j);
	}
}
```
<br><br>

## 15552번 빠른 A+B

![빠른 A+B](https://user-images.githubusercontent.com/75457050/112952125-1edf0480-9177-11eb-8a3d-6beb942d0210.JPG)

<br><br>

```java
public class fast_A_Plus_B {

	public static void main(String[] args) {
		int A;
		int B;
		int N;
		String[] A_B;
		
		BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
		BufferedWriter bw = new BufferedWriter(new OutputStreamWriter(System.out));
		
		try {
			N = Integer.parseInt(br.readLine());
			
			for(int i=0; i < N; i++) {
				A_B = br.readLine().split(" ");
				A = Integer.parseInt(A_B[0]);
				B = Integer.parseInt(A_B[1]);
				
				bw.write(String.valueOf(A+B));
				bw.newLine();
			}
			
			bw.flush();
			bw.close();
			
		} catch (Exception e) {
			e.printStackTrace();
			System.out.println("에러 = " +e.getMessage());
		}
	}
}
```
<br><br>

## 2741번 N찍기

![N찍기](https://user-images.githubusercontent.com/75457050/112952141-24d4e580-9177-11eb-8fd7-8acd6052795b.JPG)

<br><br>

```java
public class outputN {
	public static void main(String[] args) {
		int N;
		
		BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
		BufferedWriter bw = new BufferedWriter(new OutputStreamWriter(System.out));
		
		try {
			N = Integer.parseInt(br.readLine());
			
			for(int i=1; i <= N; i++) {
				bw.write(String.valueOf(i));
				bw.newLine();
				bw.flush();
			}
			
			bw.close();
			
		} catch (Exception e) {
			e.printStackTrace();
			System.out.println("에러 = " + e.getMessage());
		}
	}
}
```
<br><br>

## 2742번 기찍N

![기찍 N](https://user-images.githubusercontent.com/75457050/112952175-2d2d2080-9177-11eb-83de-dae9c9aa231e.JPG)

<br><br>

```java
public class backwards_OutputN {
	public static void main(String[] args) {
		int N;
		
		BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
		BufferedWriter bw = new BufferedWriter(new OutputStreamWriter(System.out));
		
		try {
			
			N = Integer.parseInt(br.readLine());
			
			for(int i=N; i>0; i--) {
				bw.write(String.valueOf(i));
				bw.flush();
				bw.newLine();
			}
			
			bw.close();
		} catch (Exception e) {
			e.printStackTrace();
			System.out.println("에러 = " + e.getMessage());
		}
	}
}
```
<br><br>

## 11021번 A+B-7

![A+B-7](https://user-images.githubusercontent.com/75457050/112952187-2f8f7a80-9177-11eb-8f30-b158d38a14f9.JPG)

<br><br>

```java
public class A_Plus_B_7 {
	public static void main(String[] args) {
		int A;
		int B;
		String[] AB;
		int N;
		
		BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
		BufferedWriter bw = new BufferedWriter(new OutputStreamWriter(System.out));
			
		try {
			
			N = Integer.parseInt(br.readLine());
			
			for(int i=1; i<=N; i++) {
				AB = br.readLine().split(" ");
				
				A = Integer.parseInt(AB[0]);
				B = Integer.parseInt(AB[1]);
				
				bw.write("Case #" + i + ": " + String.valueOf(A+B));
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

## 11022번 A+B-8

![A+B-8](https://user-images.githubusercontent.com/75457050/112952197-31f1d480-9177-11eb-8b1d-4d23807c49d5.JPG)

<br><br>

```java
public class A_Plus_B_8 {
	public static void main(String[] args) {
		int A;
		int B;
		int N;
		String[] AB;
		
		BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
		BufferedWriter bw = new BufferedWriter(new OutputStreamWriter(System.out));
		
		try {
			
			N = Integer.parseInt(br.readLine());
			
			for(int i=1; i<=N; i++) {
				AB = br.readLine().split(" ");
				A = Integer.parseInt(AB[0]);
				B = Integer.parseInt(AB[1]);
				
				bw.write("Case #" + i + ": " + A + " + " + B + " = " +String.valueOf(A+B));
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

## 2438번 별찍기-1

![별찍기-1](https://user-images.githubusercontent.com/75457050/112952211-361df200-9177-11eb-8da8-70e0f5333a9b.JPG)

<br><br>

```java
public class star1 {
	public static void main(String[] args) {
		String star = "*";
		int n;
		
		BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
		BufferedWriter bw = new BufferedWriter(new OutputStreamWriter(System.out));
		
		try {
			n = Integer.parseInt(br.readLine());
			
			for(int i=1; i<=n; i++) {
				for(int j=0; j<i; j++) {
					bw.write(star);
				}
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

## 2439번 별찍기-2

![별찍기-2](https://user-images.githubusercontent.com/75457050/112952218-38804c00-9177-11eb-86c8-2a5ef1737f25.JPG)

<br><br>

```java
public class star2 {
	public static void main(String[] args) {
		String star = "*";
		int n;
		
		BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
		BufferedWriter bw = new BufferedWriter(new OutputStreamWriter(System.out));
		
		try {
			
			n = Integer.parseInt(br.readLine());
			
			for(int i=1; i<=n; i++) {
				for(int j=n; j>i; j--) {
					bw.write(" ");
				}
				for(int k=0; k<i; k++) {
					bw.write(star);
				}
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

## 10871번 X보다 작은 수

![X보다 작은 수](https://user-images.githubusercontent.com/75457050/112952235-3b7b3c80-9177-11eb-8ad3-f49c6c277a34.JPG)

<br><br>

```java
public class less_than_X {
	public static void main(String[] args) {
		String[] input = null;
		int N; //수열A의 정수 갯수
		int X;
		String[] A = null;
		
		BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
		BufferedWriter bw = new BufferedWriter(new OutputStreamWriter(System.out));
		
		try {
			input = br.readLine().split(" ");
			N = Integer.parseInt(input[0]);
			X = Integer.parseInt(input[1]);
			A = br.readLine().split(" "); 
			
			for(int i=0; i<N; i++) {
				if(Integer.parseInt(A[i]) < X) {
					bw.write(A[i]);
					bw.write(" ");
				}
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
