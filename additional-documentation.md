## Section 5: Introduction to Java Platform

#### **Group 1: Steps 01 and 07**
- **Step 01 - Overview Of Java Platform - An Introduction**
- **Step 07 - JDK vs JRE vs JVM**

**Why Grouped:**
Both steps provide an overview of Java, covering the foundational concepts of the platform, including bytecode, the Java Virtual Machine (JVM), and the distinctions between the JDK, JRE, and JVM.

### **Puzzle:** (OPTIONAL)
- Write a simple explanation of how Java achieves platform independence using bytecode and the JVM.

- Can you describe what happens from the moment you compile a Java program to when it is run on a specific operating system?

### **New Quiz Questions:**

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

### **New Quiz Questions:**

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

### **Exercise 1: Create a "Device" Class with Multiple Methods and Compile It**

#### **Problem:**
Create a Java class called `Device` that represents different electronic devices. The class should:

- Have attributes for the `deviceName`, `brand`, and `powerStatus` (on/off).

- Implement methods:

  - `turnOn()` that prints "Device is turned ON."

  - `turnOff()` that prints "Device is turned OFF."

  - `showDetails()` that prints the device's name and brand.

- Create instances of the `Device` class for a few devices like "Smartphone", "Laptop", and "Tablet". Turn these devices on and off, and display their details.

Once you've created the class, follow these steps:

1. Save the file as `Device.java`.

2. Compile the file using `javac Device.java`.

3. Run the program using `java Device`.

#### **Code:**

```java
public class Device {
    // Attributes of the Device class
    String deviceName;
    String brand;
    boolean powerStatus;

    // Constructor to initialize the device
    public Device(String deviceName, String brand) {
        this.deviceName = deviceName;
        this.brand = brand;
        this.powerStatus = false; // default is off
    }

    // Method to turn on the device
    public void turnOn() {
        if (!powerStatus) {
            powerStatus = true;
            System.out.println(deviceName + " is turned ON.");
        } else {
            System.out.println(deviceName + " is already ON.");
        }
    }

    // Method to turn off the device
    public void turnOff() {
        if (powerStatus) {
            powerStatus = false;
            System.out.println(deviceName + " is turned OFF.");
        } else {
            System.out.println(deviceName + " is already OFF.");
        }
    }

    // Method to show details of the device
    public void showDetails() {
        System.out.println("Device Name: " + deviceName + ", Brand: " + brand);
    }

    // Main method to test the Device class
    public static void main(String[] args) {
        // Creating instances of Device class
        Device smartphone = new Device("Smartphone", "Samsung");
        Device laptop = new Device("Laptop", "Dell");
        Device tablet = new Device("Tablet", "Apple");

        // Turning devices on and showing details
        smartphone.turnOn();
        smartphone.showDetails();

        laptop.turnOn();
        laptop.showDetails();

        tablet.turnOn();
        tablet.showDetails();

        // Turning devices off
        smartphone.turnOff();
        laptop.turnOff();
        tablet.turnOff();
    }
}
```

#### **Explanation:**

**Attributes (deviceName, brand, powerStatus)**: These are the properties of the Device class that hold information about the device’s name, brand, and whether it’s ON or OFF.

**Constructor**: The constructor (`Device()`) initializes each object with a specific `deviceName` and `brand`, and sets the `powerStatus` to OFF by default.

**Methods**:
- `turnOn()`: Turns on the device by setting `powerStatus` to `true`.

- `turnOff()`: Turns off the device by setting `powerStatus` to `false`.

- `showDetails()`: Displays the device's name and brand.

**Main method**: This is where objects are created, methods are called, and the program is run.

#### **Steps to Compile and Run:**

1. Save the file as `Device.java`.

2. In the terminal, compile the code:

   ```
   javac Device.java
   ```

3. Run the code:

   ```
   java Device
   ```

#### **Output:**

```java
Smartphone is turned ON.
Device Name: Smartphone, Brand: Samsung
Laptop is turned ON.
Device Name: Laptop, Brand: Dell
Tablet is turned ON.
Device Name: Tablet, Brand: Apple
Smartphone is turned OFF.
Laptop is turned OFF.
Tablet is turned OFF.
```

---

### **Exercise 2: Create a "Game" Class with a Scoring System**

#### **Problem:**

Write a class called `Game` that models a simple game system. The class should:

- Have attributes for `gameName`, `maxScore`, and `currentScore`.

- Include methods to:

  - `startGame()` to initialize the game.

  - `playGame()` to increase the current score.

  - `endGame()` to print the game details and final score.

- Create instances for games like "Soccer", "Basketball", and "Tennis". Start each game, play to increase the score, and then end the game by displaying the final score.

#### Compile and run the program after saving the file.

#### **Code:**
```java
public class Game {
    // Attributes for the Game class
    String gameName;
    int maxScore;
    int currentScore;

    // Constructor to initialize the game
    public Game(String gameName, int maxScore) {
        this.gameName = gameName;
        this.maxScore = maxScore;
        this.currentScore = 0;
    }

    // Method to start the game
    public void startGame() {
        System.out.println("Starting the game: " + gameName);
        currentScore = 0; // Reset the score to 0
    }

    // Method to play the game and increase score
    public void playGame() {
        if (currentScore < maxScore) {
            currentScore += 10; // Increment score by 10
            System.out.println("Playing " + gameName + "... Current Score: " + currentScore);
        } else {
            System.out.println("Game Over! Maximum score reached.");
        }
    }

    // Method to end the game and show the final score
    public void endGame() {
        System.out.println("Ending the game: " + gameName + ". Final Score: " + currentScore);
    }

    // Main method to test the Game class
    public static void main(String[] args) {
        // Creating instances of Game class
        Game soccer = new Game("Soccer", 50);
        Game basketball = new Game("Basketball", 60);
        Game tennis = new Game("Tennis", 40);

        // Starting and playing games
        soccer.startGame();
        soccer.playGame();
        soccer.playGame();
        soccer.endGame();

        basketball.startGame();
        basketball.playGame();
        basketball.playGame();
        basketball.playGame();
        basketball.endGame();

        tennis.startGame();
        tennis.playGame();
        tennis.playGame();
        tennis.endGame();
    }
}
```

#### **Explanation:**

**Attributes (gameName, maxScore, currentScore)**: These hold the information about the name of the game, the maximum score limit, and the current score during the game.

**Constructor**: Initializes the game with the given `gameName` and `maxScore`, and sets the `currentScore` to 0 when the game starts.

**Methods**:

- `startGame()`: Starts the game and resets the score to 0.

- `playGame()`: Increases the score by 10 points. If the `maxScore` is reached, it prints a message indicating the game is over.

- `endGame()`: Prints the final score and ends the game.

**Main method**: Creates instances of Game, calls the methods to start, play, and end the game, and displays the final score.

#### **Steps to Compile and Run:**

1. Save the file as `Game.java`.

2. In the terminal, compile the code:

   ```
   javac Game.java
   ```

3. Run the code:

   ```
   java Game
   ```

#### **Output:**

```java
Starting the game: Soccer
Playing Soccer... Current Score: 10
Playing Soccer... Current Score: 20
Ending the game: Soccer. Final Score: 20
Starting the game: Basketball
Playing Basketball... Current Score: 10
Playing Basketball... Current Score: 20
Playing Basketball... Current Score: 30
Ending the game: Basketball. Final Score: 30
Starting the game: Tennis
Playing Tennis... Current Score: 10
Playing Tennis... Current Score: 20
Ending the game: Tennis. Final Score: 20
```

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

### **Existing Quiz Questions:**

1. **What is a class in Object Oriented Programming?**
   - A) An instance of an object
   - B) template for creating objects (Answer: B)
   - C) function to perform actions

2. **What are the two main components of an object in Object Oriented Programming?**
    - A) State and Behavior (Answer: A)
    - B) Template and Instance
    - C) Functions and Variables

### **New Quiz Questions:**

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

### **Existing Quiz Questions:**

1. **Which of the following methods in a class is the recommended approach to set the title attribute?**
    - A) setTitle(String title) (Answer: A)
    - B) getTitle()
    - C) setBook(String book)

2. **In a Java class, what is the purpose of a getter method?**
    - A) To modify the value of a private member variable
    - B) To access the value of a private member variable (Answer: B)

### **New Quiz Questions:**

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

### **Existing Quiz Questions:**

1. **What is the purpose of private keyword in Java?**
    - A) To make a variable or method accessible only within the class (Answer: A)
    - B) To make a variable or method accessible outside the class
    - C) To make a variable or method static

2. **What is the main principle that is violated when an object directly accesses the state of another object without using any methods?**
    - A) Inheritance
    - B) Encapsulation (Answer: B)

### **New Quiz Questions:**

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

### **Existing Quiz Questions:**

1. **What are the default values for object member variables when they are not explicitly initialized?**
    - A) null for reference types, true for boolean and the type's minimum value for numeric primitive types
    - B) null for reference types, false for boolean, and 0 for numeric primitive types (Answer: B)
    - C) The type's maximum value for primitive types, true for boolean and null for reference types

### **New Quiz Questions:**

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

### **Existing Quiz Questions:**

1. **What is a constructor in Java?**
    - A) A special method that is called when an object of a class is created. (Answer: A)
    - B) A method that is used to destroy an object.

2. **How is a constructor invoked in Java?**
    - A) By calling the method directly
    - B) By using the new keyword to create an object of the class (Answer: B)
    - C) By declaring the constructor as static

### **New Quiz Questions:**

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

### **New Quiz Questions:**

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

### **Exercise 1: Create a "`GuessTheNumber`" Game**

#### **Problem:**

Create a class called `GuessTheNumber` that allows a player to guess a randomly generated number within a certain range. The class should:

- Have private attributes for the target number, the number of attempts, and a range (minimum and maximum numbers).

- Implement methods:

  - `startGame()` – to start the game and generate a random target number within the range.

  - `guess(int number)` – to accept a guess and provide feedback (too high, too low, or correct).

  - `displayResult()` – to display the total number of attempts made by the player.

The game ends when the player guesses the correct number.

#### **Code:**

```java
import java.util.Random;
import java.util.Scanner;

public class GuessTheNumber {
    // Private attributes of the GuessTheNumber class
    private int targetNumber;     // The random number to be guessed
    private int numberOfAttempts; // Number of attempts made by the player
    private int minRange;         // Minimum value of the range
    private int maxRange;         // Maximum value of the range

    // Constructor to initialize the game with a range
    public GuessTheNumber(int minRange, int maxRange) {
        this.minRange = minRange;
        this.maxRange = maxRange;
        this.numberOfAttempts = 0; // Initialize attempts to 0
    }

    // Method to start the game and generate a random number within the range
    public void startGame() {
        Random random = new Random();
        targetNumber = random.nextInt(maxRange - minRange + 1) + minRange;
        System.out.println("Game started! Try to guess the number between " + minRange + " and " + maxRange);
    }

    // Method to accept a guess and provide feedback
    public void guess(int number) {
        numberOfAttempts++; // Increment the number of attempts with each guess
        if (number == targetNumber) {
            System.out.println("Congratulations! You guessed the correct number.");
            displayResult();
        } else if (number < targetNumber) {
            System.out.println("Too low! Try again.");
        } else {
            System.out.println("Too high! Try again.");
        }
    }

    // Method to display the result (number of attempts made)
    public void displayResult() {
        System.out.println("You guessed the correct number in " + numberOfAttempts + " attempts.");
    }

    // Main method to test the GuessTheNumber game
    public static void main(String[] args) {
        // Create a Scanner to read input from the player
        Scanner scanner = new Scanner(System.in);

        // Create a GuessTheNumber object with a range between 1 and 10
        GuessTheNumber game = new GuessTheNumber(1, 10);

        // Start the game
        game.startGame();

        // Loop until the player guesses the correct number
        boolean correctGuess = false;
        while (!correctGuess) {
            System.out.print("Enter your guess: ");
            int playerGuess = scanner.nextInt();
            game.guess(playerGuess); // Call the guess method with the player's input

            if (playerGuess == game.targetNumber) {
                correctGuess = true; // Break the loop if the guess is correct
            }
        }

        // Close the scanner
        scanner.close();
    }
}
```

#### **Explanation:**

- The `GuessTheNumber` class encapsulates the game logic, including the randomly generated target number, the number of attempts, and the range.

- The constructor initializes the game by setting the range (`minRange`, `maxRange`) and resetting the attempt counter.

- The `startGame()` method generates a random number within the given range.

- The `guess(int number)` method accepts the player's guess, compares it to the target number, and provides feedback (too high, too low, or correct). It also increments the number of attempts.

- The game loop runs until the player guesses the correct number, at which point the game displays the result.

**Attributes (`targetNumber`, `numberOfAttempts`, `minRange`, `maxRange`):** These store the target number to guess, how many guesses the player has made, and the range within which the number is generated.

**Constructor:** Initializes the game's range and resets the attempt counter.

**Methods:**

  - `startGame()`: Randomly generates the target number and starts the game.

  - `guess(int number)`: Takes a guess and gives feedback (too high, too low, or correct).

  - `displayResult()`: Displays the number of attempts made once the player guesses correctly.

**Main method:** Sets up the game, takes input from the player, and loops until the correct guess is made.

#### **Steps to Run:**

1. Save the file as `GuessTheNumber.java`.

2. Compile using:

   ```
   javac GuessTheNumber.java
   ```

3. Run the program:

   ```
   java GuessTheNumber
   ```

#### **Output:**

```
Game started! Try to guess the number between 1 and 100
Enter your guess: 4
Too high! Try again.
Enter your guess: 1
Too low! Try again.
Enter your guess: 3
Congratulations! You guessed the correct number.
You guessed the correct number in 3 attempts.
```

---

### **Exercise 2: Rock, Paper, Scissors Game**

#### **Problem:**
Write a class called `RockPaperScissors` that allows the player to compete against the computer in a game of Rock, Paper, Scissors. The game should:

- Randomly generate the computer’s choice (rock, paper, or scissors).

- Accept the player’s choice.

- Compare the choices to determine the winner.

- Track the player's **wins**, **losses**, and **ties** over multiple rounds.

The game should allow the player to play multiple rounds and display the final score when the player chooses to stop.

#### **Code:**

```java
import java.util.Random;
import java.util.Scanner;

public class RockPaperScissors {
    // Attributes to track player's wins, losses, and ties
    private int wins;
    private int losses;
    private int ties;

    // Constructor to initialize the game with 0 wins, losses, and ties
    public RockPaperScissors() {
        wins = 0;
        losses = 0;
        ties = 0;
    }

    // Method to randomly generate the computer's choice
    public String getComputerChoice() {
        Random random = new Random();
        int choice = random.nextInt(3); // Generates a number between 0 and 2
        switch (choice) {
            case 0:
                return "rock";
            case 1:
                return "paper";
            case 2:
                return "scissors";
            default:
                return ""; // This should never happen
        }
    }

    // Method to determine the winner of a round
    public void playRound(String playerChoice, String computerChoice) {
        System.out.println("Computer chose: " + computerChoice);

        if (playerChoice.equals(computerChoice)) {
            System.out.println("It's a tie!");
            ties++;
        } else if (
            (playerChoice.equals("rock") && computerChoice.equals("scissors")) ||
            (playerChoice.equals("paper") && computerChoice.equals("rock")) ||
            (playerChoice.equals("scissors") && computerChoice.equals("paper"))
        ) {
            System.out.println("You win!");
            wins++;
        } else {
            System.out.println("You lose!");
            losses++;
        }
    }

    // Method to display the player's score
    public void displayScore() {
        System.out.println("Wins: " + wins + ", Losses: " + losses + ", Ties: " + ties);
    }

    // Main method to run the game
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        RockPaperScissors game = new RockPaperScissors();

        boolean keepPlaying = true;

        // Game loop for multiple rounds
        while (keepPlaying) {
            System.out.print("Enter your choice (rock, paper, or scissors): ");
            String playerChoice = scanner.nextLine().toLowerCase(); // Get player's choice and convert to lowercase

            // Validate player input
            if (!playerChoice.equals("rock") && !playerChoice.equals("paper") && !playerChoice.equals("scissors")) {
                System.out.println("Invalid choice. Please enter rock, paper, or scissors.");
                continue;
            }

            // Get computer's choice and play the round
            String computerChoice = game.getComputerChoice();
            game.playRound(playerChoice, computerChoice);

            // Ask if the player wants to play again
            System.out.print("Do you want to play again? (yes or no): ");
            String playAgain = scanner.nextLine().toLowerCase();

            if (!playAgain.equals("yes")) {
                keepPlaying = false; // End the game loop if the player says "no"
            }
        }

        // Display the final score after the game ends
        System.out.println("\nGame Over! Final Score:");
        game.displayScore();

        // Close the scanner
        scanner.close();
    }
}
```

#### **Explanation:**

- **Attributes:**
  - `wins`, `losses`, `ties`: These variables track the player's performance over multiple rounds.
  
- **Methods:**
  - `getComputerChoice()`: Generates a random choice for the computer (either "rock", "paper", or "scissors").

  - `playRound()`: Compares the player's choice and the computer's choice, determines the winner, and updates the scores (wins, losses, ties).

  - `displayScore()`: Displays the total number of wins, losses, and ties after the game ends.

- **Main Method:** 

  - The game runs in a loop, allowing the player to play multiple rounds. The loop continues until the player chooses to stop.

  - The player's input is validated to ensure it's either "rock", "paper", or "scissors".

  - After each round, the player is asked if they want to play again.

#### **Steps to Run:**

1. Save the file as `RockPaperScissors.java`.

2. Compile using:

   ```
   javac RockPaperScissors.java
   ```

3. Run the program:

   ```
   java RockPaperScissors
   ```

#### **Output:**

```java
Enter your choice (rock, paper, or scissors): rock
Computer chose: paper
You lose!
Do you want to play again? (yes or no): yes

Enter your choice (rock, paper, or scissors): scissors
Computer chose: paper
You win!
Do you want to play again? (yes or no): no

Game Over! Final Score:
Wins: 1, Losses: 1, Ties: 0
```

---

### **Exercise 3: Math Quiz Challenge**

#### **Problem:**
Create a game where the player is presented with random math problems (addition, subtraction, multiplication, or division).

The player must solve as many problems as possible within a time limit (e.g., 10 seconds). The game tracks the player's score based on correct answers.

### **Code:**

```java
import java.util.Random;
import java.util.Scanner;
import java.util.Timer;
import java.util.TimerTask;

public class MathQuizChallenge {
    private static int score = 0; // Keeps track of the player's score
    private static boolean timeUp = false; // Keeps track of whether the time is up

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        Random random = new Random();

        System.out.println("Welcome to the Math Quiz Challenge!");
        System.out.println("Solve as many math problems as you can within 10 seconds.");
        System.out.println("Press Enter to start...");
        scanner.nextLine(); // Wait for the player to press Enter

        // Start the timer for 10 seconds
        Timer timer = new Timer();
        timer.schedule(new TimerTask() {
            @Override
            public void run() {
                timeUp = true;
                System.out.println("\nTime's up!");
            }
        }, 10000); // Timer set for 10 seconds

        // Main game loop
        while (!timeUp) {
            // Generate random numbers and a random operation
            int num1 = random.nextInt(10) + 1; // Random number between 1 and 10
            int num2 = random.nextInt(10) + 1; // Random number between 1 and 10
            int operator = random.nextInt(4);  // 0 for +, 1 for -, 2 for *, 3 for /

            String operation = "";
            int correctAnswer = 0;

            switch (operator) {
                case 0:
                    operation = "+";
                    correctAnswer = num1 + num2;
                    break;
                case 1:
                    operation = "-";
                    correctAnswer = num1 - num2;
                    break;
                case 2:
                    operation = "*";
                    correctAnswer = num1 * num2;
                    break;
                case 3:
                    operation = "/";
                    // Ensure that num2 is not zero to avoid division by zero
                    if (num2 == 0) num2 = 1;
                    correctAnswer = num1 / num2;
                    break;
            }

            // Display the math problem to the player
            System.out.print(num1 + " " + operation + " " + num2 + " = ");

            // Check if time has run out before accepting input
            if (scanner.hasNextInt() && !timeUp) {
                int playerAnswer = scanner.nextInt(); // Get the player's answer

                // Check if the player's answer is correct
                if (playerAnswer == correctAnswer) {
                    System.out.println("Correct!");
                    score++;
                } else {
                    System.out.println("Wrong. The correct answer was " + correctAnswer);
                }
            } else {
                break; // Exit the loop if the time is up or no valid input is provided
            }
        }

        // Print the final score after the game loop ends
        System.out.println("\nYour final score is: " + score);

        // Close the scanner
        scanner.close();
    }
}
```

### **Explanation:**

1. **Attributes:**

   - `score`: This variable tracks the number of correct answers the player gives.

   - `timeUp`: This boolean tracks whether the 30-second timer has ended, signaling that the game is over.

2. **Main Method:**

   - **Timer**: A `Timer` is used to count down 30 seconds. Once the time is up, the game stops, and no more problems are presented to the player.

   - **Random Math Problem Generation**: The game randomly generates two numbers (`num1` and `num2`) and selects a random operation (`+`, `-`, `*`, `/`) for the player to solve. 

   - **Game Loop**: The game keeps running until the timer expires. The player's answers are compared to the correct answers, and their score is updated accordingly.

3. **Game Flow:**

   - The player presses **Enter** to start.

   - Math problems are generated one by one, and the player inputs their answer.

   - The game provides feedback for each answer (correct or wrong).

   - After 30 seconds, the game ends, and the player's final score is displayed.

### **Steps to Run:**

1. Save the file as `MathQuizChallenge.java`.

2. Compile the program:

   ```
   javac MathQuizChallenge.java
   ```

3. Run the program:

   ```
   java MathQuizChallenge
   ```

### **Output:**

```java
Welcome to the Math Quiz Challenge!
Solve as many math problems as you can within 10 seconds.
Press Enter to start...

3 + 7 = 10
Correct!
6 * 5 = 30
Correct!
8 / 2 = 4
Correct!
4 - 9 = -5
Correct!
2 * 2 = 5
Wrong. The correct answer was 4
7 + 8 = 15
Correct!

Time's up!
Your final score is: 5
```

### **Possible Enhancements:**

1. **Different Levels:** Adding difficulty levels (easy, medium, hard) where the range of numbers or types of operations becomes more challenging.

2. **Scoring System:** Award more points for solving harder problems (e.g., multiplication and division).

3. **High Score Tracker:** Storing the player's highest score and display it at the end of each game.

---

> End of this document - Last updated 05:58 10/22