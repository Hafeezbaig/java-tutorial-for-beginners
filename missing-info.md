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

### Additional Coding Exercises:

### Exercise 1: Multiplication Table Generator

**Objective**: Create a method that prints the multiplication table for any number, up to a specified range.

**Explanation**:
In this exercise, you’ll write a method that accepts two arguments:

`number`: The number for which the multiplication table is to be printed.

`range`: The number of rows in the multiplication table (i.e., how far the table goes).

For example, calling `generateMultiplicationTable(7, 12);` would print the multiplication table of 7 up to 12.

#### Code:

```java
public class MultiplicationTable {
    public static void generateMultiplicationTable(int number, int range) {
        for (int i = 1; i <= range; i++) {
            System.out.printf("%d * %d = %d%n", number, i, number * i);
        }
    }

    public static void main(String[] args) {
        generateMultiplicationTable(7, 12);  // Example: prints multiplication table of 7 up to 12
    }
}
```

#### Output:

```java
7 * 1 = 7
7 * 2 = 14
7 * 3 = 21
...
7 * 12 = 84
```

This exercise tests your ability to work with loops, method arguments, and formatted output.

---

### Exercise 2: Reusable Print Statements

**Objective**: Create a method that prints a custom message a specific number of times.

**Explanation**:
In this exercise, you’ll write a method that takes two arguments:

`message`: A string message to print.

`times`: The number of times to print the message.

This allows you to reuse the method to print any message, as many times as desired.

#### Code:

```java
public class PrintMessageExample {
    // Method to print a custom message a specific number of times
    public static void printCustomMessage(String message, int times) {
        for (int i = 1; i <= times; i++) {
            System.out.println(message);
        }
    }

    public static void main(String[] args) {
        // Example usage of the method
        printCustomMessage("Java is fun!", 5);  // Prints the message 5 times
    }
}
```

#### Output:

```java
Java is fun!
Java is fun!
Java is fun!
Java is fun!
Java is fun!
```

This exercise reinforces how to use method arguments to allow for flexibility in method behavior, as well as loop control for repeated tasks.

---

## Section 5: Introduction to Java Platform

### Additional Coding Exercises:


### **Exercise 1: Exploring Java Platform Components**

**Objective**: Understanding the role of the JVM, JRE, and JDK through a practical scenario.

#### Scenario:
You have written a simple Java program `Greeting.java` that prints "Hello, World!" to the console. You want to share this program with two different friends:

1. **Friend A** only has the JRE installed.

2. **Friend B** has the JDK installed.

**Tasks**:

1. Explain what each friend needs to do to run your program.

2. For **Friend A**, you should provide the compiled bytecode (`Greeting.class`), explain why this is necessary, and describe how they can run the program with the JRE.

3. For **Friend B**, explain the steps they need to follow, starting with the source file (`Greeting.java`), and show how they can compile and run the program using the JDK.

#### Sample Code for `Greeting.java`:

```java
public class Greeting {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}
```

#### Expected Outcome:
- Learners should be able to describe the differences between the JRE and JDK and how each is used in different contexts (running bytecode vs. compiling and running source code).

- They should know how to compile a Java program with the JDK using `javac` and run it using `java`, and explain why the JRE alone is sufficient to run pre-compiled bytecode.

---

### **Exercise 2: Creating and Compiling a Class with a Method**

**Objective**: Writing and compiling Java code outside of JShell, understanding the use of the `javac` and `java` commands.

#### Tasks:

1. Write a Java class named `Car` in a file called `Car.java`. The class should have the following features:

    - A method `start()` that prints `"The car has started."`.

    - A method `stop()` that prints `"The car has stopped."`.

2. Add a `main` method to the class, where you create an instance of `Car` and call both `start()` and `stop()`.

3. Compile your `Car.java` file using the `javac` command.

4. Run the compiled class using the `java` command.

#### Code for `Car.java`:

```java
public class Car {
    void start() {
        System.out.println("The car has started.");
    }
    
    void stop() {
        System.out.println("The car has stopped.");
    }

    public static void main(String[] args) {
        Car myCar = new Car();
        myCar.start();
        myCar.stop();
    }
}
```

#### Expected Outcome:

- The learners will write a basic Java class with methods and a `main` method to execute it.

- They will compile the code using `javac` and understand how the `.class` file is generated.

- They will run the compiled bytecode using `java Car`, reinforcing the steps of compiling and running a Java program outside of JShell.

---

## Section 6: Introduction to Eclipse - First Java Programming Project

### Additional Coding Exercises:

### **Exercise 1: Creating and Debugging a Java Class in Eclipse**

**Objective**: Practice creating a Java class in Eclipse, running it, and using the Debug mode to examine its behavior.

#### Tasks:

1. **Create a Java class** named `Calculator` with the following methods:

   - `add(int a, int b)`: Returns the sum of `a` and `b`.

   - `subtract(int a, int b)`: Returns the result of `a - b`.
   - `multiply(int a, int b)`: Returns the result of `a * b`.
   - `divide(int a, int b)`: Returns the result of `a / b`. Ensure you handle division by zero.

2. **Add a `main()` method** to the class where you create an instance of `Calculator` and call each of the methods with some example values. Print the results of each operation.

3. **Run the class** using Eclipse’s "Run as --> Java Application" option to see the results in the console.

4. **Set breakpoints** in each of the methods (`add`, `subtract`, `multiply`, `divide`) and debug the program using Eclipse’s Debug mode.

At each breakpoint, inspect the values of the variables and step through the program execution.

#### Code:
```java
public class Calculator {
    public int add(int a, int b) {
        return a + b;
    }
    
    public int subtract(int a, int b) {
        return a - b;
    }
    
    public int multiply(int a, int b) {
        return a * b;
    }
    
    public int divide(int a, int b) {
        if (b == 0) {
            System.out.println("Error: Division by zero");
            return 0;
        }
        return a / b;
    }

    public static void main(String[] args) {
        Calculator calc = new Calculator();
        System.out.println("Addition: " + calc.add(10, 5));
        System.out.println("Subtraction: " + calc.subtract(10, 5));
        System.out.println("Multiplication: " + calc.multiply(10, 5));
        System.out.println("Division: " + calc.divide(10, 0));
    }
}
```

#### Expected Outcome:

- Learners will gain hands-on experience creating and running Java classes in Eclipse.

- They will also learn how to set breakpoints, step through code, and inspect variables using Eclipse’s Debug mode.

---

### **Exercise 2: Using Eclipse to Refactor and Organize Code into Packages**

**Objective**: Practice organizing Java classes into packages, using Eclipse's refactoring tools, and running a program with multiple classes.

#### Tasks:

1. **Create a new Java project** in Eclipse and organize your code into packages:

   - Create a package called `math.operations`.

   - Inside `math.operations`, create two classes:
     - `Addition`: A class with a method `add(int a, int b)` that returns the sum of two integers.

     - `Multiplication`: A class with a method `multiply(int a, int b)` that returns the product of two integers.

2. **Create a separate package** called `main` and inside it, create a class named `MathRunner` with the `main()` method.

   - The `MathRunner` class should import the `Addition` and `Multiplication` classes from the `math.operations` package.

   - In the `main()` method, create instances of `Addition` and `Multiplication` and call their methods, printing the results.

3. **Use Eclipse’s Refactoring tools** to rename one of the classes (e.g., rename `Addition` to `Sum`). Ensure the code updates correctly throughout the project.

4. **Run the program** using "Run as --> Java Application" and observe the output.

#### Code:

**Addition.java (in `math.operations`)**:
```java
package math.operations;

public class Addition {
    public int add(int a, int b) {
        return a + b;
    }
}
```

**Multiplication.java (in `math.operations`)**:
```java
package math.operations;

public class Multiplication {
    public int multiply(int a, int b) {
        return a * b;
    }
}
```

**MathRunner.java (in `main`)**:
```java
package main;

import math.operations.Addition;
import math.operations.Multiplication;

public class MathRunner {
    public static void main(String[] args) {
        Addition add = new Addition();
        Multiplication multiply = new Multiplication();
        
        System.out.println("Sum: " + add.add(10, 5));
        System.out.println("Product: " + multiply.multiply(10, 5));
    }
}
```

#### Expected Outcome:

- Learners will practice using packages to organize classes and gain familiarity with Eclipse’s refactoring tools.

- They will also understand how to import classes from different packages and run multi-class programs in Eclipse.

---

## Section 9: Introduction To Java Object Oriented Programming

### Additional Coding Exercises:

### **Exercise 1: Designing a Simple Banking System Using OOP**

**Objective**: Practice designing a system with classes, encapsulation, and constructors.

#### Tasks:

1. **Create a class `BankAccount`** that models a simple bank account with the following attributes:

   - `accountNumber`: The account number of the bank account (private).

   - `balance`: The current balance in the account (private).

2. **Add methods** to the `BankAccount` class:

   - `deposit(double amount)`: A method to add money to the balance.

   - `withdraw(double amount)`: A method to withdraw money from the balance. Ensure that the balance does not go below zero.

   - `getBalance()`: A method to retrieve the current balance.
   
3. **Add a constructor** to the `BankAccount` class that accepts an account number and an initial balance.

4. **Create a class `BankAccountRunner`** with the `main()` method where you:

   - Create two instances of `BankAccount` with different account numbers and initial balances.

   - Perform deposit and withdrawal operations and print the balance after each operation.

#### Code:

**BankAccount.java**:
```java
public class BankAccount {
    private String accountNumber;
    private double balance;

    public BankAccount(String accountNumber, double balance) {
        this.accountNumber = accountNumber;
        this.balance = balance;
    }

    public void deposit(double amount) {
        if (amount > 0) {
            balance += amount;
        }
    }

    public void withdraw(double amount) {
        if (amount > 0 && amount <= balance) {
            balance -= amount;
        } else {
            System.out.println("Insufficient balance or invalid amount.");
        }
    }

    public double getBalance() {
        return balance;
    }
}
```

**BankAccountRunner.java**:

```java
public class BankAccountRunner {
    public static void main(String[] args) {
        BankAccount account1 = new BankAccount("12345", 1000.00);
        BankAccount account2 = new BankAccount("67890", 500.00);

        account1.deposit(500.00);
        account1.withdraw(200.00);
        System.out.println("Account 1 Balance: " + account1.getBalance());

        account2.deposit(300.00);
        account2.withdraw(100.00);
        System.out.println("Account 2 Balance: " + account2.getBalance());
    }
}
```

#### Output:

```java
Account 1 Balance: 1300.0
Account 2 Balance: 700.0
```

**Explanation**:

- Account 1 starts with a balance of 1000, then deposits 500, and withdraws 200, resulting in a balance of 1300.

- Account 2 starts with a balance of 500, then deposits 300, and withdraws 100, resulting in a balance of 700.

#### Expected Outcome:

- Learners will practice using constructors to initialize objects.

- They will reinforce the concept of **encapsulation** by using private variables and methods to interact with object state.

- They will learn how to handle validation in methods, such as ensuring a withdrawal doesn't leave the account with a negative balance.

---

### **Exercise 2: Object-Oriented Inventory Management System**
**Objective**: Practice creating multiple classes and using objects to simulate an inventory management system.

#### Tasks:

1. **Create a class `Product`** with the following attributes:

   - `productId`: A unique identifier for the product (private).

   - `productName`: The name of the product (private).

   - `quantity`: The quantity of the product available in stock (private).
   
2. **Add methods** to the `Product` class:

   - `increaseStock(int amount)`: A method to increase the stock of a product.

   - `decreaseStock(int amount)`: A method to decrease the stock of a product. Ensure that the quantity doesn't fall below zero.

   - `getQuantity()`: A method to get the current quantity of the product.

   - `getProductName()`: A method to get the product name.
   
3. **Create a class `Inventory`** to manage multiple `Product` objects. The class should:

   - Contain a list of products.

   - Have methods `addProduct(Product product)` to add a product to the inventory and `removeProduct(String productId)` to remove a product by ID.

4. **Create a class `InventoryManager`** with the `main()` method where:

   - You create a few `Product` objects.

   - You add products to the inventory, increase and decrease stock, and display product details.

#### Code:

**Product.java**:

```java
public class Product {
    private String productId;
    private String productName;
    private int quantity;

    public Product(String productId, String productName, int quantity) {
        this.productId = productId;
        this.productName = productName;
        this.quantity = quantity;
    }

    public void increaseStock(int amount) {
        if (amount > 0) {
            quantity += amount;
        }
    }

    public void decreaseStock(int amount) {
        if (amount > 0 && amount <= quantity) {
            quantity -= amount;
        } else {
            System.out.println("Insufficient stock or invalid amount.");
        }
    }

    public int getQuantity() {
        return quantity;
    }

    public String getProductName() {
        return productName;
    }
}
```

**Inventory.java**:

```java
import java.util.ArrayList;

public class Inventory {
    private ArrayList<Product> products = new ArrayList<>();

    public void addProduct(Product product) {
        products.add(product);
    }

    public void removeProduct(String productId) {
        products.removeIf(product -> product.getProductId().equals(productId));
    }

    public void displayInventory() {
        for (Product product : products) {
            System.out.println("Product: " + product.getProductName() + ", Quantity: " + product.getQuantity());
        }
    }
}
```

**InventoryManager.java**:

```java
public class InventoryManager {
    public static void main(String[] args) {
        Inventory inventory = new Inventory();

        Product laptop = new Product("101", "Laptop", 10);
        Product smartphone = new Product("102", "Smartphone", 20);

        inventory.addProduct(laptop);
        inventory.addProduct(smartphone);

        laptop.increaseStock(5);
        smartphone.decreaseStock(10);

        inventory.displayInventory();
    }
}
```

Output:

```java
Product: Laptop, Quantity: 15
Product: Smartphone, Quantity: 10
```

**Explanation**:

- The Laptop starts with a quantity of 10, and after increasing the stock by 5, its new quantity is 15.

- The Smartphone starts with a quantity of 20, and after decreasing the stock by 10, its new quantity is 10.

#### Expected Outcome:

- Learners will practice object-oriented design by managing relationships between multiple classes (Inventory and Product).

- They will understand the importance of **code encapsulation** by handling inventory operations through methods.

- They will explore concepts like managing collections of objects (`ArrayList`).

---

## Section 11: Primitive Data Types And Alternatives in Java Programming

### Additional Coding Exercises

### **Exercise 1: Number System Converter**

**Objective**: Practice working with different number systems (decimal, octal, and hexadecimal) and integer type conversions in Java.

#### Tasks:

1. **Create a class `NumberSystemConverter`** that has the following functionalities:

   - Convert a decimal number to its binary, octal, and hexadecimal representations.

   - Convert an octal or hexadecimal number (input as a string) back to decimal.
   
2. **Add methods** to the `NumberSystemConverter` class:
   - `toBinary(int number)`: Converts a decimal number to its binary representation.

   - `toOctal(int number)`: Converts a decimal number to its octal representation.

   - `toHexadecimal(int number)`: Converts a decimal number to its hexadecimal representation.

   - `fromOctal(String octal)`: Converts an octal number (as a string) back to decimal.

   - `fromHexadecimal(String hex)`: Converts a hexadecimal number (as a string) back to decimal.
   
3. **Create a `main()` method** to test these methods by converting values between different number systems.

#### Code:

**NumberSystemConverter.java**:

```java
public class NumberSystemConverter {
    public String toBinary(int number) {
        return Integer.toBinaryString(number);
    }

    public String toOctal(int number) {
        return Integer.toOctalString(number);
    }

    public String toHexadecimal(int number) {
        return Integer.toHexString(number);
    }

    public int fromOctal(String octal) {
        return Integer.parseInt(octal, 8);
    }

    public int fromHexadecimal(String hex) {
        return Integer.parseInt(hex, 16);
    }
}
```

**NumberSystemConverterRunner.java**:

```java
public class NumberSystemConverterRunner {
    public static void main(String[] args) {
        NumberSystemConverter converter = new NumberSystemConverter();

        // Decimal to Binary, Octal, Hexadecimal
        int decimal = 255;
        System.out.println("Binary of 255: " + converter.toBinary(decimal));
        System.out.println("Octal of 255: " + converter.toOctal(decimal));
        System.out.println("Hexadecimal of 255: " + converter.toHexadecimal(decimal));

        // Octal and Hexadecimal back to Decimal
        String octal = "377";
        String hex = "FF";
        System.out.println("Octal 377 to Decimal: " + converter.fromOctal(octal));
        System.out.println("Hexadecimal FF to Decimal: " + converter.fromHexadecimal(hex));
    }
}
```

#### Output:

```java
Binary of 255: 11111111
Octal of 255: 377
Hexadecimal of 255: ff
Octal 377 to Decimal: 255
Hexadecimal FF to Decimal: 255
```

**Explanation**:

- The binary representation of 255 is 11111111.

- The octal representation of 255 is 377.

- The hexadecimal representation of 255 is ff.

- The octal number 377 is equivalent to 255 in decimal.

- The hexadecimal number FF is also equivalent to 255 in decimal.

#### Expected Outcome:

- Learners will gain a better understanding of how Java handles different number systems.

- They will practice working with **string parsing** and **integer conversion** functions in Java.
  
---

### **Exercise 2: Simple Interest Calculator Using `BigDecimal`**

**Objective**: Practice handling precise floating-point calculations using `BigDecimal`.

#### Tasks:

1. **Create a class `SimpleInterestCalculator`** that performs a simple interest calculation using `BigDecimal`.

   - The class should accept a principal amount and interest rate as `String` inputs.

   - It should calculate the total value after a given number of years using the formula:  
     `Total Amount = Principal + (Principal * Interest * Number of Years)`
   
2. **Add methods** to the `SimpleInterestCalculator` class:

   - `calculateTotalValue(int years)`: Calculates the total value after the given number of years.

3. **Create a `main()` method** to test the interest calculation with various inputs.

#### Code:

**SimpleInterestCalculator.java**:

```java
import java.math.BigDecimal;

public class SimpleInterestCalculator {
    private BigDecimal principal;
    private BigDecimal interestRate;

    public SimpleInterestCalculator(String principal, String interestRate) {
        this.principal = new BigDecimal(principal);
        this.interestRate = new BigDecimal(interestRate).divide(new BigDecimal("100"));
    }

    public BigDecimal calculateTotalValue(int years) {
        BigDecimal totalInterest = principal.multiply(interestRate).multiply(new BigDecimal(years));
        return principal.add(totalInterest);
    }
}
```

**SimpleInterestCalculatorRunner.java**:

```java
public class SimpleInterestCalculatorRunner {
    public static void main(String[] args) {
        SimpleInterestCalculator calculator = new SimpleInterestCalculator("5000", "5");
        BigDecimal totalValue = calculator.calculateTotalValue(3);
        System.out.println("Total Amount after 3 years: " + totalValue);
    }
}
```

#### Output:

```java
Total Amount after 3 years: 5750.00
```

**Explanation**:

- The principal amount is `5000`.

- The interest rate is 5%, which, over 3 years, results in a total interest of `750` (`5000 * 0.05 * 3`).
Therefore, the total amount after 3 years is `5750`.


#### Expected Outcome:

- Learners will reinforce the use of the `BigDecimal` class for accurate floating-point arithmetic.

- They will explore handling **precise calculations**, which is particularly useful in financial applications.

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

### Additional Coding Exercises:

### **Exercise 1: Grade Evaluator Using if-else and switch**

**Objective**: Create a Java program that evaluates a student's grade based on their score and gives feedback using both `if-else` and `switch` statements.

#### Task:

1. Create a class `GradeEvaluator` that performs the following:

   - **If-else version**: Takes an integer input (score between 0 and 100) and prints the corresponding letter grade using `if-else if` logic:

     - 90-100: Grade A

     - 80-89: Grade B

     - 70-79: Grade C

     - 60-69: Grade D

     - 0-59: Grade F

   - **Switch version**: Using integer division, create a `switch` version to achieve the same result. (For example, dividing the score by 10 simplifies the range logic.)

2. Add a method to print feedback for each grade:

   - A: "Excellent work!"

   - B: "Good job!"

   - C: "You passed."

   - D: "Barely passed."

   - F: "Failed. Try again."

#### Code:

**GradeEvaluator.java**:

```java
public class GradeEvaluator {

    // if-else version
    public void evaluateGradeIfElse(int score) {
        if (score >= 90 && score <= 100) {
            System.out.println("Grade A - Excellent work!");
        } else if (score >= 80 && score < 90) {
            System.out.println("Grade B - Good job!");
        } else if (score >= 70 && score < 80) {
            System.out.println("Grade C - You passed.");
        } else if (score >= 60 && score < 70) {
            System.out.println("Grade D - Barely passed.");
        } else if (score >= 0 && score < 60) {
            System.out.println("Grade F - Failed. Try again.");
        } else {
            System.out.println("Invalid score.");
        }
    }

    // switch version
    public void evaluateGradeSwitch(int score) {
        switch (score / 10) {
            case 10:
            case 9:
                System.out.println("Grade A - Excellent work!");
                break;
            case 8:
                System.out.println("Grade B - Good job!");
                break;
            case 7:
                System.out.println("Grade C - You passed.");
                break;
            case 6:
                System.out.println("Grade D - Barely passed.");
                break;
            default:
                System.out.println("Grade F - Failed. Try again.");
        }
    }
}
```

**GradeEvaluatorRunner.java**:

```java
public class GradeEvaluatorRunner {
    public static void main(String[] args) {
        GradeEvaluator evaluator = new GradeEvaluator();

        // Test with different scores
        System.out.println("Using if-else:");
        evaluator.evaluateGradeIfElse(85);

        System.out.println("Using switch:");
        evaluator.evaluateGradeSwitch(72);
    }
}
```

Input (in `GradeEvaluatorRunner.java`):

```java
evaluator.evaluateGradeIfElse(85);
evaluator.evaluateGradeSwitch(72);
```

**Output**:

```java
Using if-else:
Grade B - Good job!

Using switch:
Grade C - You passed.
```

**Explanation**:

- For the if-else evaluation with an input of 85, the output is "Grade B - Good job!" because 85 falls in the 80-89 range, which corresponds to a B grade.

- For the switch evaluation with an input of 72, the output is "Grade C - You passed." because 72 falls in the 70-79 range, which corresponds to a C grade.

#### Expected Outcome:

- Learners will understand how to use both `if-else` and `switch` to handle conditional branching.

- They'll see how range logic can be simplified with integer division for `switch` cases.

---

### **Exercise 2: Tax Bracket Calculator Using Ternary Operator**

**Objective**: Use the ternary operator to calculate and print tax brackets based on income.

#### Task:

1. Create a class `TaxBracketCalculator` that:

   - Takes an integer input representing annual income and calculates the applicable tax rate using the ternary operator.

   - Tax Brackets:

     - Income > 100,000: 30% tax

     - Income between 50,001 and 100,000: 20% tax

     - Income between 30,001 and 50,000: 10% tax

     - Income ≤ 30,000: 5% tax
     
2. Add methods:

   - `calculateTaxRate`: Returns the tax rate as a percentage.

   - `calculateTax`: Returns the total tax amount (income * tax rate).

#### Code:

**TaxBracketCalculator.java**:

```java
public class TaxBracketCalculator {

    // Calculate tax rate using the ternary operator
    public double calculateTaxRate(int income) {
        return (income > 100000) ? 0.30 :
               (income > 50000) ? 0.20 :
               (income > 30000) ? 0.10 : 0.05;
    }

    // Calculate total tax based on income
    public double calculateTax(int income) {
        double taxRate = calculateTaxRate(income);
        return income * taxRate;
    }
}
```

**TaxBracketCalculatorRunner.java**:

```java
public class TaxBracketCalculatorRunner {
    public static void main(String[] args) {
        TaxBracketCalculator calculator = new TaxBracketCalculator();

        int income = 75000;
        double taxRate = calculator.calculateTaxRate(income);
        double tax = calculator.calculateTax(income);

        System.out.println("Income: $" + income);
        System.out.println("Tax Rate: " + (taxRate * 100) + "%");
        System.out.println("Tax Amount: $" + tax);
    }
}
```

#### Input (in `TaxBracketCalculatorRunner.java`):

```java
int income = 75000;
```

#### Output:

```java
Income: $75000
Tax Rate: 20.0%
Tax Amount: $15000.0
```

**Explanation**:

- With an income of $75,000, the program calculates the tax rate as 20%, which applies to incomes between $50,001 and $100,000.

- The tax amount is calculated as 75,000 * 0.20 = 15,000, so the tax to be paid is $15,000.

#### Expected Outcome:

- Learners will explore using the ternary operator for compact conditional logic.

- They'll practice calculating tax rates and amounts based on given inputs.

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

### Additional Coding Exercises:

> **Note**: Exercises are based on the Step 1 as other Steps are not present in Github repo for Loops.

> EXERCISES TO BE ADDED IN NEXT PULL REQUEST - Last Updated - 12th Oct 2024 (03:12 AM)

---

## Section 16: Reference Types in Java Programming

### Step 14 - Java Reference Types - Conclusion

> **Note**: Step-14 is not present in GitHub repo.

---

## Section 18: Arrays and ArrayLists in Java Programming

### Step 01 - Understanding the need and Basics about an Array

You can use an index to find the specific element from the array. It is done by using the indexing operator, '[]'.

The expression marks[0] maps to the first array element stored at index 0 of the array marks.

```java
jshell> marks[0]
$20 ==> 75

jshell> marks[1]
$21 ==> 60

jshell> marks[2]
$22 ==> 56
```

---

### Step 16 - Introduction to Array and ArrayList - Conclusion

> **Note**: Step-16 is not present in GitHub repo.

---

## Section 20: Java - Oriented Programming Again

### Step 20 - Java Interface Flyable and Abstract Class Animal - An Exercise

> Not found in Github repo.

---

### Step 21 - Polymorphism - An introduction

> Not found in Github repo.

---

## Section 25: Introduction to Functional Programming in Java

### Step 12 - Optional class in Java - An Introduction

In an earlier section, we wrote and ran the following code:

```java
	jshell> List.of(23, 12, 34, 53).stream().max((n1, n2) -> Integer.compare(n1, n2));
	Optional[53]
	jshell>
```

In order to get the result in a form you would appreciate, we modified this code to look like:

```java
jshell> List.of(23, 12, 34, 53).stream().max((n1, n2) -> Integer.compare(n1, n2)).get();
53
jshell>
```

`max()` is a stream operation, that needs to consume a stream. It is possible that the input stream is empty. In that case, the maximum value would be null. It is undesirable in FP to encounter an exception during a stream operation.

It is extremely inelegant if we are asked to handle an exception in an FP code pipeline.

---

## Section 27: Introduction to Threads And Concurrency in Java

### Step 08 - Need for Controlling the Execution of Threads

Drawbacks of earlier approaches

We saw few of the methods for synchronization in the Thread class

- `start()`
- `join()`
- `sleep()`
- `wait()`

#### Above approaches have a few drawbacks:

No Fine-Grained Control: Suppose, for instance , we want Task3 to run after any one of Task1 or Task2 is done.

#### How do we do it?

- **Difficult to maintain**: Imagine managing 5-10 threads with code written in earlier examples. It would become very difficult to maintain.

- **NO Sub-Task Return Mechanism**: With the Thread class or the Runnable interface, there is no way to get the result from a sub-task.

---

### Step 14 - Threads and MultiThreading - Conclusion

> **Note**: Step-14 is not present in GitHub repo.

---

## Section 28: Introduction to Exception Handling in Java

### Step 01 - Introduction to Exception Handling - Your Thought Process during Exceptions

#### Snippet-1 : Exception Condition

ExceptionHandlingRunner.java

```java

	package com.in28minutes.exceptionhandling;
	
	public class ExceptionHandlingRunner {
		public static void main(String[] args) {
			callMethod();
			System.out.println("callMethod Done");		
		}

		static void callMethod() {
			String str = null;
			int len = str.length();
			System.out.println("String Length Done");
		}		
	}	
```

#### Console Output

```java
java.lang.NullPointerException

Exception in thread "main" java.lang.NullPointerException

at com.in28minutes.exceptionhandling.ExceptionHandlingRunner.callMethod (ExceptionHandlingRunner.java:8)

at com.in28minutes.exceptionhandling.ExceptionHandlingRunner.main (ExceptionHandlingRunner.java:4)
```


#### Snippet-01 Explained

A java.lang.NullPointerException is thrown by the Java run-time when we called length() on the null reference.

If an exception is not handled in the entire call chain, including main, the exception is thrown out and the program terminates.

System.out.println() statements after the exception are never executed.

The runtime prints the call stack trace onto the console.

For instance, consider this simple class Test:

```java
	public class Test {
		public static void main(String[] args) {
			callOne();
		}

		public static void callOne() {
			callTwo();
		}

		public static void callTwo() {
			callThree();
		}

		public static void callThree() {
			String name;
			System.out.println("This name is %d characters long", name.length());
		}
	}
```

However, the code name.length() used in callThree() caused a NullPointerException to be thrown.

However, this is not handled, and the console coughs up the following display:

```java
Exception in thread "main" java.lang.NullPointerException

at Test.callThree(Test.java:13)

at Test.callTwo(Test.java:9)

at Test.callOne(Test.java:6)

at Test.main(Test.java:3)
```

This is nothing but a call trace of the stack, frozen in time.

---

### Step 14 - Exception Handling - Conclusion with Best Practices

> **Note**: Step-14 is not present in GitHub repo.

---

## Section 29: Files and Directories in Java

### Step 05 - Files - Conclusion

> Not found in Github repo.

---

## Section 30: More Concurrency with Concurrent Collections and Atomic Operations

### Step 09 - Conclusion

> **Note**: Step-9 is not present in GitHub repo.

---

## Section 31: Java Tips

> **Note**: Section-31 is not present in GitHub repo.

---

## Section 34: Java New Features - Java 10 to Java 16

> **Note**: Section-34 is not present in GitHub repo.

---
