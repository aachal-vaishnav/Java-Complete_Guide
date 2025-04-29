
# 📌 6. Classes & Objects  

## **Topics Covered:**  
1. Process vs Object-Oriented Approach  
2. Instance Variables and Methods  
3. Declaring and Using Objects  
4. Class vs Object  
5. `this` & `static` Keyword  
6. Constructors & Code Blocks  
7. Stack vs Heap Memory  
8. Primitive vs Reference Types  
9. Variable Scopes  
10. Garbage Collection & `finalize()`  

---

## **6.1 Process vs Object-Oriented Approach**  
📌 **Process-Oriented Programming:**  
🔹 Focuses on **functions & procedures** instead of objects.  
🔹 Data and behavior are **separate**, leading to repetitive code.  

📌 **Object-Oriented Programming (OOP):**  
🔹 Based on **objects & classes** to **group data & behavior together**.  
🔹 Encourages **code reuse, modularity & abstraction**.  
🔹 **Example:**  

```java
class Car {
    String brand;
    void honk() {
        System.out.println("Beep beep!");
    }
}
```

---

## **6.2 Instance Variables & Methods**  
📌 **Instance variables** are variables **associated with objects**, whereas **methods** define behavior.  

```java
class Person {
    String name; // Instance variable
    void greet() { // Instance method
        System.out.println("Hello, " + name);
    }
}
```

---

## **6.3 Declaring Objects**  
✅ **Object creation uses `new` keyword.**  
✅ **Memory allocated in heap & constructor initializes the object.**  

```java
Person p = new Person();
```

📌 **Steps in Object Creation:**  
1️⃣ **Memory Allocation** → Heap memory stores object data.  
2️⃣ **Constructor Invocation** → Initializes the object attributes.  
3️⃣ **Reference Return** → Stores object address in variable.  

---

## **6.4 Class vs Object**  
🔹 **Class** → Blueprint for creating objects.  
🔹 **Object** → Instance of a class with actual data.  

✅ **Example:**  
```java
class Car { 
    String brand; 
} 

Car myCar = new Car(); // Object created!
myCar.brand = "Toyota"; 
System.out.println(myCar.brand); // Output: Toyota
```

---

## **6.5 `this` Keyword**  
📌 `this` refers to the **current object instance**.  

✅ **Uses of `this`:**  
🔹 Refers to **current instance variables**.  
🔹 Calls **another constructor** in the same class (`this()`).  
🔹 Passes the current instance as a method argument.  

Example:  
```java
class Example {
    int x;
    Example(int x) {
        this.x = x; // Referring to instance variable
    }
}
```

---

## **6.5 `static` Keyword**  
📌 `static` members belong **to the class, not objects**.  

✅ **Static Variables:** Shared among all instances.  
✅ **Static Methods:** Can be called **without creating objects**.  

```java
class Counter {
    static int count = 0;
    Counter() {
        count++;
    }
    static void showCount() {
        System.out.println(count);
    }
}
```

---

## **6.6 Constructors**  
📌 **Constructors initialize new objects automatically!**  

🔹 **Default Constructor:** Provided if no explicit constructor is defined.  
🔹 **Parameterized Constructor:** Allows passing values during object creation.  
🔹 **Constructor Chaining:** Calls another constructor in the same class.  

```java
class Example {
    int num;
    Example() { this(100); } // Constructor chaining
    Example(int num) { this.num = num; } 
}
```

---

## **6.6 Code Blocks**  
📌 **Types of Code Blocks:**  
✔ **Instance Block:** Runs every time an object is created.  
✔ **Static Block:** Runs once when the class is loaded.  

```java
class Test {
    static { System.out.println("Static block executed."); }
    { System.out.println("Instance block executed."); }
}
```

---

## **🔹 Tasks for Practice:**  
✔ **Create a `Book` class for a library system**  
✔ **Design a `Course` class with enrollments & max capacity**  

```java
class Book {
    String title, author;
    static int totalBooks;
    Book(String title, String author) {
        this.title = title;
        this.author = author;
        totalBooks++;
    }
    static int getTotalBooks() {
        return totalBooks;
    }
}
```

---

## **6.7 Stack vs Heap Memory**  
📌 **Stack Memory:** Stores **local variables & method calls** (short-lived).  
📌 **Heap Memory:** Stores **objects & class instances** (long-lived).  

✅ **Example Memory Allocation:**  
```
Stack (Method calls)
⬇️
Heap (Objects live here!)
```

---

## **6.8 Primitive vs Reference Types**  
📌 **Difference Between Primitive & Reference Types:**  

✔ **Primitive Types** → Store actual values (`int`, `double`, `boolean`).  
✔ **Reference Types** → Store **addresses** to objects (`String`, `Array`).  

```java
int a = 10;      // Primitive
String str = "Hello"; // Reference type
```

---

## **6.9 Variable Scopes**  
📌 **Scope defines variable visibility.**  

✔ **Local Variables:** Inside method/block  
✔ **Instance Variables:** Inside class but outside methods  
✔ **Static Variables:** Class-level variables  

```java
class Example {
    static int staticVar = 100;  // Static variable
    int instanceVar = 50;        // Instance variable
    void method() {
        int localVar = 10;       // Local variable
    }
}
```

---

## **6.10 Garbage Collection & `finalize()`**  
📌 **Automatic process handled by JVM!**  

✅ **Garbage Collection:** Removes **unused objects** to free memory.  
✅ **Object Eligibility:** If no active references → eligible for garbage collection.  
✅ **`System.gc()` Call:** Suggests JVM to perform garbage collection, but **not guaranteed!**  

```java
class Test {
    protected void finalize() {
        System.out.println("Object is being garbage collected!");
    }
}
Test obj = new Test();
obj = null; // Object eligible for garbage collection
System.gc();
```

⚠ **Note:** `finalize()` is **not reliable**, avoid using it!  

---

## ✅ **Revision Summary**  
✔ **Process vs Object-Oriented Programming**  
✔ **Instance Variables & Methods**  
✔ **Declaring & Using Objects**  
✔ **Class vs Object**  
✔ **`this` & `static` Keywords**  
✔ **Constructors & Code Blocks**  
✔ **Stack vs Heap Memory**  
✔ **Primitive vs Reference Types**  
✔ **Variable Scopes**  
✔ **Garbage Collection & `finalize()`**  

---
