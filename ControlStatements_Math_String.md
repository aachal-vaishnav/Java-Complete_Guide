
# 📌 7. Control Statements, Math & String  

## **Topics Covered:**  
1. Ternary Operator  
2. Switch Statement  
3. Loops (`do-while, for, for-each`)  
4. Using `break` & `continue`  
5. Recursion  
6. Random Numbers & Math Class  
7. Don't Learn Syntax  
8. `toString()` Method  
9. `String` Class  
10. `StringBuffer` vs `StringBuilder`  
11. `final` Keyword  

---

## **7.1 Ternary Operator**  
📌 **Shorthand for simple conditional expressions.**  

✅ **Syntax:**  
```java
condition ? expression1 : expression2
```
✅ **Example:**  
```java
int num = 10;
String result = (num % 2 == 0) ? "Even" : "Odd";
System.out.println(result); // Output: Even
```

---

## **7.2 Switch Statement**  
📌 **Efficient alternative for multiple conditions.**  

✅ **Example:**  
```java
int month = 3;
switch (month) {
    case 1: System.out.println("January"); break;
    case 2: System.out.println("February"); break;
    case 3: System.out.println("March"); break;
    default: System.out.println("Invalid month");
}
```

✅ **Enhanced Switch (Java 12+):**  
```java
String day = switch (month) {
    case 1, 2, 3 -> "Winter";
    case 4, 5, 6 -> "Spring";
    default -> "Unknown";
};
```

---

## **🔹 Tasks for Practice:**  
✔ **Find minimum of two numbers**  
✔ **Determine if a number is even or odd**  
✔ **Calculate absolute value**  
✔ **Categorize student score as "High", "Moderate", or "Low" using ternary operator**  
✔ **Print month name based on user input (1-12)**  
✔ **Simple calculator using switch statement**  

---

## **7.3 Loops in Java**  
📌 **Loops allow executing code multiple times efficiently.**  

### **✅ `do-while` Loop:**  
✔ Executes block first, then checks condition.  
✔ Always runs at least **one iteration**.  

```java
int x = 1;
do {
    System.out.println(x);
    x++;
} while (x <= 5);
```

### **✅ `for` Loop:**  
✔ Used when **number of iterations is known**.  
```java
for (int i = 1; i <= 5; i++) {
    System.out.println(i);
}
```

### **✅ `for-each` Loop (Enhanced for loop):**  
✔ Iterates over **arrays or collections** efficiently.  
```java
int[] numbers = {10, 20, 30};
for (int num : numbers) {
    System.out.println(num);
}
```

---

## **7.4 Using `break` & `continue`**  
📌 **Control loop execution.**  

✅ **Break Example:**  
```java
for (int i = 1; i <= 10; i++) {
    if (i == 5) break; // Stops loop
    System.out.println(i);
}
```

✅ **Continue Example:**  
```java
for (int i = 1; i <= 10; i++) {
    if (i % 2 != 0) continue; // Skips odd numbers
    System.out.println(i);
}
```

---

## **🔹 Tasks for Practice:**  
✔ **Password checker using `do-while`**  
✔ **Number guessing game using `do-while`**  
✔ **Multiplication table using `for` loop**  
✔ **Prime number check using `for` loop**  
✔ **Find max value in an integer array using `for-each`**  

---

## **7.5 Recursion**  
📌 **Functions calling themselves to solve problems.**  

✅ **Factorial Example:**  
```java
int factorial(int n) {
    if (n == 1) return 1;
    return n * factorial(n - 1);
}
```

✅ **Fibonacci using Recursion:**  
```java
int fibonacci(int n) {
    if (n <= 1) return n;
    return fibonacci(n - 1) + fibonacci(n - 2);
}
```

---

## **7.6 Random Numbers & Math Class**  
📌 **Provides mathematical operations.**  

✅ **Key Methods:**  
✔ `Math.abs()` → Absolute value  
✔ `Math.ceil()` / `Math.floor()` → Rounding  
✔ `Math.sqrt()` → Square root  
✔ `Math.pow(x, y)` → `x^y`  
✔ `Math.random()` → Generates **random numbers**  

✅ **Example:**  
```java
double randomNum = Math.random() * 100; // Random number between 0-100
System.out.println(randomNum);
```

---

## **7.7 Don't Learn Syntax**  
📌 **Focus on concepts, not memorizing syntax!**  

✅ **Helpful Resources:**  
✔ [Oracle Documentation](https://docs.oracle.com/)  
✔ **Google for quick fixes**  
✔ **AI assistants (like me 😎)**  

---

## **7.8 `toString()` Method**  
📌 **Provides a string representation of objects.**  

✅ **Example:**  
```java
class Student {
    String name; int age;
    public String toString() {
        return "Student{name='" + name + "', age=" + age + "}";
    }
}
```

---

## **7.9 `String` Class**  
📌 **Immutable Strings with useful methods.**  

✅ **Common String Methods:**  
✔ `length()` → String length  
✔ `substring()` → Extract substring  
✔ `equals()` → Compare strings  
✔ `indexOf()` → Find character index  

```java
String str = "Hello Java!";
System.out.println(str.length()); // Output: 12
```

---

## **7.10 `StringBuffer` vs `StringBuilder`**  
📌 **Used for mutable string modifications.**  

| **Feature**       | **StringBuffer** | **StringBuilder** |
|------------------|---------------|----------------|
| **Thread Safe**  | ✅ Yes          | ❌ No         |
| **Performance**  | 🔄 Slower      | ⚡ Faster    |
| **Mutability**   | ✅ Yes          | ✅ Yes       |

---

## **7.11 `final` Keyword**  
📌 **Restricts modification.**  

✅ **Final Variable:**  
```java
final int MAX_USERS = 100;
```

✅ **Final Class:**  
```java
final class Constants { }
```

✅ **Final Method:**  
```java
class Example {
    final void display() { System.out.println("Can't override this method!"); }
}
```

---

## **🔹 More Practice Tasks:**  
✔ **Use `toString()` in a Student class**  
✔ **Concatenate & convert strings to uppercase**  
✔ **Calculate area/circumference using `Math.PI`**  
✔ **Simulate a dice roll using `Math.random()`**  
✔ **Number guessing game with random numbers**  
✔ **Concatenate array of words using `StringBuilder`**  
✔ **Create an object with final fields**  

---
