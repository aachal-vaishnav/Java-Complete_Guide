
# 📌 8. Encapsulation & Inheritance  

## **Topics Covered:**  
1. Intro to OOPs Principles  
2. What is Encapsulation  
3. Import & Packages  
4. Access Modifiers  
5. Getter & Setter Methods  
6. What is Inheritance  
7. Types of Inheritance  
8. `Object` Class  
9. `equals()` and `hashCode()` Methods  
10. Nested & Inner Classes  

---

## **8.1 Intro to OOPs Principle**  
📌 **Object-Oriented Programming (OOP)** revolves around real-world entities like **objects & classes**.  

✅ **Four Pillars of OOP:**  
1️⃣ **Encapsulation** → Hiding internal data & exposing only necessary details.  
2️⃣ **Inheritance** → Reusing properties/methods from another class.  
3️⃣ **Polymorphism** → Using methods differently based on objects.  
4️⃣ **Abstraction** → Showing only essential features & hiding complexity.  

---

## **8.2 What is Encapsulation?**  
📌 **Encapsulation ensures controlled access to object properties.**  

✅ **Encapsulation Benefits:**  
✔ **Data Hiding:** Restricts direct access to fields via `private` keyword.  
✔ **Access Modifiers:** Uses `private`, `public`, `protected` to control visibility.  
✔ **Getter/Setter:** Public methods for controlled property access.  
✔ **Enhances Modularity:** Keeps classes separate & reduces dependency.  

✅ **Example Using Encapsulation:**  
```java
class BankAccount {
    private double balance;

    public double getBalance() { return balance; } // Getter
    public void setBalance(double amount) { // Setter
        if (amount >= 0) this.balance = amount;
    }
}
```

---

## **8.3 Import & Packages**  
📌 **Packages organize Java classes & prevent name conflicts.**  

✅ **Types of Import Statements:**  
✔ **Single Class Import:** `import java.util.List;`  
✔ **Wildcard Import:** `import java.util.*;`  
✔ **Static Import:** `import static java.lang.Math.PI;`  

✅ **Example:**  
```java
package com.example.utils; // Package declaration
import java.util.Scanner;  // Importing Scanner class
```

---

## **8.4 Access Modifiers**  
📌 **Java provides four access levels for variables, methods & classes.**  

| **Modifier**  | **Class-Level** | **Within Package** | **Outside Package** | **Subclass Access** |
|--------------|---------------|-----------------|-----------------|----------------|
| `public`     | ✅ Yes        | ✅ Yes         | ✅ Yes         | ✅ Yes         |
| `protected`  | ❌ No        | ✅ Yes         | ❌ No         | ✅ Yes         |
| `default`    | ❌ No        | ✅ Yes         | ❌ No         | ❌ No         |
| `private`    | ❌ No        | ❌ No         | ❌ No         | ❌ No         |

✅ **Example Usage:**  
```java
class Employee {
    private String name; // Private access
    protected int salary; // Protected access
    public void display() { System.out.println(name + ": " + salary); } // Public method
}
```

---

## **8.5 Getter & Setter Methods**  
📌 **Used to access private fields safely.**  

✅ **Getter Example:**  
```java
public String getName() { return name; }
```

✅ **Setter Example (With Validation):**  
```java
public void setSalary(int amount) {
    if (amount >= 30000) this.salary = amount;
}
```

---

## **🔹 Tasks for Practice:**  
✔ **Create `com.example.geometry` package with Circle & Rectangle classes**  
✔ **Define a `BankAccount` class with private attributes & validation**  
✔ **Design an `Employee` class using package-private methods**  

---

## **8.6 What is Inheritance?**  
📌 **Inheritance allows a subclass to inherit properties/methods from a superclass.**  

✅ **Example:**  
```java
class Animal { void makeSound() { System.out.println("Animal makes sound"); } }
class Dog extends Animal { void bark() { System.out.println("Dog barks"); } }
```

---

## **8.7 Types of Inheritance**  
📌 **Java supports multiple inheritance types via class extensions or interfaces.**  

✔ **Single Inheritance** → `Child` inherits from `Parent`.  
✔ **Multi-level Inheritance** → `Grandchild` inherits from `Child`, which inherits from `Parent`.  
✔ **Hierarchical Inheritance** → Multiple subclasses inherit from one parent.  
✔ **Multiple Inheritance via Interfaces** → Java doesn't allow multiple class inheritance, but supports via interfaces.  

✅ **Example:**  
```java
class A { void show() { System.out.println("Class A"); } }
class B extends A { void display() { System.out.println("Class B"); } }
```

---

## **8.8 `Object` Class**  
📌 **Root class for all Java classes, providing fundamental methods.**  

| **Method**      | **Purpose**                                      |
|----------------|----------------------------------------------|
| `equals()`     | Compares objects logically                  |
| `hashCode()`   | Generates hash code for collections         |
| `toString()`   | Returns string representation of object     |
| `getClass()`   | Retrieves runtime class of an object       |

✅ **Example:**  
```java
class Example {
    @Override
    public String toString() { return "Custom Object"; }
}
Example obj = new Example();
System.out.println(obj); // Calls toString()
```

---

## **8.9 Equals & HashCode Methods**  
📌 **Used to compare objects and store them efficiently in collections.**  

✅ **Example Overriding `equals()` & `hashCode()`:**  
```java
class Person {
    String name;
    @Override
    public boolean equals(Object obj) {
        if (obj instanceof Person p) return name.equals(p.name);
        return false;
    }
    @Override
    public int hashCode() { return name.hashCode(); }
}
```

---

## **8.10 Nested & Inner Classes**  
📌 **Encapsulate logic inside another class for better organization.**  

✔ **Static Nested Class** → No reference to outer class instance.  
✔ **Inner Class** → Can access outer class members, including private ones.  
✔ **Anonymous Inner Class** → Used for one-time functionality.  

✅ **Example Static Nested Class:**  
```java
class Outer {
    static class Nested {
        void show() { System.out.println("Inside Nested Class"); }
    }
}
Outer.Nested obj = new Outer.Nested();
```

✅ **Example Inner Class:**  
```java
class Outer {
    class Inner {
        void display() { System.out.println("Inside Inner Class"); }
    }
}
Outer obj = new Outer();
Outer.Inner innerObj = obj.new Inner();
```

---

## **🔹 Tasks for Practice:**  
✔ **Create a base class `LibraryItem` with subclasses `Book`, `Magazine`, `DVD`**  
✔ **Override `equals()` & `hashCode()` methods in a `Person` class**  
✔ **Create an `ArrayOperations` class with a static nested `Statistics` class**  

---

