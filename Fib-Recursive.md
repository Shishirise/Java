```java
import java.util.Scanner;

public class Main {

    public static int fib(int n) {
        if (n == 0) return 0;
        if (n == 1) return 1;
        return fib(n - 1) + fib(n - 2);
    }

    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);  // fixed Scanner initialization

        System.out.println("Enter your number:");
        int n = in.nextInt();  // read the number of Fibonacci terms

        int[] arr = new int[n];  // create an array to store Fibonacci numbers

        // fill the array
        for (int i = 0; i < n; i++) {
            arr[i] = fib(i);
        }

        // print the Fibonacci series
        System.out.println("Fibonacci Series:");
        for (int i = 0; i < n; i++) {
            System.out.print(arr[i] + " ");
        }
    }
}
```
