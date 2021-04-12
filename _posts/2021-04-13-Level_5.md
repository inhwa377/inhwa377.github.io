---
title: 백준 단계별 5 - 1차원 배열 - 10818 / 2562 / 2577 / 3052
categories: [beakJoon]
comments: true
---

## 10818번 최소, 최대

![최소최대](https://user-images.githubusercontent.com/75457050/114446390-250bc100-9c0c-11eb-9c60-cdc2d404daa1.JPG)

<br><br>

```java
public class min_max {
	public static void main(String[] args) {
		
		BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
		BufferedWriter bw = new BufferedWriter(new OutputStreamWriter(System.out));
		
		try {
			int N = Integer.parseInt(br.readLine());
			StringTokenizer st = new StringTokenizer(br.readLine(), " ");
			
			int index = 0;
			int[] arr = new int[N];
			
			while(st.hasMoreTokens()) {
				arr[index] = Integer.parseInt(st.nextToken());
				index++;
			}
			
			Arrays.sort(arr);
			bw.write(arr[0] + " " + arr[N - 1]);
			bw.flush();
			bw.close();
			
		} catch (Exception e) {
			e.printStackTrace();
			System.out.println(e.getMessage());
		}
	}
}
```
<br><br>

## 2562번 최댓값

![최댓값](https://user-images.githubusercontent.com/75457050/114446529-4c628e00-9c0c-11eb-991a-ff1d261b3c0a.JPG)

<br><br>

```java
public class max {

	public static void main(String[] args) {
		int[] arr = new int[9];
		
		BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
		BufferedWriter bw = new BufferedWriter(new OutputStreamWriter(System.out));
		
		try {
			for(int i=0; i<arr.length; i++) {
				arr[i] = Integer.parseInt(br.readLine());
			}
			
			int max = 0; //최댓값
			int index = 0; //최댓값의 n번째 번호
			int count = 0; //최댓값의 번호를 세기위한 카운트
			
			for(int value:arr) {
				count++;
				if(value > max) {
					max = value;
					index = count;
				}
			}
			
			bw.write(String.valueOf(max));
			bw.newLine();
			bw.write(String.valueOf(index));
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


## 숫자의 개수

![숫자의개수](https://user-images.githubusercontent.com/75457050/114446597-6308e500-9c0c-11eb-8f73-2f238c4f558e.JPG)

<br><br>

```java
public class countNum {
	public static void main(String[] args) {
		
		int[] arr = new int[10];
		
		BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
		BufferedWriter bw = new BufferedWriter(new OutputStreamWriter(System.out));
		
		try {

			int mul = Integer.parseInt(br.readLine()) * Integer.parseInt(br.readLine()) * Integer.parseInt(br.readLine());
			
			String str = String.valueOf(mul);
			
			for(int i=0; i<str.length(); i++) {
				arr[(str.charAt(i) - 48)]++;
			}
			
			for(int j : arr) {
				bw.write(String.valueOf(j));
				bw.newLine();
				bw.flush();
			}
			
			bw.close();
			
		}catch (Exception e) {
			e.printStackTrace();
			System.out.println(e.getMessage());
		}
	}
}
```
<br><br>

## 3052번 나머지

![나머지](https://user-images.githubusercontent.com/75457050/114446702-7f0c8680-9c0c-11eb-83c6-cfeea244c08e.JPG)
<br><br>

```java
public class leftover {
	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		HashSet<Integer> hs = new HashSet<Integer>();
		
		for(int i=0; i<10; i++) {
			hs.add(sc.nextInt() % 42);
		}
		
		sc.close();
		System.out.print(hs.size());		
	}
}
```
<br><br>
