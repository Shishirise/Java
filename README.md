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
Declared inside the class but outside any method
Each object of Main gets its own copy

public class Main{
     int x;
     String  name; 
    public static void main(String[]args){
      
    }
}

Declared inside the method main()
Can only be used inside main()
Must be initialized before use

public class Main{
    public static void main(String[]args){
        
    int x;
     String  name;
      
    }
}


```

