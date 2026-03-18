# Odd_Numer_Finder
You write a number and it will tell you if its an odd or even number
This is a Prime Number Checker
This program determines whether a given positive integer is a prime number or not. It reads an integer from the user and prints "prime" if the number is prime, otherwise "not prime".

Input Description
A single integer n
Constraints:
2 ≤ 𝑛 ≤ 2,000,000

Output Description
"prime" → if the number is prime
"not prime" → if the number is not prime

Algorithm Explanation
A number is considered prime if:
*It is greater than or equal to 2
*It has no divisors other than 1 and itself
Steps:
1. If the number is less than 2 → return false
2. Loop from 2 to √n (square root of n)
3. If any number divides n evenly → return false
4. If no divisors are found → return true

import java.util.Scanner;
- Imports the Scanner class
- Used to read user input from the console

public class NumeroPrimo
- Defines the main class of the program
- In Java, every program must have at least one class

public static void main(String[] args)
- Entry point of the program
- The JVM (Java Virtual Machine) starts execution here

Scanner sc = new Scanner(System.in);
- Creates a Scanner object
- System.in allows reading input from the keyboard

int n = sc.nextInt();
-Reads an integer value entered by the user
-Stores it in variable n

if (esPrimo(n))
- Calls the method esPrimo
-Evaluates whether the number is prime

System.out.println("prime");
- Prints "prime" if the number is prime
System.out.println("not prime");
- Prints "not prime" if the number is not prime

sc.close();
- Closes the Scanner object
- Prevents resource leaks

Method: esPrimo(int n)
public static boolean esPrimo(int n)
-Declares a method that returns a boolean (true or false)
-static allows it to be called without creating an object

if (n < 2)
-Checks if the number is less than 2
-Returns false because primes start at 2

for (int i = 2; i <= Math.sqrt(n); i++)
-Loops from 2 up to the square root of n
-Optimization: reduces the number of iterations

if (n % i == 0)
-Checks if n is divisible by i
-% is the modulus operator (remainder)

return false;
-If a divisor is found, the number is not prime

return true;
-If no divisors are found, the number is prime

Time Complexity
- O(√n) → Efficient for values up to 2,000,000
