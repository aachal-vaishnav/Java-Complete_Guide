
# 📌 3. Data Types, Variables & Input  

## **3.1 What are Variables?**  
✅ Variables are **containers** used for **storing data values**.  
✅ Every variable has a **name, type, and value**.  
✅ Example in Java:  

```java
int age = 25; // 'age' is a variable storing 25
```

---

## **3.1 Memory Allocation**  
📌 The **Java Virtual Machine (JVM)** allocates memory for variables in different sections:  
🔹 **Stack Memory** → Stores local variables inside methods.  
🔹 **Heap Memory** → Stores objects and global variables.  

---

## **3.1 Variable Declaration**  
🔹 **Declaring a variable** means **reserving space in memory**:  
```java
int number; // Declaring a variable 'number' of type int
number = 10; // Assigning a value to the variable
```
✅ **Declaration** → Defines the variable name & type.  
✅ **Initialization** → Assigns a value to the variable.  

---

## **3.2 Data Types**  
📌 Java has **two types of data types**:  
🔹 **Primitive Data Types** (Basic types)  
🔹 **Reference Data Types** (Objects & arrays)  

### **Primitive Data Types in Java**  
| **Type**    | **Size**  | **Example**    |  
|------------|---------|--------------|  
| `byte`     | 1 byte  | `byte b = 100;` |  
| `short`    | 2 bytes | `short s = 20000;` |  
| `int`      | 4 bytes | `int num = 500000;` |  
| `long`     | 8 bytes | `long bigNum = 9223372036854775807L;` |  
| `float`    | 4 bytes | `float pi = 3.14f;` |  
| `double`   | 8 bytes | `double rate = 99.99;` |  
| `char`     | 2 bytes | `char letter = 'A';` |  
| `boolean`  | 1 bit   | `boolean isJavaFun = true;` |  

---

## **3.3 Naming Conventions**  
📌 **Rules for naming variables in Java**:  

✅ **camelCase** → Start with a lowercase letter. Capitalize first letter of each word.  
Example: `myVariableName`  

✅ **snake_case** → Use lowercase letters & separate words with `_`.  
Example: `my_variable_name`  

✅ **kebab-case** → All lowercase letters, separate words with `-`.  
Example: `my-variable-name`  

✅ **Good Naming Practice** →  
✔ Use **meaningful names** → `age`, `firstName`, `isMarried`  
✔ **Avoid very long names**  
✔ **Do not use Java keywords**  

---

## **3.3 Java Identifier Rules**  
📌 Identifiers are names for **variables, methods, classes, etc.**  

✅ Allowed characters → **Alphanumeric (`A-Z`, `a-z`, `0-9`), `$`, `_`**  
✅ Cannot use **keywords or reserved words**  
✅ **Cannot start with a digit (`0-9`)**  
✅ **Case-sensitive** (`name` ≠ `Name`)  
✅ No length limit, but **4–15 letters is optimal**  

---

## **3.4 Literals**  
📌 **Literals** are fixed values assigned to variables.  

✅ **Integer Literal** → `int x = 100;`  
✅ **Floating Point Literal** → `double pi = 3.14;`  
✅ **Character Literal** → `char letter = 'J';`  
✅ **Boolean Literal** → `boolean isActive = true;`  
✅ **String Literal** → `String name = "Java";`  

---

## **3.5 Keywords**  
📌 **Java has 50+ reserved keywords** that **cannot be used as variable names**.  

✅ `public`, `static`, `class`, `void`, `int`, `boolean`, `if`, `else`, `return`, etc.  

---

## **3.6 Escape Sequences**  
📌 Special characters in Java strings:  

✅ `\n` → New Line  
✅ `\t` → Tab Space  
✅ `\"` → Double Quote  
✅ `\\` → Backslash  

Example:  
```java
System.out.println("Java is awesome!\nLet's learn it.");
```
✅ Expected Output:  
```
Java is awesome!  
Let's learn it.
```

---

## **3.7 User Input**  
📌 **Using Scanner class** to take input:  

```java
import java.util.Scanner;

public class InputExample {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter your name: ");
        String name = scanner.nextLine();
        System.out.println("Welcome " + name + " to KG Coding!");
    }
}
```

✅ Output Example:  
```
Enter your name: John  
Welcome John to KG Coding!
```

---

## **3.8 Type Conversion and Casting**  
📌 **Implicit Conversion (Widening)**  
✅ Smaller type **automatically converts** to a larger type.  
```java
int num = 10;
double doubleNum = num; // No explicit conversion needed
```

📌 **Explicit Conversion (Narrowing/Casting)**  
✅ **Larger type** needs **explicit conversion** to a smaller type.  
```java
double pi = 3.14;
int roundedPi = (int) pi; // Casting required
```

---

## 🔥 **Revision Summary**  
✅ **Variables & Memory Allocation**  
✅ **Primitive & Reference Data Types**  
✅ **Naming Conventions & Java Identifiers**  
✅ **Literals, Keywords & Escape Sequences**  
✅ **User Input using Scanner Class**  
✅ **Type Conversion & Casting**  

---

## ✅ **Tasks:**  
1️⃣ **Show the following patterns using a single print statement:**  
```java
System.out.println("*\n**\n***\n****\n*****");
```

2️⃣ **Create a program that takes a user's name and welcomes them:**  
```java
System.out.print("Welcome " + name + " to KG Coding!");
```

3️⃣ **Create a program to add two numbers:**  
```java
Scanner sc = new Scanner(System.in);
System.out.print("Enter first number: ");
int num1 = sc.nextInt();
System.out.print("Enter second number: ");
int num2 = sc.nextInt();
System.out.println("Sum: " + (num1 + num2));
```

---

