---
title: 백준 단계별 2 - if문 - 1330 / 9498 / 2753 / 14681 / 2884
categories: [beakJoon]
comments: true
---

## 1330번 두 수 비교하기

![두 수 비교하기](https://user-images.githubusercontent.com/75457050/112943388-6318d780-916c-11eb-8efc-e8191328f4ef.JPG)
<br><br>

```java
public class CompareAB {
	public static void main(String[] args) {
		int A;
		int B;
		
		Scanner sc = new Scanner(System.in);
		
		A = sc.nextInt();
		B = sc.nextInt();
		
		if(A > B) {
			System.out.println(">");
		} 
		if(A < B) {
			System.out.println("<");
		} 
		if(A == B) {
			System.out.println("==");
		}
	}
}
```
<br><br>

## 9498번 시험 성적

![시험 성적](https://user-images.githubusercontent.com/75457050/112943408-66ac5e80-916c-11eb-96fc-4db7f0dec266.JPG)
<br><br>

```java
public class examScore {
	public static void main(String[] args) {
		int score;
		
		Scanner sc = new Scanner(System.in);
		
		score = sc.nextInt();
		
		if(90 <= score && score <= 100) {
			System.out.println("A");
		} else if(80 <= score && score <=89) {
			System.out.println("B");
		} else if(70 <= score && score <= 79) {
			System.out.println("C");
		} else if(60 <= score && score <= 69) {
			System.out.println("D");
		} else if(score <= 59) {
			System.out.println("F");
		}
	}
}
```
<br><br>

## 2753번 윤년

![윤년](https://user-images.githubusercontent.com/75457050/112943424-6a3fe580-916c-11eb-9ae8-ec2b876784fc.JPG)
<br><br>

```java
public class leapYear {
	public static void main(String[] args) {
		int year;
		
		Scanner sc = new Scanner(System.in);
		
		year = sc.nextInt();

		if((year%4) == 0 && ((year%100) != 0 || (year%400) == 0)) {
			System.out.println("1");
		} else {
			System.out.println("0");
		}
	}
}
```
<br><br>

## 14681번 사분면 고르기

![사분면 고르기](https://user-images.githubusercontent.com/75457050/112943443-6d3ad600-916c-11eb-8601-7bcea0b18ab1.JPG)
<br><br>

```java
public class quadrant {
	public static void main(String[] args) {
		int X;
		int Y;
		
		Scanner sc = new Scanner(System.in);
		
		X = sc.nextInt();
		Y = sc.nextInt();
		
		if(X > 0 && Y > 0) {
			System.out.println("1");
		} else if (X < 0 && Y > 0) {
			System.out.println("2");
		} else if (X < 0 && Y < 0) {
			System.out.println("3");
		} else if (X > 0 && Y < 0) {
			System.out.println("4");
		}
	}
}
```
<br><br>

## 2884번 알람 시계

![알람 시계](https://user-images.githubusercontent.com/75457050/112943455-7035c680-916c-11eb-809b-949da61e7ff6.JPG)
<br><br>

```java
public class alarmClock {
	public static void main(String[] args) {
		int H;
		int M;
		int MM;
		
		Scanner sc = new Scanner(System.in);
		
		H = sc.nextInt();
		M = sc.nextInt();
		MM = M - 45;
		
		if((0 <= H && H <= 23) || (0 <= M && M <= 59)) {
			if(MM < 0) {
				H = H - 1;
				M = MM + 60;
				
				if(H < 0) {
					H += 24;
				}
				
				System.out.println(H);
				System.out.println(M);
				
			} else if(MM >= 0) {
				System.out.println(H);
				System.out.println(MM);
			}
		}
	}
}
```
<br><br>
