# Java Basics

### 🔹 JVM (Java Virtual Machine)

*   Executes bytecode (`.class` files).
*   Converts bytecode → machine code for your OS.
*   Makes Java platform independent ("Write once, run anywhere").

### 🔹 JRE (Java Runtime Environment)

*   JRE = JVM + libraries.
*   Used to run Java programs.
*   Contains core libraries like `java.lang`, `java.util`.

### 🔹 JDK (Java Development Kit)

*   JDK = JRE + development tools.
*   Includes:
    *   `javac` → Compiler (source → bytecode).
    *   `java` → Launcher (runs bytecode in JVM).
    *   Debuggers, docs generator, etc.
*   Needed for development.

### 🔹 Flow of Java Program

Source Code (`.java`) → [`javac`] → Bytecode (`.class`) → [`JVM`] → Machine Code

### 🔹 First Program

```java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}
```

**Compile:**

```bash
javac HelloWorld.java
```

**Run:**

```bash
java HelloWorld
```

### Core Syntax & Building Blocks

#### 🔹 Printing
*   `System.out.println("Hello");` // with newline
*   `System.out.print("Hello");`   // without newline

#### 🔹 Comments
*   `// single-line`
*   `/* multi-line */`

### Variables & Data Types

#### Primitive Types
*   `int` → integers (32-bit)
*   `double` → decimals (64-bit)
*   `char` → single character ('A')
*   `boolean` → `true` or `false`

#### Reference Types
*   `String` → sequence of characters
*   `Array` → collection of elements
*   Custom classes

#### 🔹 Example
```java
int age = 20;
double pi = 3.14;
char grade = 'A';
boolean isJavaFun = true;
String name = "Alice";
```

### Control Flow

#### 🔹 If-Else
```java
if (marks >= 90) {
    System.out.println("A");
} else {
    System.out.println("E");
}
```

#### 🔹 Switch
```java
int day = 3;
switch (day) {
    case 1: System.out.println("Monday"); break;
    case 2: System.out.println("Tuesday"); break;
    default: System.out.println("Other day");
}
```

#### 🔹 Loops
**For Loop:**
```java
for (int i = 1; i <= 5; i++) {
    System.out.println(i);
}
```

**While Loop:**
```java
int j = 1;
while (j <= 5) {
    System.out.println(j);
    j++;
}
```

**Do-While Loop:**
```java
int k = 1;
do {
    System.out.println(k);
    k++;
} while (k <= 5);
```

### Methods, Scope & Memory Model

#### 🔹 Method (Function)
```java
public static int square(int x) {
    return x * x;
}
```

#### 🔹 Calling a Method
```java
int result = square(5);
System.out.println(result); // 25
```

#### 🔹 Method Overloading
```java
int add(int a, int b) { return a + b; }
double add(double a, double b) { return a + b; }
```

#### 🔹 Memory Model
*   **Stack** → stores primitive values & method calls.
*   **Heap** → stores objects & arrays.

**Example:**
```java
int x = 10;          // stack
String s = "Hello";  // reference in stack, object in heap
```

### Classes & Core OOP Fundamentals

#### 🔹 Class
*   A blueprint for objects.
*   Contains fields (variables) and methods (functions).

#### 🔹 Object
*   An instance of a class, created with `new`.

#### 🔹 Example
```java
class Car {
    String brand;
    int year;

    void drive() {
        System.out.println(brand + " is driving.");
    }
}

public class Main {
    public static void main(String[] args) {
        Car myCar = new Car();  // create object
        myCar.brand = "Tesla";
        myCar.year = 2023;

        myCar.drive(); // Tesla is driving.
    }
}
```

#### 🔹 Constructor
*   Special method to initialize objects.

```java
class Car {
    String brand;
    int year;

    Car(String b, int y) { // constructor
        brand = b;
        year = y;
    }
}

// Example Usage:
// Car c1 = new Car("BMW", 2022);
```

#### 🔹 Encapsulation
*   Keep fields private and use getters/setters.

```java
class Student {
    private String name;

    public void setName(String n) { name = n; }
    public String getName() { return name; }
}
```