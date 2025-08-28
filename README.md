# Java
WORA (Write Once, Run Anywhere)

## Variables in Java
```
dataType variableName = value;
```
```java
Example:
int age = 21;
double price = 19.99;
String name = "Bahubali";
```
# Types of Variables in Java
## 1. Local Variables
```java
Declared inside a method/functions.
Only accessible within that method.
Must be initialized before use.


public class Example {
    public static void main(String[] args) {
        int x = 10; // local variable
        System.out.println(x);
    }
}
```
## 2.Instance Variables
```java
Declared inside a class but outside methods.
Each object gets its own copy.


public class Student {
    // ✅ Instance Variables
    String name;   // inside class, but outside methods
    int age;

    // Instance Method
    public void display() {
        System.out.println("Name: " + name + ", Age: " + age);
    }

    public static void main(String[] args) {
        // First object
        Student s1 = new Student();
        s1.name = "Alice";
        s1.age = 20;

        // Second object
        Student s2 = new Student();
        s2.name = "Bob";
        s2.age = 22;

        // Each object has its OWN copy of instance variables
        s1.display();  // Name: Alice, Age: 20
        s2.display();  // Name: Bob, Age: 22
    }
}

```

