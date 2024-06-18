
```markdown
# Java Notes for Beginners

## Introduction to Java
- **Java**: A high-level, class-based, object-oriented programming language designed to have as few implementation dependencies as possible.
- **JVM (Java Virtual Machine)**: Runs Java bytecode and ensures Java's platform independence.
- **JRE (Java Runtime Environment)**: Provides libraries, Java Virtual Machine (JVM), and other components to run applications written in Java.
- **JDK (Java Development Kit)**: Full-featured software development kit, includes JRE, an interpreter/loader (Java), a compiler (javac), an archiver (jar), a documentation generator (Javadoc), and other tools needed in Java development.

## Basic Syntax
- **Main Method**: Entry point of any Java program.
  ```java
  public class Main {
      public static void main(String[] args) {
          System.out.println("Hello, World!");
      }
  }
  ```

## Variables and Data Types
- **Primitive Data Types**:
  - `int` (Integer): 32-bit signed two's complement integer.
  - `float` (Floating Point): Single-precision 32-bit IEEE 754 floating point.
  - `double` (Double Precision): Double-precision 64-bit IEEE 754 floating point.
  - `char` (Character): 16-bit Unicode character.
  - `boolean` (Boolean): Represents one bit of information, true or false.
  - `byte` (Byte): 8-bit signed two's complement integer.
  - `short` (Short): 16-bit signed two's complement integer.
  - `long` (Long): 64-bit signed two's complement integer.
  
- **Reference Data Types**: Classes, Arrays, Interfaces, etc.

## Operators
- **Arithmetic Operators**: `+`, `-`, `*`, `/`, `%`
- **Relational Operators**: `==`, `!=`, `>`, `<`, `>=`, `<=`
- **Logical Operators**: `&&`, `||`, `!`
- **Assignment Operators**: `=`, `+=`, `-=`, `*=`, `/=`
- **Unary Operators**: `+`, `-`, `++`, `--`, `!`

## Control Flow Statements
- **Conditional Statements**:
  - `if`, `if-else`, `if-else-if`, `switch`
  ```java
  if (condition) {
      // code to be executed if condition is true
  } else {
      // code to be executed if condition is false
  }
  
  switch (expression) {
      case value1:
          // code to be executed
          break;
      case value2:
          // code to be executed
          break;
      default:
          // code to be executed if all cases are false
  }
  ```

- **Loops**:
  - `for`, `while`, `do-while`
  ```java
  for (int i = 0; i < 5; i++) {
      System.out.println(i);
  }

  int i = 0;
  while (i < 5) {
      System.out.println(i);
      i++;
  }

  int j = 0;
  do {
      System.out.println(j);
      j++;
  } while (j < 5);
  ```

## Arrays
- **One-dimensional array**:
  ```java
  int[] numbers = new int[5];
  numbers[0] = 1;
  numbers[1] = 2;
  // and so on...
  ```
- **Multi-dimensional array**:
  ```java
  int[][] matrix = new int[3][3];
  matrix[0][0] = 1;
  matrix[0][1] = 2;
  // and so on...
  ```

## Methods
- **Method Declaration**:
  ```java
  public static int add(int a, int b) {
      return a + b;
  }
  
  // Calling a method
  int sum = add(5, 3);
  System.out.println(sum); // Outputs 8
  ```

## Object-Oriented Programming (OOP) Concepts
- **Class and Object**:
  - **Class**: Blueprint for creating objects (a particular data structure).
  - **Object**: Instance of a class.

  ```java
  public class Car {
      // Fields
      int year;
      String model;
      
      // Method
      void display() {
          System.out.println(year + " " + model);
      }
  }

  public class Main {
      public static void main(String[] args) {
          Car myCar = new Car(); // Creating an object
          myCar.year = 2020;
          myCar.model = "Toyota";
          myCar.display(); // Outputs 2020 Toyota
      }
  }
  ```

- **Inheritance**:
  ```java
  class Animal {
      void eat() {
          System.out.println("This animal eats");
      }
  }

  class Dog extends Animal {
      void bark() {
          System.out.println("The dog barks");
      }
  }

  public class Main {
      public static void main(String[] args) {
          Dog myDog = new Dog();
          myDog.eat(); // Outputs: This animal eats
          myDog.bark(); // Outputs: The dog barks
      }
  }
  ```

- **Polymorphism**: Ability of an object to take many forms. Method overloading (compile-time) and method overriding (runtime) are examples.

- **Encapsulation**:
  ```java
  public class Person {
      private String name;
      public String getName() {
          return name;
      }
      public void setName(String newName) {
          name = newName;
      }
  }
  ```

- **Abstraction**:
  ```java
  abstract class Animal {
      abstract void makeSound();
  }

  class Dog extends Animal {
      void makeSound() {
          System.out.println("Bark");
      }
  }

  public class Main {
      public static void main(String[] args) {
          Animal myDog = new Dog();
          myDog.makeSound(); // Outputs: Bark
      }
  }
  ```

## Exception Handling
- **Try-Catch Block**:
  ```java
  try {
      // Code that may throw an exception
  } catch (Exception e) {
      // Code to handle the exception
  } finally {
      // Code to be executed regardless of an exception
  }
  ```

- **Throwing Exceptions**:
  ```java
  public void checkAge(int age) {
      if (age < 18) {
          throw new ArithmeticException("Access denied - You must be at least 18 years old.");
      } else {
          System.out.println("Access granted - You are old enough!");
      }
  }
  ```

## Basic Input and Output
- **Using Scanner**:
  ```java
  import java.util.Scanner;
  public class Main {
      public static void main(String[] args) {
          Scanner scanner = new Scanner(System.in);
          System.out.print("Enter your name: ");
          String name = scanner.nextLine();
          System.out.println("Hello, " + name);
      }
  }
  ```

## Java Collections Framework
- **Common Interfaces**: List, Set, Map
- **Common Classes**: ArrayList, HashSet, HashMap
  ```java
  import java.util.ArrayList;
  import java.util.HashSet;
  import java.util.HashMap;

  public class Main {
      public static void main(String[] args) {
          // ArrayList
          ArrayList<String> list = new ArrayList<>();
          list.add("Apple");
          list.add("Banana");
          System.out.println(list);

          // HashSet
          HashSet<String> set = new HashSet<>();
          set.add("Apple");
          set.add("Banana");
          System.out.println(set);

          // HashMap
          HashMap<String, String> map = new HashMap<>();
          map.put("name", "Rudhresh");
          map.put("role", "Developer");
          System.out.println(map);
      }
  }
  ```

## Conclusion
- **Practice**: The best way to learn Java is through practice and building projects.
- **Resources**: Utilize online tutorials, documentation, and communities for additional help and examples.
```

You can copy and save this content into a markdown (.md) file.
