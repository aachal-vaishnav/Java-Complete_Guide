
# 📌 9. Abstraction & Polymorphism  

## **Topics Covered:**  
1. What is Abstraction  
2. `abstract` Keyword  
3. Interfaces  
4. What is Polymorphism  
5. References & Objects (`Upcasting / Downcasting`)  
6. Method / Constructor Overloading  
7. `super` Keyword  
8. Method / Constructor Overriding  
9. `final` Keyword (Revisited)  
10. Pass by Value vs Pass by Reference  

---

## **9.1 What is Abstraction?**  
📌 **Abstraction hides unnecessary implementation details & only shows relevant functionalities.**  

✅ **Benefits of Abstraction:**  
✔ **Simplifies complexity** → Focuses only on required details.  
✔ **Improves security** → Hides internal details from the user.  
✔ **Enhances modularity** → Clear separation of concerns.  

✅ **Example Using Abstraction:**  
```java
abstract class Vehicle {
    abstract void start(); // Abstract method (must be implemented)
}
class Car extends Vehicle {
    void start() { System.out.println("Car starts with a key!"); }
}
```
---

## **9.2 `abstract` Keyword**  
📌 **The `abstract` keyword defines abstract classes & abstract methods.**  

✅ **Features of Abstract Classes:**  
✔ **Cannot be instantiated** → Used as a base class for inheritance.  
✔ **Must have at least one abstract method**  
✔ **Can have normal methods & attributes**  

✅ **Example Using Abstract Methods:**  
```java
abstract class Shape {
    abstract double calculateArea(); // Must be implemented by subclasses
}
class Circle extends Shape {
    double radius;
    Circle(double radius) { this.radius = radius; }
    double calculateArea() { return Math.PI * radius * radius; }
}
```

---

## **9.3 Interfaces**  
📌 **Interfaces define a contract without implementation, ensuring flexibility.**  

✅ **Features of Interfaces:**  
✔ **Can be implemented by multiple classes**  
✔ **Methods are public & abstract by default**  
✔ **Supports default & static methods (Java 8+)**  

✅ **Example Using Interfaces:**  
```java
interface Flyable {
    void fly(); // Abstract method
}
class Bird implements Flyable {
    public void fly() { System.out.println("Bird is flying!"); }
}
```

---

## **🔹 Tasks for Practice:**  
✔ **Create an abstract class `Shape` with a method `calculateArea()`**  
✔ **Implement subclasses `Circle` & `Square` with unique attributes & methods**  
✔ **Create an interface `Flyable` and an abstract class `Bird` implementing it**  

---

## **9.4 What is Polymorphism?**  
📌 **Polymorphism enables methods to take different forms based on objects.**  

✅ **Types of Polymorphism:**  
✔ **Compile-Time Polymorphism** → Method Overloading  
✔ **Run-Time Polymorphism** → Method Overriding  

✅ **Example Using Polymorphism:**  
```java
class Animal {
    void sound() { System.out.println("Animal makes a sound"); }
}
class Dog extends Animal {
    void sound() { System.out.println("Dog barks"); }
}
Animal a = new Dog(); // Run-Time Polymorphism
a.sound(); // Output: Dog barks
```

---

## **9.5 References & Objects (`Upcasting / Downcasting`)**  
📌 **References determine which methods are accessible, while objects define the implementation.**  

✔ **Upcasting (Safe & Automatic)** → Subclass to Superclass  
✔ **Downcasting (Risky & Manual)** → Superclass to Subclass  

✅ **Example:**  
```java
class Parent { void show() { System.out.println("Parent method"); } }
class Child extends Parent { void display() { System.out.println("Child method"); } }

Parent p = new Child(); // ✅ Upcasting
Child c = (Child) p; // ⚠️ Downcasting (Requires instanceof check)
```

---

## **9.6 Method / Constructor Overloading**  
📌 **Overloading allows multiple methods with the same name but different parameters.**  

✅ **Example Using Method Overloading:**  
```java
class Calculator {
    int add(int a, int b) { return a + b; }
    double add(double a, double b) { return a + b; }
}
```

---

## **9.7 `super` Keyword**  
📌 **Used to refer to the parent class in a subclass.**  

✅ **Example Using `super`:**  
```java
class Parent {
    void greet() { System.out.println("Hello from Parent"); }
}
class Child extends Parent {
    void greet() {
        super.greet(); // Calls parent method
        System.out.println("Hello from Child");
    }
}
```

---

## **9.8 Method / Constructor Overriding**  
📌 **Overriding allows a subclass to provide a specific implementation of a parent method.**  

✅ **Example Using Method Overriding:**  
```java
class Parent {
    void show() { System.out.println("Parent method"); }
}
class Child extends Parent {
    @Override
    void show() { System.out.println("Child method"); }
}
```

---

## **9.9 `final` Keyword (Revisited)**  
📌 **`final` restricts modification of variables, methods & classes.**  

✅ **Example:**  
```java
final class Constants { } // Cannot be inherited

class Example {
    final void display() { System.out.println("Final method!"); } // Cannot be overridden
}
```

---

## **9.10 Pass by Value vs Pass by Reference**  
📌 **Java passes variables by value, but objects by reference.**  

✅ **Example Using Pass by Value:**  
```java
void changeValue(int num) { num = 50; }
int x = 10;
changeValue(x);
System.out.println(x); // Output: 10 (Original remains unchanged)
```

✅ **Example Using Pass by Reference:**  
```java
void modifyObject(MyClass obj) { obj.value = 50; }
MyClass myObj = new MyClass();
modifyObject(myObj);
System.out.println(myObj.value); // Output: 50 (Object value modified)
```

---

## **🔹 More Practice Tasks:**  
✔ **Overload `add()` method in a Calculator class**  
✔ **Override `service()` method in a `Vehicle` & `Car` class**  

---
