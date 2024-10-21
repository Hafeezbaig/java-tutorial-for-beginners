## Section 5: Introduction to Java Platform

#### **Group 1: Steps 01 and 07**
- **Step 01 - Overview Of Java Platform - An Introduction**
- **Step 07 - JDK vs JRE vs JVM**

**Why Grouped:**
Both steps provide an overview of Java, covering the foundational concepts of the platform, including bytecode, the Java Virtual Machine (JVM), and the distinctions between the JDK, JRE, and JVM.

### **Puzzle:** (OPTIONAL)
- Write a simple explanation of how Java achieves platform independence using bytecode and the JVM.

- Can you describe what happens from the moment you compile a Java program to when it is run on a specific operating system?

### **Quiz Questions:**
1. **What is bytecode?**
   - A) Machine code for Windows
   - B) Code that runs directly on a CPU
   - C) An intermediate representation understood by the JVM (Answer: C)

2. **What does the JDK contain that the JRE does not?**
   - A) Debugging tools and the compiler (Answer: A)
   - B) The JVM
   - C) Java libraries

3. **Which component is responsible for converting bytecode to machine-specific instructions?**
   - A) JDK
   - B) JVM (Answer: B)
   - C) Compiler

### **Fun Fact:**
- **Did you know?** Java was originally developed by James Gosling at Sun Microsystems and was initially called "Oak" after an oak tree that stood outside Gosling's office. It was later renamed to "Java" after the Indonesian coffee.

---

#### **Group 2: Steps 02, 03, 04, 05, and 06**
- **Step 02 - Java Class and Object - First Look**
- **Step 03 - Create a Method in a Java Class**
- **Step 04 - Create and Compile Planet.java Class**
- **Step 05 - Run Planet Class with Java - Using a main method**
- **Step 06 - Play and Learn with Planet Class**

**Why Grouped:**
These steps introduce learners to creating a basic Java class (`Planet`), adding methods, compiling the code, running it with the `main()` method, and experimenting with the class. These topics flow logically as they guide learners through hands-on programming with Java.

### **Puzzle 1: Creating a Class and Objects**
- Create a class called `Planet` with a method `revolve()` that prints "Revolving around the sun." Instantiate two objects, `earth` and `mars`, and call the `revolve()` method for both objects.

**Code Snippet:**
```java
class Planet {
    void revolve() {
        System.out.println("Revolving around the sun.");
    }
}

public class Main {
    public static void main(String[] args) {
        Planet earth = new Planet();
        Planet mars = new Planet();
        earth.revolve();
        mars.revolve();
    }
}
```

**Expected Output:**
```
Revolving around the sun.
Revolving around the sun.
```

### **Puzzle 2: Add Properties to the Planet Class**
- Extend the `Planet` class to have two properties: `name` and `diameter`. Write a method `displayInfo()` that prints the name and diameter of the planet. Create instances for Earth and Mars with appropriate data.

**Code Snippet:**
```java
class Planet {
    String name;
    double diameter;

    Planet(String name, double diameter) {
        this.name = name;
        this.diameter = diameter;
    }

    void displayInfo() {
        System.out.println(name + " has a diameter of " + diameter + " kilometers.");
    }
}

public class Main {
    public static void main(String[] args) {
        Planet earth = new Planet("Earth", 12742);
        Planet mars = new Planet("Mars", 6779);
        earth.displayInfo();
        mars.displayInfo();
    }
}
```

**Expected Output:**
```
Earth has a diameter of 12742 kilometers.
Mars has a diameter of 6779 kilometers.
```

### **Quiz Questions:**

1. **What is a Java class?**
   - A) A template for creating objects (Answer: A)
   - B) A block of code that runs methods
   - C) A part of the JVM

2. **How do you create an object in Java?**
   - A) Using the `new` keyword (Answer: A)
   - B) Using the `class` keyword
   - C) By declaring an array

3. **What is the purpose of the `main()` method?**
   - A) It compiles the program.
   - B) It is the entry point of the program (Answer: B).
   - C) It defines the class.

### **Fun Fact:**
- **Did you know?** The Java `main()` method is always `public static void main(String[] args)`, and if it's not written exactly like this, Java won't recognize it as the entry point of the program.

---

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

## Section 9: Introduction To Java Object Oriented Programming

#### **Group 1: Steps 01, 02, and 03**

- **Step 01 - Introduction to Object Oriented Programming - Basics**
- **Step 02 - Introduction to Object Oriented Programming - Terminology - Class, Object**
- **Step 03 - Introduction to Object Oriented Programming - Exercise - Online Shopping**

**Why Grouped**: These lectures provide an introduction to Object-Oriented Programming (OOP) concepts, including the basics, terminology, and a practical exercise on online shopping.

### **Puzzle: Define a Class for an Online Shopping Item**

**Problem:**
Create a class called `Item` that represents an item in an online shopping system.

- The `Item` class should have properties like `name`, `price`, and `quantity`.

- Write a method to display the details of the item, including the total cost (`price * quantity`).

**Explanation:**

1. **Define the Class and Properties:**  
   The `Item` class will have `name` (String), `price` (double), and `quantity` (int) properties.
   
   Example:
   ```java
   class Item {
       String name;
       double price;
       int quantity;
   }
   ```

2. **Constructor for Initialization:**  
   The constructor will initialize the values for these properties.
   
   Example:
   ```java
   Item(String name, double price, int quantity) {
       this.name = name;
       this.price = price;
       this.quantity = quantity;
   }
   ```

3. **Method to Display Item Details:**  
   A `displayItemDetails()` method will print the name, price, and total cost (price * quantity).
   
   Example:
   ```java
   void displayItemDetails() {
       double totalCost = price * quantity;
       System.out.println("Item: " + name + ", Price: " + price + ", Quantity: " + quantity + ", Total Cost: " + totalCost);
   }
   ```

4. **Create Objects and Call the Method:**  
   Create instances of `Item` and call `displayItemDetails()` to show details.

   Example:
   ```java
   public class Main {
       public static void main(String[] args) {
           Item phone = new Item("Phone", 299.99, 2);
           phone.displayItemDetails();
       }
   }
   ```

**Output:**

```java
Item: Phone, Price: 299.99, Quantity: 2, Total Cost: 599.98
```

### **Quiz Questions:**

1. **What is the key concept behind Object-Oriented Programming (OOP)?**
   - A) Procedural coding
   - B) Organizing code around objects and classes (Answer: B)
   - C) Structured programming

2. **What does a class define in OOP?**
   - A) Only methods
   - B) Attributes and actions (Answer: B)
   - C) Objects

### **Fun Fact:**
- **Did you know?** Java is one of the most widely used Object-Oriented Programming languages, and OOP helps manage large and complex applications by organizing code into reusable objects.

---

#### **Group 2: Steps 04, 05, and 06**

- **Step 04 - Create Motor Bike Java Class and a couple of objects**
- **Step 05 - Exercise Solutions - Book class and Three instances**
- **Step 06 - Introducing State of an object with speed variable**

**Why Grouped**: These lectures cover practical exercises and examples (Motor Bike and Book classes), focusing on creating objects and introducing state with variables.


### **Puzzle 1: MotorBike Class with Speed**

**Problem:**
Create a class `MotorBike` with a variable `speed`. Write methods to get and set the speed.

- Create two objects: `ducati` and `honda`, with different speeds. Then, print out the speeds of both bikes.

**Explanation:**

1. **Define the Class:**  
   Define the `MotorBike` class with the `speed` property.
   
   Example:
   ```java
   class MotorBike {
       int speed;
   }
   ```

2. **Get and Set Methods:**  
   Write methods to get and set the speed.

   Example:
   ```java
   void setSpeed(int speed) {
       this.speed = speed;
   }
   
   int getSpeed() {
       return this.speed;
   }
   ```

3. **Create Objects and Set Speeds:**  
   Create two instances of `MotorBike` and set their speeds.

   Example:
   ```java
   public class Main {
       public static void main(String[] args) {
           MotorBike ducati = new MotorBike();
           MotorBike honda = new MotorBike();
           
           ducati.setSpeed(100);
           honda.setSpeed(80);
           
           System.out.println("Ducati speed: " + ducati.getSpeed());
           System.out.println("Honda speed: " + honda.getSpeed());
       }
   }
   ```

**Output:**

```java
Ducati speed: 100
Honda speed: 80
```

---

### **Puzzle 2: Create a Book Class and Instances**

**Problem:**
Create a class `Book` with attributes `title`, `author`, and `noOfCopies`. Write a method to display the book’s details.

- Create three instances: `Art of Computer Programming`, `Effective Java`, and `Clean Code`.

**Explanation:**

1. **Step 1: Define the Class and Attributes:**  
   The `Book` class will have `title`, `author`, and `noOfCopies`.

   Example:
   ```java
   class Book {
       String title;
       String author;
       int noOfCopies;
   }
   ```

2. **Step 2: Constructor and Method to Display Book Details:**  
   Add a constructor and a method to display details.

   Example:
   ```java
   Book(String title, String author, int noOfCopies) {
       this.title = title;
       this.author = author;
       this.noOfCopies = noOfCopies;
   }
   
   void displayBookDetails() {
       System.out.println(title + " by " + author + " has " + noOfCopies + " copies.");
   }
   ```

3. **Step 3: Create Objects and Display Details:**  
   Create three `Book` objects and display their details.

   Example:
   ```java
   public class Main {
       public static void main(String[] args) {
           Book book1 = new Book("Art of Computer Programming", "Donald Knuth", 1000);
           Book book2 = new Book("Effective Java", "Joshua Bloch", 500);
           Book book3 = new Book("Clean Code", "Robert Martin", 300);
           
           book1.displayBookDetails();
           book2.displayBookDetails();
           book3.displayBookDetails();
       }
   }
   ```

**Output:**

```java
Art of Computer Programming by Donald Knuth has 1000 copies.
Effective Java by Joshua Bloch has 500 copies.
Clean Code by Robert Martin has 300 copies.
```

### **Quiz Questions:**

1. **What does the `setSpeed()` method in the MotorBike class do?**
   - A) Sets the speed of the bike (Answer: A)
   - B) Starts the bike
   - C) Increases speed automatically

2. **What is the purpose of instance variables in OOP?**
   - A) To store state data for each object (Answer: A)
   - B) To execute methods
   - C) To call constructors

### **Fun Fact:**
- **Did you know?** Each object in Java has its own **state** (stored in instance variables) and **behavior** (defined by methods), which is why each `MotorBike` or `Book` object can have its own unique values.

---

#### **Group 3: Steps 07, 08, and 09**

- **Step 07 - Understanding basics of Encapsulation with Setter methods**
- **Step 08 - Exercises and Tips - Getters and Generating Getters and Setters with Eclipse**
- **Step 09 - Puzzles on this and initialization of member variables**

**Why Grouped**: These lectures introduce the concept of encapsulation and provide exercises and puzzles related to using getters and setters.

### **Puzzle: Encapsulation with Speed and Validation**

**Problem:**
Modify the `MotorBike` class to use **encapsulation**. Make the `speed` variable private and provide getter and setter methods. Ensure the setter method does not allow negative speeds.

**Explanation:**

1. **Encapsulate the Speed Property:**  
   Make the `speed` variable private.

   Example:
   ```java
   private int speed;
   ```

2. **Create Getters and Setters with Validation:**  
   Create getter and setter methods. The setter should only allow non-negative values for speed.

   Example:
   ```java
   void setSpeed(int speed) {
       if (speed >= 0) {
           this.speed = speed;
       }
   }
   
   int getSpeed() {
       return this.speed;
   }
   ```

3. **Create Objects and Test the Validation:**  
   Create `MotorBike` objects, set their speeds, and attempt to set a negative speed (which should be ignored).

   Example:
   ```java
   public class Main {
       public static void main(String[] args) {
           MotorBike ducati = new MotorBike();
           ducati.setSpeed(100);
           ducati.setSpeed

           (-50); // This should be ignored
           
           System.out.println("Ducati speed: " + ducati.getSpeed()); // Output should be 100
       }
   }
   ```

**Output:**

```java
Ducati speed: 100
```

### **Quiz Questions:**

1. **What is encapsulation in Java?**
   - A) Hiding implementation details (Answer: A)
   - B) Making all variables public
   - C) Creating multiple objects

2. **What does the getter method do?**
   - A) Retrieves the value of a variable (Answer: A)
   - B) Changes the value of a variable
   - C) Deletes a variable

### **Fun Fact:**

- **Did you know?** Encapsulation is a way to protect data in a class by restricting direct access to it and using controlled methods (getters and setters) for modification.

---

#### **Group 4: Steps 10, 11, and 12**

- **Step 10 - First Advantage of Encapsulation**
- **Step 11 - Introduction to Encapsulation - Level 2**
- **Step 12 - Encapsulation Exercises - Better Validation and Book class**

**Why Grouped:** These steps explore **encapsulation** in more depth, focusing on its advantages and how better validation can be achieved by using it.

### **Puzzle 1: Book Class with Price Validation**

**Problem:**
Create a class `Book` with private properties `title`, `author`, and `price`. Use getter and setter methods to access these properties, but ensure the `price` cannot be negative.

- Create a few instances of the `Book` class and test the validation.

**Explanation:**

1. **Private Properties:**  
   Make the `title`, `author`, and `price` variables private to ensure encapsulation.

   Example:
   ```java
   class Book {
       private String title;
       private String author;
       private double price;
   }
   ```

2. **Getters and Setters with Validation:**  
   Write getter and setter methods. The setter for `price` will ensure that it does not accept negative values.

   Example:
   ```java
   void setPrice(double price) {
       if (price >= 0) {
           this.price = price;
       }
   }

   double getPrice() {
       return price;
   }
   ```

3. **Create and Test Book Objects:**  
   Create instances of the `Book` class and test setting the `price`. Try setting both valid and invalid prices to see the validation in action.

   Example:
   ```java
   public class Main {
       public static void main(String[] args) {
           Book book1 = new Book();
           book1.setPrice(20);
           book1.setPrice(-5); // This should be ignored

           System.out.println("Book price: " + book1.getPrice()); // Should display 20
       }
   }
   ```

**Output:**

```java
Book price: 20.0
```

---

### **Puzzle 2: Better Validation with Book Class**

**Problem:**
Extend the `Book` class to add a new private property `numberOfPages`. 

- Add a setter for `numberOfPages` that ensures the value must be greater than zero.

- Create a few book instances and validate the number of pages.

**Explanation:**

1. **Add `numberOfPages` Property:**  
   Make `numberOfPages` private and ensure encapsulation.

   Example:
   ```java
   private int numberOfPages;
   ```

2. **Setter with Validation:**  
   The setter for `numberOfPages` will validate that the number must be greater than zero.

   Example:
   ```java
   void setNumberOfPages(int numberOfPages) {
       if (numberOfPages > 0) {
           this.numberOfPages = numberOfPages;
       }
   }

   int getNumberOfPages() {
       return numberOfPages;
   }
   ```

3. **Test Validation:**  
   Test the validation by creating instances of the `Book` class and setting valid and invalid values for `numberOfPages`.

   Example:
   ```java
   public class Main {
       public static void main(String[] args) {
           Book book2 = new Book();
           book2.setNumberOfPages(100);
           book2.setNumberOfPages(-10); // This should be ignored

           System.out.println("Number of pages: " + book2.getNumberOfPages()); // Should display 100
       }
   }
   ```

**Output:**

```java
Number of pages: 100
```

### **Quiz Questions:**

1. **What is the main advantage of using encapsulation?**
   - A) Faster code execution
   - B) Better control over data validation (Answer: B)
   - C) More readable code

2. **What does a private variable mean in Java?**
   - A) The variable can only be accessed inside its class (Answer: A)
   - B) The variable can be accessed by other classes

### **Fun Fact:**

- **Did you know?** Encapsulation is one of the key principles of OOP and helps create **safe** and **modular** code by hiding the internal workings of classes and exposing only what is necessary.

---

#### **Group 5: Steps 13, 14, and 15**

- **Step 13 - Introduction to Abstraction**
- **Step 14 - Introduction to Java Constructors**
- **Step 15 - Introduction to Java Constructors - Exercises and Puzzles**

**Why Grouped:** These steps cover the concepts of **abstraction** and **constructors** in Java. There are exercises and puzzles related to constructors.

Sure! Here’s the updated version of the **Puzzle 1: Abstraction with Vehicle Class** example, following the correct approach for **inner classes** and abstract classes, as we've just fixed it.

### **Puzzle 1: Abstraction with Vehicle Class (Using Inner Classes)**

#### **Problem:**
Create an abstract class `Vehicle` with an abstract method `move()`. 

- Inside `Vehicle`, create two inner classes `Car` and `Bicycle` that extend `Vehicle` and provide their own implementation of `move()`.

#### **Explanation:**

1. **Abstract Class and Method:**
   - The `Vehicle` class is abstract and contains an abstract method `move()` that must be implemented by the inner classes.

   **Example:**
   ```java
   abstract class Vehicle {
       abstract void move();
   }
   ```

2. **Inner Classes Implementing the Abstract Method:**
   - Both `Car` and `Bicycle` are inner classes of `Vehicle`, and each implements the `move()` method in its own way.

   **Example:**
   ```java
   class Car extends Vehicle {
       void move() {
           System.out.println("Car is moving on the road.");
       }
   }

   class Bicycle extends Vehicle {
       void move() {
           System.out.println("Bicycle is pedaling on the street.");
       }
   }
   ```

3. **Test the Classes:**
   - To test these classes, create an anonymous instance of `Vehicle` and use it to instantiate the inner classes (`Car` and `Bicycle`). Then, call the `move()` methods on each instance.

   **Example:**
   ```java
   public class Main {
       public static void main(String[] args) {
           // Create an instance of the outer Vehicle class
           Vehicle vehicle = new Vehicle() {
               @Override
               void move() {
                   // This block is required but not used
               }
           };
           
           // Use the outer class instance to create inner class objects
           Vehicle.Car car = vehicle.new Car();
           Vehicle.Bicycle bicycle = vehicle.new Bicycle();

           // Call the move method on both inner class instances
           car.move();        // Output: Car is moving on the road.
           bicycle.move();    // Output: Bicycle is pedaling on the street.
       }
   }
   ```

4. **Output:**
   ```
   Car is moving on the road.
   Bicycle is pedaling on the street.
   ```

---

### **Puzzle 2: Constructor in a Person Class**

**Problem:**
Create a class `Person` with attributes `name` and `age`. Write a constructor that initializes these attributes.

- Create instances of `Person` and print the name and age.

**Explanation:**

1. **Class with Constructor:**  
   The `Person` class will have a constructor that initializes `name` and `age`.

   Example:
   ```java
   class Person {
       String name;
       int age;

       Person(String name, int age) {
           this.name = name;
           this.age = age;
       }
   }
   ```

2. **Create and Display `Person` Objects:**  
   Create two `Person` objects and display their details using the constructor.

   Example:
   ```java
   public class Main {
       public static void main(String[] args) {
           Person person1 = new Person("Alice", 25);
           Person person2 = new Person("Bob", 30);

           System.out.println(person1.name + " is " + person1.age + " years old.");
           System.out.println(person2.name + " is " + person2.age + " years old.");
       }
   }
   ```

**Output:**

```java
Alice is 25 years old.
Bob is 30 years old.
```

### **Quiz Questions:**

1. **What is the purpose of a constructor in Java?**
   - A) It defines an abstract method
   - B) It initializes an object when it is created (Answer: B)
   - C) It deletes the object

2. **What is abstraction in OOP?**
   - A) Hiding implementation details and exposing only essential features (Answer: A)
   - B) Creating multiple objects
   - C) Writing simple code

### **Fun Fact:**

- **Did you know?** **Abstraction** allows you to define **general behaviors** in a base class, while **specific behaviors** are left to subclasses. Constructors, on the other hand, help you initialize objects when they are created.

---

#### **Group 6: Step 16**

- **Step 16 - Introduction to Object Oriented Programming - Conclusion**

**Why Grouped:** This step wraps up the entire OOP section, summarizing the key concepts learned.

### **Quiz Questions:**

1. **Which of the following is NOT one of the four pillars of OOP?**
   - A) Encapsulation
   - B) Abstraction
   - C) Compilation (Answer: C)

2. **What is polymorphism in OOP?**
   - A) The ability of one method to behave differently based on the object (Answer: A)
   - B) The inheritance of properties
   - C) Writing multiple methods

### **Fun Fact:**

- **Did you know?** The four pillars of OOP are designed to help developers **organize, structure, and manage complex code** by providing a framework that promotes flexibility, reusability, and scalability.

---

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

    public Object getProductId() {
        return null;
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
