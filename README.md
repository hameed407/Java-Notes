# Java-Notes

Great! Let’s look at **operations on data types in Java** — covering **primitive and non-primitive** types with **examples**.

---

# 🔢 1. Arithmetic Operations (for Numeric Data Types)

Applicable to: `byte`, `short`, `int`, `long`, `float`, `double`

### Operators: `+`, `-`, `*`, `/`, `%`

```java
int a = 10, b = 3;
System.out.println(a + b);  // 13
System.out.println(a - b);  // 7
System.out.println(a * b);  // 30
System.out.println(a / b);  // 3
System.out.println(a % b);  // 1
```

---

# 🔄 2. Type Casting (Conversion)

- **Widening**: automatic
- **Narrowing**: manual

```java
int x = 10;
double y = x; // widening

double p = 9.78;
int q = (int)p; // narrowing
System.out.println(q);  // 9
```

---

# 🧠 3. Boolean Operations

Applicable to: `boolean`

### Operators: `&&`, `||`, `!`

```java
boolean a = true;
boolean b = false;

System.out.println(a && b); // false
System.out.println(a || b); // true
System.out.println(!a);     // false
```

---

# 🔤 4. Character Operations

Applicable to: `char`

```java
char c1 = 'A';  // Unicode: 65
char c2 = 'B';  // Unicode: 66

System.out.println(c1 + c2); // 131 (adds ASCII/Unicode values)
System.out.println((int)c1); // 65
```

---

# 📕 5. String Operations (Non-Primitive)

```java
String s1 = "Java";
String s2 = "World";

System.out.println(s1 + " " + s2);           // Java World
System.out.println(s1.length());             // 4
System.out.println(s1.toUpperCase());        // JAVA
System.out.println(s1.charAt(1));            // a
System.out.println(s1.equals("java"));       // false
System.out.println(s1.equalsIgnoreCase("java")); // true
```

---

# 🧰 6. Relational Operations

Applicable to: numeric types and `char`

### Operators: `==`, `!=`, `<`, `>`, `<=`, `>=`

```java
int a = 5, b = 10;
System.out.println(a < b);   // true
System.out.println(a == b);  // false
System.out.println(a != b);  // true
```

---

# 🧠 7. Bitwise Operations

Applicable to: `byte`, `short`, `int`, `long`

### Operators: `&`, `|`, `^`, `~`, `<<`, `>>`

```java
int a = 5;  // 0101
int b = 3;  // 0011

System.out.println(a & b); // 1
System.out.println(a | b); // 7
System.out.println(a ^ b); // 6
System.out.println(~a);    // -6 (inverts all bits)
System.out.println(a << 1); // 10 (shift left)
System.out.println(b >> 1); // 1  (shift right)
```

---

# ✅ Summary Table

| Data Type     | Common Operations                              |
|---------------|------------------------------------------------|
| int, float    | +, -, *, /, %, ==, <, >, etc.                  |
| boolean       | &&, ||, !, ==, !=                              |
| char          | Arithmetic (based on Unicode), Comparison      |
| String        | + (concat), `.length()`, `.equals()`, etc.     |
| All numbers   | Type casting (widening, narrowing), bitwise    |

---

Perfect! Let's now look at **real-world examples** of conditionals and loops in Java to understand how they are used in actual coding scenarios — like authentication checks, filtering, pattern generation, menu systems, and searching.

---

### ✅ 1. **User Authentication (if-else)**
```java
String username = "admin";
String password = "1234";

if (username.equals("admin") && password.equals("1234")) {
    System.out.println("Login Successful!");
} else {
    System.out.println("Invalid Credentials");
}
```
**Output:**
```
Login Successful!
```

---

### ✅ 2. **Check Even or Odd Using `if-else`**
```java
int number = 7;
if (number % 2 == 0) {
    System.out.println("Even");
} else {
    System.out.println("Odd");
}
```
**Output:**
```
Odd
```

---

### ✅ 3. **Grade Evaluation Using `switch`**
```java
char grade = 'B';

switch (grade) {
    case 'A': System.out.println("Excellent!"); break;
    case 'B': System.out.println("Well done"); break;
    case 'C': System.out.println("Good"); break;
    default: System.out.println("Needs Improvement");
}
```
**Output:**
```
Well done
```

---

### ✅ 4. **Sum of First N Numbers (`for` Loop)**
```java
int n = 5;
int sum = 0;

for (int i = 1; i <= n; i++) {
    sum += i;
}
System.out.println("Sum = " + sum);
```
**Output:**
```
Sum = 15
```

---

### ✅ 5. **Filtering Even Numbers From an Array (Enhanced `for`)**
```java
int[] nums = {1, 2, 3, 4, 5};

for (int num : nums) {
    if (num % 2 == 0) {
        System.out.println(num);
    }
}
```
**Output:**
```
2  
4
```

---

### ✅ 6. **Search in Array (Linear Search using `for`)**
```java
int[] arr = {10, 20, 30, 40};
int target = 30;
boolean found = false;

for (int num : arr) {
    if (num == target) {
        found = true;
        break;
    }
}
System.out.println(found ? "Found" : "Not Found");
```
**Output:**
```
Found
```

---

### ✅ 7. **Menu System with `do-while`**
```java
int choice;
Scanner sc = new Scanner(System.in);

do {
    System.out.println("1. Add\n2. Subtract\n3. Exit");
    choice = sc.nextInt();

    switch (choice) {
        case 1: System.out.println("Addition selected"); break;
        case 2: System.out.println("Subtraction selected"); break;
        case 3: System.out.println("Exiting..."); break;
        default: System.out.println("Invalid Choice");
    }
} while (choice != 3);
```
**Output Example:**
```
1. Add  
2. Subtract  
3. Exit  
1  
Addition selected  
...
```

---

### ✅ 8. **Pattern Printing with Nested Loops**
```java
for (int i = 1; i <= 3; i++) {
    for (int j = 1; j <= i; j++) {
        System.out.print("* ");
    }
    System.out.println();
}
```
**Output:**
```
*  
* *  
* * *
```
These examples demonstrate how **loops and conditionals** are the building blocks of logic in most Java programs — from **input handling and validation** to **pattern building and searching/filtering data**.

Here is a complete and structured explanation of the **OOP Concepts in Java**, including your provided definitions, Java code examples, and output for each concept:

---

Great! Let's enhance each OOP concept (Class, Object, Inheritance, Polymorphism, Encapsulation, and Abstraction) with **advanced concepts**, **real-world use cases**, and **improved examples** to deepen your understanding.

---

### 🔹 1. Class and Object  
**Definition:**  
A **class** is a template that defines the structure and behavior (fields and methods) of objects.  
An **object** is an instance of a class with actual values, capable of invoking methods.

**Advanced Concept:**  
- Constructors: Special methods used to initialize objects.  
- Static members: Belong to the class, not instances.

**Example:**
```java
class BankAccount {
    String holderName;
    double balance;
    
    BankAccount(String name, double bal) {
        holderName = name;
        balance = bal;
    }
    
    void display() {
        System.out.println(holderName + "'s balance: ₹" + balance);
    }
}

public class Main {
    public static void main(String[] args) {
        BankAccount acc1 = new BankAccount("Aman", 5000.0);
        acc1.display();
    }
}
```
**Output:**
```
Aman's balance: ₹5000.0
```

**Real-World Example:**  
A `User` class in an e-commerce app representing customers.

---

### 🔹 2. Inheritance  
**Definition:**  
Inheritance allows one class to inherit fields and methods from another. Promotes **code reuse** and **hierarchical classification**.

**Advanced Concept:**  
- `super` keyword to refer to parent class constructors/methods.  
- Multi-level inheritance.

**Example:**
```java
class Vehicle {
    int speed = 60;
    void start() {
        System.out.println("Vehicle started");
    }
}

class Car extends Vehicle {
    void display() {
        System.out.println("Speed: " + speed + " km/h");
    }
}

public class Main {
    public static void main(String[] args) {
        Car myCar = new Car();
        myCar.start();
        myCar.display();
    }
}
```

**Output:**
```
Vehicle started  
Speed: 60 km/h
```

**Real-World Example:**  
`Employee` → `Manager`, `Developer` in a payroll system.

---

### 🔹 3. Polymorphism  
**Definition:**  
Polymorphism = “**one name, many forms**.” A method behaves differently based on the object or parameters.

**Types:**
- Compile-time (Method Overloading)
- Runtime (Method Overriding)

**Advanced Concept:**  
- Upcasting and dynamic method dispatch.  
- Interfaces and loose coupling.

**Example:**
```java
class Notification {
    void alert() {
        System.out.println("General notification");
    }
}

class Email extends Notification {
    void alert() {
        System.out.println("Email notification");
    }
}

class SMS extends Notification {
    void alert() {
        System.out.println("SMS notification");
    }
}

public class Main {
    public static void main(String[] args) {
        Notification n;
        n = new Email();
        n.alert();
        n = new SMS();
        n.alert();
    }
}
```
**Output:**
```
Email notification  
SMS notification
```

**Real-World Example:**  
Payment gateway interface with different implementations like UPI, Credit Card, and PayPal.

---

### 🔹 4. Encapsulation  
**Definition:**  
Encapsulation is the bundling of data (variables) and behavior (methods). It restricts **direct access** to internal state and uses **getters/setters**.

**Advanced Concept:**  
- JavaBeans convention: private fields with public getter/setter.  
- Ensures immutability using final + no setters.

**Example:**
```java
class Student {
    private int age;

    public void setAge(int a) {
        if (a > 0)
            age = a;
    }

    public int getAge() {
        return age;
    }
}

public class Main {
    public static void main(String[] args) {
        Student s = new Student();
        s.setAge(20);
        System.out.println("Student age: " + s.getAge());
    }
}
```
**Output:**
```
Student age: 20
```

**Real-World Example:**  
`BankAccount` class hides balance and restricts access via deposit/withdraw methods.

---

### 🔹 5. Abstraction  
**Definition:**  
Abstraction hides unnecessary internal details and shows only essential features to the user.

**Advanced Concept:**  
- Implemented using **abstract classes** and **interfaces**.  
- Promotes **loose coupling** and **contract-based design**.

**Example using Interface:**
```java
interface Shape {
    void draw();
}

class Rectangle implements Shape {
    public void draw() {
        System.out.println("Drawing Rectangle");
    }
}

public class Main {
    public static void main(String[] args) {
        Shape s = new Rectangle();
        s.draw();
    }
}
```
**Output:**
```
Drawing Rectangle
```

**Real-World Example:**  
In an ATM machine, the user only interacts with buttons/screen (abstracted), not the backend logic.

---

Would you like me to now generate this as a PDF document for easy download and revision?
