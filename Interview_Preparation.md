

## **1️⃣ Java Basics & OOP Concepts**  

### **Q1: What are the four pillars of OOP?**  
✅ **Answer:**  
- **Encapsulation** → Hides internal details and exposes only necessary functionalities.  
- **Inheritance** → Allows a subclass to inherit from a superclass.  
- **Polymorphism** → Enables objects to take different forms (Method Overloading & Overriding).  
- **Abstraction** → Hides implementation details and exposes only essential behavior.  

✅ **Example:**  
```java
class Animal {
    void sound() { System.out.println("Animal makes sound"); }
}
class Dog extends Animal {
    void sound() { System.out.println("Dog barks"); } // Method overriding
}
```

---

### **Q2: What is the difference between Method Overloading and Method Overriding?**  
✅ **Answer:**  
| Feature  | **Method Overloading** | **Method Overriding** |
|----------|----------------------|----------------------|
| **Definition** | Same method name but different parameters | Same method name, same parameters |
| **Where it occurs** | Same class | Parent & Child classes |
| **Return Type** | Can be different | Must be the same or subtype |
| **Execution** | Compile-time polymorphism | Run-time polymorphism |

✅ **Example Overloading:**  
```java
class MathOperations {
    int add(int a, int b) { return a + b; }
    double add(double a, double b) { return a + b; } // Overloading
}
```

✅ **Example Overriding:**  
```java
class Parent {
    void show() { System.out.println("Parent Method"); }
}
class Child extends Parent {
    @Override
    void show() { System.out.println("Child Method"); } // Overriding
}
```

---

## **2️⃣ Data Types, Variables & Operators**  

### **Q3: What is Autoboxing & Unboxing in Java?**  
✅ **Answer:**  
- **Autoboxing** → Automatic conversion of **primitive data types** to their **wrapper classes** (int → Integer).  
- **Unboxing** → Automatic conversion of **wrapper classes** back to **primitive types** (Integer → int).  

✅ **Example:**  
```java
Integer num = 10;  // Autoboxing
int x = num;  // Unboxing
```

---

### **Q4: What is the difference between `==` and `.equals()` in Java?**  
✅ **Answer:**  
- `==` → **Compares object references** (memory addresses).  
- `.equals()` → **Compares object content** (actual values).  

✅ **Example:**  
```java
String s1 = new String("Hello");
String s2 = new String("Hello");
System.out.println(s1 == s2);      // Output: false (Different objects)
System.out.println(s1.equals(s2)); // Output: true (Same content)
```

---

## **3️⃣ Loops, Methods & Arrays**  

### **Q5: What is the difference between an Array and ArrayList?**  
✅ **Answer:**  
| Feature   | **Array** | **ArrayList** |
|-----------|----------|--------------|
| **Size** | Fixed | Dynamic |
| **Memory Allocation** | Stored in contiguous memory | Uses dynamic resizing |
| **Performance** | Fast | Slower (due to resizing overhead) |

✅ **Example Using `ArrayList`:**  
```java
List<Integer> numbers = new ArrayList<>();
numbers.add(10); numbers.add(20);
System.out.println(numbers); // Output: [10, 20]
```

---

### **Q6: How do you find the largest element in an array?**  
✅ **Answer:**  
```java
int[] numbers = {10, 25, 3, 50, 15};
int max = Arrays.stream(numbers).max().getAsInt();
System.out.println("Largest: " + max); // Output: 50
```

---

## **4️⃣ Exception & File Handling**  

### **Q7: What is the difference between Checked & Unchecked Exceptions?**  
✅ **Answer:**  
| Feature   | **Checked Exception** | **Unchecked Exception** |
|-----------|----------------------|----------------------|
| **Definition** | Must be handled with `try-catch` or `throws` | Occurs at runtime, handling optional |
| **Examples** | `IOException`, `SQLException` | `NullPointerException`, `ArithmeticException` |

✅ **Example Handling `IOException`:**  
```java
try {
    FileReader file = new FileReader("test.txt");
} catch (IOException e) {
    System.out.println("File not found!");
}
```

---

## **5️⃣ Collections & Generics**  

### **Q8: What is the difference between `ArrayList` and `LinkedList`?**  
✅ **Answer:**  
| Feature  | **ArrayList** | **LinkedList** |
|----------|------------|--------------|
| **Performance** | Faster (random access) | Slower (traversal required) |
| **Memory Usage** | Less | More (extra memory for links) |

✅ **Example Using `LinkedList`:**  
```java
List<Integer> list = new LinkedList<>();
list.add(10); list.add(20);
System.out.println(list); // Output: [10, 20]
```

---

## **6️⃣ Multi-threading & Executor Service**  

### **Q9: What are the states of a thread?**  
✅ **Answer:**  
- **New** → Created but not started  
- **Runnable** → Ready to execute  
- **Running** → Actively executing  
- **Blocked/Waiting** → Waiting for resources  
- **Terminated** → Execution completed  

✅ **Example Checking Thread State:**  
```java
Thread t = new Thread();
System.out.println(t.getState()); // Output: NEW
```

---

### **Q10: What is the difference between `Runnable` & `Callable` in Java?**  
✅ **Answer:**  
| Feature  | **Runnable** | **Callable** |
|----------|------------|--------------|
| **Return Type** | `void` | `Future<T>` |
| **Checked Exceptions** | Not Allowed | Allowed |

✅ **Example Using `Callable`:**  
```java
ExecutorService executor = Executors.newFixedThreadPool(3);
Callable<Integer> task = () -> 5 * 5;
Future<Integer> future = executor.submit(task);
System.out.println(future.get()); // Output: 25
executor.shutdown();
```

---

## **7️⃣ Functional Programming & Streams**  

### **Q11: What is the difference between `map()` & `filter()` in Streams?**  
✅ **Answer:**  
- **map()** → Transforms each element.  
- **filter()** → Removes elements that don't meet a condition.  

✅ **Example Using `map()` & `filter()`:**  
```java
List<Integer> numbers = Arrays.asList(1, 2, 3, 4, 5);
List<Integer> squared = numbers.stream().map(n -> n * n).collect(Collectors.toList());
List<Integer> evens = numbers.stream().filter(n -> n % 2 == 0).collect(Collectors.toList());
System.out.println(squared); // Output: [1, 4, 9, 16, 25]
System.out.println(evens); // Output: [2, 4]
```

---
