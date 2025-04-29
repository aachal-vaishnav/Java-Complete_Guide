
# 📌 2. Java Basics  

## **2.1 Installation & Setup**  
Before writing Java code, we need to install the **Java Development Kit (JDK)**.  

### ✅ **Installing JDK**  
1. **Search for "JDK Download"**  
2. **Download from the official Oracle website:** [Click here](https://www.oracle.com/java/technologies/javase-jdk-downloads.html)  
3. **Choose the latest version** based on your OS (Windows/macOS/Linux)  
4. **Install the JDK** following the setup instructions  
5. **Set up `JAVA_HOME`** environment variable (if needed)  

Once installed, verify by running:  
```bash
java -version
```
✅ If correctly installed, this command will display the Java version installed on your machine.  

---  

## **2.2 What is JDK, JRE & JVM?**  
Understanding **JDK, JRE, and JVM** is **critical** for working with Java!  

### **JDK (Java Development Kit)**  
🛠️ The **JDK** is required for **developing** Java applications.  
🔹 Includes **compiler (`javac`), debugger, documentation tools (`javadoc`), and development libraries**.  
🔹 **Essentially, JDK is a superset of JRE**.  

### **JRE (Java Runtime Environment)**  
📦 The **JRE** is needed **only for running Java applications**, not developing them.  
🔹 Includes **JVM, core libraries, and runtime components** required for execution.  
🔹 **JRE does not have a compiler or debugging tools**.  

### **JVM (Java Virtual Machine)**  
🚀 The **JVM** is responsible for **executing Java bytecode** (`.class` files).  
🔹 Ensures **Java’s platform independence** (Write Once, Run Anywhere).  
🔹 **Different JVM versions exist for each OS**, making Java cross-platform.  

### **JDK vs JRE vs JVM – Relationship & Workflow**  
1️⃣ **JDK** → **Compiles Java code** (`javac`) → Produces **Bytecode** (`.class`)  
2️⃣ **JRE** → **Contains JVM** to **run** compiled Java programs  
3️⃣ **JVM** → **Executes Bytecode** and ensures platform independence  

🚀 **In short**:  
✅ **JDK = JRE + Development tools**  
✅ **JRE = JVM + Runtime libraries**  
✅ **JVM = Executes Java Bytecode**  

---  

## **2.3 Writing Your First Java Program**  
Now that Java is installed, let’s write and run our **first Java program**!  

### ✅ **Create a Simple Java File**  
📌 Open a **text editor** (Notepad, VS Code, or IntelliJ IDEA).  
📌 Create a new file **MyFirstProgram.java**.  
📌 Write this simple **Java program**:  

```java
public class MyFirstProgram {
    public static void main(String[] args) {
        System.out.println("Hello, Java!");
    }
}
```

📌 **Save** the file in a known location.  

### ✅ **Compiling & Running Java Program**  
📌 **Compile the program** using `javac`:  
```bash
javac MyFirstProgram.java
```
📌 **Run the compiled program** using `java`:  
```bash
java MyFirstProgram
```
✅ **Expected Output:**  
```
Hello, Java!
```

🚀 **Congrats! 🎉 You’ve written and executed your first Java program!**  

---  

## **2.4 Central Theme – What This Section Covers?**  
This section **establishes a strong foundation** for Java beginners by covering:  

✅ **Installation & Setup** → Getting JDK ready  
✅ **JDK vs JRE vs JVM** → Understanding their roles & relationships  
✅ **Writing First Java Program** → Learning how Java code is structured & executed  

---
