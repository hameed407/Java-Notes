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

Would you like a **Java program that demonstrates all these types in one place**?
