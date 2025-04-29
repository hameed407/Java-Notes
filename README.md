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

### 🔹 **1. Class and Object**
**Definition:**  
A **class** is a blueprint or template that defines the structure and behavior (fields and methods) of objects.  
An **object** is an instance of a class that holds actual values and can invoke methods.

**Example:**
```java
class Car {
    String color;
    void display() {
        System.out.println("Car color is " + color);
    }
}

public class Main {
    public static void main(String[] args) {
        Car myCar = new Car();
        myCar.color = "Red";
        myCar.display();
    }
}
```

**Output:**
```
Car color is Red
```

---

### 🔹 **2. Inheritance**
**Definition:**  
Inheritance allows one class (child) to inherit fields and methods from another class (parent).  
It promotes code reuse and establishes a parent-child relationship between classes.

**Example:**
```java
class Animal {
    void sound() {
        System.out.println("Animal makes sound");
    }
}

class Dog extends Animal {
    void sound() {
        System.out.println("Dog barks");
    }
}

public class Main {
    public static void main(String[] args) {
        Dog d = new Dog();
        d.sound();
    }
}
```

**Output:**
```
Dog barks
```

---

### 🔹 **3. Polymorphism**
**Definition:**  
Polymorphism means "one interface, many forms"—it allows methods to behave differently based on the object.  
It is achieved via **method overloading** (compile-time) and **method overriding** (runtime).

**Example (Runtime Polymorphism):**
```java
class Animal {
    void sound() {
        System.out.println("Animal sound");
    }
}

class Cat extends Animal {
    void sound() {
        System.out.println("Cat meows");
    }
}

class Dog extends Animal {
    void sound() {
        System.out.println("Dog barks");
    }
}

public class Main {
    public static void main(String[] args) {
        Animal a1 = new Cat();
        Animal a2 = new Dog();
        a1.sound();
        a2.sound();
    }
}
```

**Output:**
```
Cat meows  
Dog barks
```

---

### 🔹 **4. Encapsulation**
**Definition:**  
Encapsulation is the practice of wrapping data (variables) and code (methods) together as a single unit.  
It restricts direct access to some of an object’s components using **private** fields and **public getters/setters**.

**Example:**
```java
class Person {
    private String name;

    public void setName(String name) {
        this.name = name;
    }

    public String getName() {
        return name;
    }
}

public class Main {
    public static void main(String[] args) {
        Person p = new Person();
        p.setName("John");
        System.out.println(p.getName());
    }
}
```

**Output:**
```
John
```

---

### 🔹 **5. Abstraction**
**Definition:**  
Abstraction hides complex internal implementation details and only shows essential features to the user.  
It is implemented using **abstract classes** and **interfaces** in Java.

**Example using Abstract Class:**
```java
abstract class Shape {
    abstract void draw();
}

class Circle extends Shape {
    void draw() {
        System.out.println("Drawing Circle");
    }
}

public class Main {
    public static void main(String[] args) {
        Shape s = new Circle();
        s.draw();
    }
}
```

**Output:**
```
Drawing Circle
```

---

Would you like me to generate this into a downloadable **PDF cheat sheet** now?
