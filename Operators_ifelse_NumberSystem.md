
# 📌 4. Operators, If-else & Number System  

## **Topics Covered:**  
1. Assignment Operator  
2. Arithmetic Operators  
3. Order of Operation  
4. Shorthand Operators  
5. Unary Operators  
6. If-else  
7. Relational Operators  
8. Logical Operators  
9. Operator Precedence  
10. Intro to Number System  
11. Intro to Bitwise Operators  

---

## **4.1 Assignment Operator**  
📌 **Assigns the right-hand operand's value to the left-hand operand.**  
Example:  
```java
int a = 5; // a is assigned the value 5
```

---

## **🔹 Task:**  
✅ **Swap two numbers using assignment operator**  
```java
int a = 5, b = 10;
a = a + b;  
b = a - b;  
a = a - b;
System.out.println("a = " + a + ", b = " + b);
```

---

## **4.2 Arithmetic Operators**  
📌 **Perform mathematical operations**  

| **Operator** | **Meaning**       | **Example**       | **Result** |
|-------------|------------------|-----------------|------------|
| `+`         | Addition         | `5 + 3`        | `8`        |
| `-`         | Subtraction      | `5 - 3`        | `2`        |
| `*`         | Multiplication   | `5 * 3`        | `15`       |
| `/`         | Division         | `6 / 3`        | `2`        |
| `%`         | Modulus (Remainder) | `5 % 3`        | `2`        |

---

## **🔹 Task:**  
✅ **Create a program that performs all arithmetic operations**  
```java
int x = 10, y = 5;
System.out.println("Addition: " + (x + y));
System.out.println("Subtraction: " + (x - y));
System.out.println("Multiplication: " + (x * y));
System.out.println("Division: " + (x / y));
System.out.println("Modulus: " + (x % y));
```

---

## **4.3 Order of Operation (Operator Precedence)**  
✅ **Multiplication & Division (`* / %`) happen before Addition & Subtraction (`+ -`)**  
✅ **Parentheses `()` override default precedence**  

Example:  
```java
int result = 10 + 5 * 2; // result = 20, NOT 30!
```

---

## **4.4 Shorthand Operators**  
✅ **Shorthand assignment operators:**  
```java
int x = 5;
x += 10; // Same as x = x + 10;
```

| **Operator** | **Equivalent To** |
|-------------|------------------|
| `+=`        | `a = a + b`      |
| `-=`        | `a = a - b`      |
| `*=`        | `a = a * b`      |
| `/=`        | `a = a / b`      |
| `%=`        | `a = a % b`      |

---

## **4.5 Unary Operators**  
📌 **Works on a single operand**  

| **Operator** | **Meaning**       | **Example**        |
|-------------|------------------|------------------|
| `+`         | Positive Sign    | `int x = +10;`  |
| `-`         | Negative Sign    | `int x = -10;`  |
| `++`        | Increment        | `x++` or `++x`  |
| `--`        | Decrement        | `x--` or `--x`  |

---

## **🔹 Task:**  
✅ **Create a program to calculate product of two floating points numbers**  
```java
float num1 = 3.5f, num2 = 2.5f;
float product = num1 * num2;
System.out.println("Product: " + product);
```

---

## **4.6 If-else Statements**  
📌 **Conditional statements control program flow**  

✅ Basic Syntax:  
```java
if (condition) {
    // Code executes if condition is true
} else {
    // Code executes if condition is false
}
```

✅ Example:  
```java
int age = 18;
if (age >= 18) {
    System.out.println("You are an adult.");
} else {
    System.out.println("You are a minor.");
}
```

---

## **4.7 Relational & Logical Operators**  
📌 **Compare values & check conditions**  

| **Operator** | **Meaning**       | **Example**    |
|-------------|------------------|---------------|
| `==`        | Equal to         | `x == y`     |
| `!=`        | Not Equal        | `x != y`     |
| `>`         | Greater than     | `x > y`      |
| `<`         | Less than        | `x < y`      |
| `&&`        | AND              | `(x > 0 && y > 0)` |
| `||`        | OR               | `(x > 0 || y > 0)` |
| `!`         | NOT              | `!(x > 0)`   |

---

## **🔹 Task:**  
✅ **Create a program to check if a number is positive, negative, or zero**  
```java
int num = 5;
if (num > 0) {
    System.out.println("Positive");
} else if (num < 0) {
    System.out.println("Negative");
} else {
    System.out.println("Zero");
}
```

---

## **4.10 Intro to Number System**  
📌 **Understanding Binary, Octal & Hexadecimal**  

| **System** | **Base** | **Digits Used**             |
|-----------|--------|--------------------------|
| **Decimal** | `10`   | `0-9`                    |
| **Binary**  | `2`    | `0,1`                    |
| **Octal**   | `8`    | `0-7`                    |
| **Hex**     | `16`   | `0-9, A-F`               |

✅ **Example of Binary to Decimal Conversion:**  
```java
int binaryNumber = 0b1101; // Decimal equivalent = 13
System.out.println("Decimal: " + binaryNumber);
```

---

## **4.11 Bitwise Operators**  
## **Bitwise Operators - Perform Bit-Level Operations**  
Bitwise operators work **directly on binary representations of numbers**, manipulating individual bits.  

<table>
  <tr>
    <th>Operator</th>
    <th>Meaning</th>
    <th>Example</th>
    <th>Explanation</th>
  </tr>
  <tr>
    <td><code>&</code></td>
    <td>Bitwise AND</td>
    <td><code>x & y</code></td>
    <td>Sets bits to <code>1</code> if both bits are <code>1</code></td>
  </tr>
  <tr>
    <td><code>|</code></td>
    <td>Bitwise OR</td>
    <td><code>x | y</code></td>
    <td>Sets bits to <code>1</code> if any bit is <code>1</code></td>
  </tr>
  <tr>
    <td><code>^</code></td>
    <td>Bitwise XOR</td>
    <td><code>x ^ y</code></td>
    <td>Sets bits to <code>1</code> if bits are different</td>
  </tr>
  <tr>
    <td><code>~</code></td>
    <td>Bitwise NOT</td>
    <td><code>~x</code></td>
    <td>Inverts all bits (0 → 1, 1 → 0)</td>
  </tr>
  <tr>
    <td><code>&lt;&lt;</code></td>
    <td>Left Shift</td>
    <td><code>x << 2</code></td>
    <td>Shifts bits left, filling zeros</td>
  </tr>
  <tr>
    <td><code>&gt;&gt;</code></td>
    <td>Right Shift</td>
    <td><code>x >> 2</code></td>
    <td>Shifts bits right, filling zeros or ones</td>
  </tr>
</table>

### **✅ Examples of Bitwise Operators**  

```java
int a = 5;  // Binary: 0101
int b = 3;  // Binary: 0011

System.out.println("AND: " + (a & b));   // 0101 & 0011 → 0001 → 1
System.out.println("OR: " + (a | b));    // 0101 | 0011 → 0111 → 7
System.out.println("XOR: " + (a ^ b));   // 0101 ^ 0011 → 0110 → 6
System.out.println("NOT A: " + (~a));    // ~0101 → Inverts → -6
System.out.println("Left Shift A: " + (a << 2));  // 0101 << 2 → 10100 → 20
System.out.println("Right Shift A: " + (a >> 2)); // 0101 >> 2 → 0001 → 1



---

## ✅ **Practice Questions**  
✔ Write a program to **swap two numbers**  
✔ Check if a number is **even/odd using bitwise operator**  
✔ Convert **Fahrenheit to Celsius** using formula  
✔ Find **largest among three numbers** using `if-else`  

---
