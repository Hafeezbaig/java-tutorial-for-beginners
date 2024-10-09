# Missing Info in Lectures From Github Repo

## Section 3: Introduction to Java Programming with Jshell using Multiplication Table

### Step 10 - Printing output to console with Java - Puzzles:

### Whitespace is ignored by the compiler when used around numeric expressions.

```java
	jshell> System.out.println(24 * 60 * 60)
	86400
	jshell> System.out.println(24    *    60    *    60)
	86400
	jshell>
```
---
### Step 14 - Introduction to Variables in Java - Exercises and Puzzles

### Let's consider another example:

```java
	jshell> int number = "Hello World"
	| Error:
	| incompatible types: java.lang.String cannot be converted to int
	| int number = "Hello World"
	|_____________^--------------^
	jshell>
```

- number is an int variable, and we are trying to store a String value "Hello World". Not allowed.

---

### Step 16 - How are variables stored in memory?

### An assignment to a constant literal is not allowed.

```java
	jshell> 20 = var
	| Error:
	| unexpected type
	| required : variable
	| found : value
	| 20 = var
	| ^^

	jshell>
```

---

### Additional Coding Exercises:

### Programming Exercise 1: Multiplication Table for Any Number

Objective: Allow the user to input any number and display its multiplication table from 1 to 10.

#### Instructions:

- Write a program that prompts the user to enter a number.
- Use a loop to display the multiplication table for the entered number from 1 to 10.
- Format the output using System.out.printf() for clean display.

#### Sample Code:

```java
import java.util.Scanner;

public class MultiplicationTable {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        // Prompt user for input
        System.out.print("Enter a number to display its multiplication table: ");
        int number = scanner.nextInt();
        
        // Display multiplication table for the entered number
        System.out.println("Multiplication Table for " + number + ":");
        for (int i = 1; i <= 10; i++) {
            System.out.printf("%d * %d = %d%n", number, i, number * i);
        }
        
        scanner.close();
    }
}
```

#### Expected Output:

```java
Enter a number to display its multiplication table: 7
Multiplication Table for 7:
7 * 1 = 7
7 * 2 = 14
7 * 3 = 21
7 * 4 = 28
7 * 5 = 35
7 * 6 = 42
7 * 7 = 49
7 * 8 = 56
7 * 9 = 63
7 * 10 = 70
```

---

### Programming Exercise 2: Even Numbers Table

Objective: Generate and print the multiplication table for all even numbers between 2 and 10.

#### Instructions:

- Write a program that generates the multiplication table for all even numbers between 2 and 10.
- Use nested loops to calculate and display each table.
- Format the output using System.out.printf() for clean display.

#### Sample Code:

```java
public class EvenMultiplicationTable {
    public static void main(String[] args) {
        System.out.println("Multiplication Tables for Even Numbers (2 to 10):");
        
        // Loop through even numbers from 2 to 10
        for (int number = 2; number <= 10; number += 2) {
            System.out.printf("Multiplication Table for %d:%n", number);
            for (int i = 1; i <= 10; i++) {
                System.out.printf("%d * %d = %d%n", number, i, number * i);
            }
            System.out.println();  // Print a blank line for better readability
        }
    }
}
```

#### Expected Output:

```java
Multiplication Tables for Even Numbers (2 to 10):
Multiplication Table for 2:
2 * 1 = 2
2 * 2 = 4
2 * 3 = 6
2 * 4 = 8
2 * 5 = 10
2 * 6 = 12
2 * 7 = 14
2 * 8 = 16
2 * 9 = 18
2 * 10 = 20

Multiplication Table for 4:
4 * 1 = 4
4 * 2 = 8
4 * 3 = 12
4 * 4 = 16
4 * 5 = 20
4 * 6 = 24
4 * 7 = 28
4 * 8 = 32
4 * 9 = 36
4 * 10 = 40

... (and so on for 6, 8, and 10)
```

---

## Section 4: Introduction to Java Method with Multiplication Table

### Step 04 - Introduction to Java Methods - Arguments and Parameters

### Snippet-5 : Parameter type mismatch

- Java is a strongly typed language, with strict rules laid out for type compatibility. We saw that with variables, and how they play out with expressions and assignments.

- The same type compatibility rules are enforced by the compiler, when it needs to match the arguments from method calls with method definition.

```java
	jshell> sayHelloWorld("value")
	| Error:
	| incompatible types: java.lang.String cannot be converted to int
	| sayHelloWorld("value")
	|               ^-----^
	jshell> sayHelloWorld(4.5)
	| Error:
	| incompatible types: possibly lossy conversion from double to int
	| sayHelloWorld(4.5)
	|               ^-^
	jshell>
```

---

### Step 06 - Introduction to Java Method Arguments - Puzzles and Tips

> **Note**: Step-6 is not present in GitHub repo.

---

## Section 12: Conditionals in Java Programming

### Step 09: Comparing The if Family, And switch

Let's compare and contrast these two approaches, to gain some experience on how to choose a conditional.

First comes an example using the if-else if-else statement.

#### Snippet-01 : Formatted Output Using if

#### OperatorChoiceRunner.java

```java
	package com.in28minutes.ifstatement.examples;

	public class OperatorChoiceRunner {
		public static void main(String[] args) {
			OperatorChoice opChoice = new OperatorChoice(5, 2, 1);
			opChoice.operate();
		}
	}
```
#### OperatorChoice.java

```java
	package com.in28minutes.ifstatement.examples;

	public class OperatorChoice {
		private int number1;
		private int number2;
		private int choice;
		
		public OperatorChoice(int number1, int number2, int choice) {
			this.number1 = number1;		
			this.number2= number2;
			this.choice = choice;
		}

		public void operate() {
			System.out.printf("number1 : %d", number1).println();
			System.out.printf("number2 : %d", number2).println();
			System.out.printf("choice : %d", choice).println();
			
			if(choice == 1) {
				System.out.printf("result : %d", number1 + number2).println();
			} else if(choice == 2) {
				System.out.printf("result : %d", number1 - number2).println();
			} else if(choice == 3) {
				System.out.printf("result : %d", number1 * number2).println();
			} else if(choice == 4) {
				System.out.printf("result : %d", number1 / number2).println();
			} else {
				System.out.println("Invalid Operation");
			}
		}
	}
```

#### Console Output

```java
number1 : 5

number2 : 2

choice : 1

result : 7
```

Next in line, is an example involving a switch.

#### Snippet-02 : Formatted Output Using switch

#### OperatorChoiceRunner.java

```java
	package com.in28minutes.ifstatement.examples;

	public class OperatorChoiceRunner {
		public static void main(String[] args) {
			OperatorChoice opChoice = new OperatorChoice(5, 2, 1);
			opChoice.operateUsingSwitch();
		}
	}
```

#### OperatorChoice.java

```java

	package com.in28minutes.ifstatement.examples;

	public class OperatorChoice {
		private int number1;
		private int number2;
		private int choice;

		public OperatorChoice(int number1, int number2, int choice) {
			this.number1 = number1;
			this.number2= number2;
			this.choice = choice;
		}

		public void operateUsingSwitch() {
			System.out.printf("number1 : %d", number1).println();
			System.out.printf("number2 : %d", number2).println();
			System.out.printf("choice : %d", choice).println();

			switch(choice) {
				case 1: System.out.printf("result : %d", number1 + number2).println(); 
					break;
				case 2: System.out.printf("result : %d", number1 - number2).println(); 
					break;
				case 3: System.out.printf("result : %d", number1 * number2).println(); 
					break;				
				case 4: System.out.printf("result : %d", number1 / number2).println(); 
					break;
				default: System.out.printf("result : %d", number1 + number2).println(); 
					break;
			}
		}
	}
```

#### Console Output

```java
number1 : 5

number2 : 2

choice : 1

result : 7
```

#### Summary

In this step, we:

- Observed that the same conditional code could be written using an if-family conditional, or the switch.

- Learned that an if family conditional is difficult to get wrong, as the rules for it are very strict. It can be used to evaluate only boolean conditions. But it is verbose, and often less readable.

- Came to know that a switch conditional can be used to check for only integer values. It is very compact, and very readable.

- However, the relative order of case clauses and default are not fixed, and the usage of break is optional. This can lead to subtle errors in your program.

---

## Section 14: Loops in Java Programming

### Step 02 - Java For Loop - Exercises Overview and First Exercise Prime Numbers

> **Note**: Step-2 is not present in GitHub repo.

### Step 03 - Java For Loop - Exercise - Sum Upto N Numbers and Sum of Divisors

> **Note**: Step-3 is not present in GitHub repo.

### Step 04 - Java For Loop - Exercise - Print a Number Triangle

> **Note**: Step-4 is not present in GitHub repo.

### Step 05 - While Loop in Java - An Introduction

> **Note**: Step-5 is not present in GitHub repo.

### Step 06 - While Loop - Exercises - Cubes and Squares upto limit

> **Note**: Step-6 is not present in GitHub repo.

### Step 07 - Do While Loop in Java - An Introduction

> **Note**: Step-7 is not present in GitHub repo.

### Step 08 - Do While Loop in Java - An Example - Cube while user enters positive numbers

> **Note**: Step-8 is not present in GitHub repo.

### Step 09 - Introduction to Break and Continue

> **Note**: Step-9 is not present in GitHub repo.

### Step 10 - Selecting Loop in Java - For vs While vs Do While

> **Note**: Step-10 is not present in GitHub repo.

---

## Section 16: Reference Types in Java Programming

### Step 14 - Java Reference Types - Conclusion

> **Note**: Step-14 is not present in GitHub repo.

---
