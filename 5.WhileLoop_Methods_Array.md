
# 📌 5. While Loop, Methods & Arrays  

## **Topics Covered:**  
1. Comments  
2. While Loop  
3. Methods  
4. Return Statement  
5. Arguments  
6. Arrays  
7. 2D Arrays  

---

## **5.1 Java Comments**  
📌 **Used to add notes in Java code** for better readability.  

✅ **Single-line comment:**  
```java
// This is a single-line comment
```

✅ **Multi-line comment:**  
```java
/* This is a 
multi-line comment */
```

✅ **Java Documentation comment (for generating docs):**  
```java
/** This is a documentation comment */
```

---

## **5.2 What is a Loop?**  
🔹 **Loops allow repeated execution of code based on a condition.**  
🔹 **Useful for automating repetitive tasks.**  

✅ **Types of Loops in Java:**  
- `for` Loop  
- `while` Loop  
- `do-while` Loop  

✅ **Iterations:** Number of times the loop runs.  

---

## **5.2 While Loop**  
📌 **Executes a block of code repeatedly while a condition is true.**  

✅ **Syntax:**  
```java
while (condition) {
    // Loop body (executes while condition is true)
}
```

✅ **Example:**  
```java
int i = 1;
while (i <= 5) {
    System.out.println("Iteration: " + i);
    i++; // Update condition (avoid infinite loops)
}
```

---

## **5.3 What are Methods/Functions?**  
📌 **Functions (also called Methods) are reusable blocks of code that perform specific tasks.**  

✅ **DRY Principle:** *"Don't Repeat Yourself" → Code reusability*  
✅ **Naming Rules:** Follow `camelCase` (e.g., `myFunction()`)  

✅ **Example Function:**  
```java
void greet() {
    System.out.println("Hello, Java!");
}
```

---

## **5.3 Method Syntax**  
📌 **Basic structure of a method:**  

```java
returnType methodName(parameters) {
    // Method body
}
```

✅ **Example Method with Parameters & Return:**  
```java
int add(int a, int b) {
    return a + b; // Returning sum
}
```

---

## **5.4 Return Statement**  
📌 **Returns a value from a method to the caller.**  

✅ **Example:**  
```java
int square(int num) {
    return num * num; // Returns squared value
}
```

✅ **Return Statement Immediately Ends Method Execution!**  
✅ **Prefer returning values over modifying global variables.**  

---

## **5.5 Arguments vs Parameters**  
📌 **Key differences:**  

✅ **Parameters → Input values inside method definition.**  
✅ **Arguments → Actual values passed when calling the method.**  

✅ **Example:**  
```java
void greet(String name) {  // 'name' is a parameter
    System.out.println("Welcome, " + name);
}

// Function call
greet("John"); // "John" is an argument
```

---

## **🔹 Tasks for Practice:**  
✔ **Multiplication Table of a Given Number**  
✔ **Sum of Odd Numbers from 1 to N**  
✔ **Factorial of a Given Number**  
✔ **Sum of Digits of an Integer**  
✔ **Least Common Multiple (LCM) of Two Numbers**  
✔ **Greatest Common Divisor (GCD) of Two Numbers**  
✔ **Check Whether a Number is Prime**  
✔ **Reverse the Digits of a Number**  
✔ **Print Fibonacci Series**  
✔ **Check if a Number is an Armstrong Number**  
✔ **Verify if a Number is a Palindrome**  

---

## **5.6 What is an Array?**  
📌 **An Array is a collection of multiple values stored in a single variable.**  
📌 **Indexing starts at `0`.**  

✅ **Example of Declaring an Array:**  
```java
int[] numbers = {10, 20, 30, 40, 50};
System.out.println(numbers[2]); // Accessing element (Output → 30)
```

---

## **5.6 Array Memory Allocation**  
📌 **Arrays store values in contiguous memory locations.**  
✅ **Each element has a unique index for access.**  

✅ **Example Memory Representation:**  
```
Index   →  0    1    2    3    4  
Value   → 10   20   30   40   50  
```

---

## **5.7 2D Arrays**  
📌 **Arrays with multiple rows & columns.**  
✅ **Syntax:**  
```java
int[][] matrix = {
    {1, 2, 3},
    {4, 5, 6},
    {7, 8, 9}
};
```

✅ **Accessing Elements:**  
```java
System.out.println(matrix[1][2]); // Output → 6
```

---

## **🔹 More Array-Based Tasks:**  
✔ **Find sum & average of all elements in an array**  
✔ **Find occurrences of an element in an array**  
✔ **Find max & min values in an array**  
✔ **Check if an array is sorted**  
✔ **Reverse an array**  
✔ **Check if an array is palindrome**  
✔ **Merge two sorted arrays**  
✔ **Search an element in a 2D array**  
✔ **Find sum & average of 2D array elements**  
✔ **Find sum of diagonal elements**  

---

## ✅ **Revision Summary**  
✔ **Comments (`//, /* */, /** */`)**  
✔ **Loops (`while, for, do-while`)**  
✔ **Methods, Arguments & Return Statement**  
✔ **Arrays (`1D & 2D Arrays`)**  

---
