# Documentation- Fibonacci function in Recursive and Iterative fashion. 

import java.util.Scanner;

public class Fibonacci {
	
	//Recursive method
	int fibRecursive(int x) {
		
		//If x is in the 0th or 1st place return n
		if (x <= 1)
			return x ;
		return fibRecursive(x - 1) + fibRecursive(x - 2);
	}
	
	//Iterative method
	int fibIterative(int n) {
		if (n <= 1)
			return n;

		int fib = 1, prevFib = 1;
		for (int i = 2; i < n; i++) {
			int temp = fib;
			fib += prevFib;
			prevFib = temp;
		}
	return fib;
}
	//Print out Time
	public static void showTime() {
		
		long startTime = System.nanoTime();
		System.out.println("t = " + (System.nanoTime() - startTime) + " nanosecs.");
	}
	
	public static void main(String[] args1) {
		Fibonacci fib = new Fibonacci();
		Scanner input = new Scanner(System.in);
		System.out.println("Enter a value: ");
	       
		int n = input.nextInt();
		System.out.println("Iterative version:");
		
		long startTime = System.nanoTime();
		System.out.println(fib.fibIterative(n));
		System.out.println("time = " + (System.nanoTime() - startTime) + " nanosecs.");
		
		System.out.println("Recursive version:");
		startTime = System.nanoTime();
		System.out.println(fib.fibRecursive(n));
		System.out.println("time = " + (System.nanoTime() - startTime) + " nanosecs.");
}
	private char[] fibIterative1(int n) {
		return null;
	}
	private static int fibRecursive1(int i) {
		return 0;
	}
}
