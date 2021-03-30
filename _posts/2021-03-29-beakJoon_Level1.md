---
title: 백준 단계별 1 - 입출력과 사칙연산 - 2557 / 10718 / 10171 / 10172 / 1000 / 1001 / 10998 / 1008 / 10869 / 10430 / 2588
categories: [beakJoon]
comments: true
---


## 2557번 Hello World


![HelloWorld](https://user-images.githubusercontent.com/75457050/112940532-39f64800-9168-11eb-8b59-98917de7997f.JPG)
<br><br>

```java

public class helloWorld {
	public static void main(String[] args) {
		System.out.println("Hello World!");
		System.exit(0);
	}
} 
```
<br>
<br>

## 10718번 We love kriii

![We love kriii](https://user-images.githubusercontent.com/75457050/112940549-424e8300-9168-11eb-946b-df47422b6e3d.JPG)
<br><br>

```java
public class weLoveKriii {
	public static void main(String[] args) {
		String a = "강한친구 대한육군";
		
		System.out.println(a);
		System.out.println(a);
	}
}
```
<br><br>

## 10171번 고양이

![고양이](https://user-images.githubusercontent.com/75457050/112940570-48446400-9168-11eb-816f-0edefbc1e3ba.JPG)
<br><br>

```
public class cat {
	public static void main(String[] args) {
		System.out.println("\\    /\\");
		System.out.println(" )  ( ')");
		System.out.println("(  /  )");
		System.out.println(" \\(__)|");
	}
}
```
<br><br>

## 10172번 개

![개](https://user-images.githubusercontent.com/75457050/112940576-4c708180-9168-11eb-9861-830e704a2d02.JPG)
<br><br>

```
public class dog {
	public static void main(String[] args) {
		System.out.println("|\\_/|");
		System.out.println("|q p|   /}");
		System.out.println("( 0 )\"\"\"\\");
		System.out.println("|\"^\"`    |");
		System.out.println("||_/=\\\\__|");
	}
}
```
<br><br>

## 1000번 A+B

![A+B](https://user-images.githubusercontent.com/75457050/112941044-f6500e00-9168-11eb-9328-58bb8a38e6d8.JPG)
<br><br>

```
public class A_Plus_B {
	public static void main(String[] args) {
		int A;
		int B;
		
		Scanner sc = new Scanner(System.in);
		
		A = sc.nextInt();
		B = sc.nextInt();
		
		System.out.println(A+B);		
	}
}
```
<br><br>

## 1001번 A-B

![A-B](https://user-images.githubusercontent.com/75457050/112941184-21d2f880-9169-11eb-9e01-dd667ea2bdd6.JPG)
<br><br>

```
public class A_minus_B {
	public static void main(String[] args) {
		int A;
		int B;
		
		Scanner sc = new Scanner(System.in);
		
		A = sc.nextInt();
		B = sc.nextInt();
		
		System.out.println(A-B);
	}
}
```
<br><br>

## 10998번 AxB

![AxB](https://user-images.githubusercontent.com/75457050/112941289-4b8c1f80-9169-11eb-8b89-3fae43415043.JPG)
<br><br>

```
public class A_multiply_B {

	public static void main(String[] args) {
		int A;
		int B;
		
		Scanner sc = new Scanner(System.in);
		
		A = sc.nextInt();
		B = sc.nextInt();
		
		System.out.println(A*B);

	}

}
```
<br><br>

## 1008번 A÷B

![AdivB](https://user-images.githubusercontent.com/75457050/112941541-b6d5f180-9169-11eb-8b0d-67975ad203e2.JPG)
<br><br>

```
public class A_division_B {
	public static void main(String[] args) {
		int A;
		int B;
		
		Scanner sc = new Scanner(System.in);
		
		A = sc.nextInt();
		B = sc.nextInt();
		
		System.out.println((double)A / (double)B);
	}
}

```
<br><br>

## 10869번 사칙연산

![사칙연산](https://user-images.githubusercontent.com/75457050/112941612-dd942800-9169-11eb-9577-993d4392fc75.JPG)
<br><br>

```
public class fourRuleCalculations {
	public static void main(String[] args) {
		int A;
		int B;
		
		Scanner sc = new Scanner(System.in);
		
		A = sc.nextInt();
		B = sc.nextInt();
		
		System.out.println(A+B);
		System.out.println(A-B);
		System.out.println(A*B);
		System.out.println(A/B);
		System.out.println(A%B);
	}
}
```
<br><br>

## 10430번 나머지

![나머지](https://user-images.githubusercontent.com/75457050/112941687-f997c980-9169-11eb-9cff-78a5c13e4869.JPG)
<br><br>

```
public class Remainder {
	public static void main(String[] args) {
		int A;
		int B;
		int C;
		
		Scanner sc = new Scanner(System.in);
		
		A = sc.nextInt();
		B = sc.nextInt();
		C = sc.nextInt();
		
		System.out.println((A+B)%C);
		System.out.println(((A%C) + (B%C))%C);
		System.out.println((A*B)%C);
		System.out.println(((A%C) * (B%C))%C);
	}
}
```
<br><br>


## 2588번 곱셈

![곱셈](https://user-images.githubusercontent.com/75457050/112941780-1c29e280-916a-11eb-8175-44c4dcebac5e.JPG)
<br><br>

```
public class multiply {
	public static void main(String[] args) {
		int A;
		int B;
		int sum;
		
		Scanner sc = new Scanner(System.in);
		
		A = sc.nextInt();
		B = sc.nextInt();
		sum = A*B;
		
		System.out.println(A * (B%10));
		System.out.println(A * ((B/10)%10));
		System.out.println(A * ((B/100)%10));
		System.out.println(sum);
	}
}
```
<br><br>
