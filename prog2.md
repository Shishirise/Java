```java
import java.util.Scanner;

public class Complexnum {

    private double r;
    private double im;

    // Default constructor
    public Complexnum() {
        r = 0;
        im = 0;
    }

    // Parameterized constructor
    public Complexnum(double r, double im) {
        this.r = r;
        this.im = im;
    }

    // Copy constructor
    public Complexnum(Complexnum c) {
        this.r = c.r;
        this.im = c.im;
    }

    // Getters
    public double getReal() {
        return r;
    }

    public double getImaginary() {
        return im;
    }

    // Setters
    public void setReal(double r) {
        this.r = r;
    }

    public void setImaginary(double im) {
        this.im = im;
    }

    // Addition
    public Complexnum add(Complexnum c) {
        double newR = this.r + c.r;
        double newIm = this.im + c.im;
        return new Complexnum(newR, newIm);
    }

    // Subtraction
    public Complexnum subtract(Complexnum c) {
        double newR = this.r - c.r;
        double newIm = this.im - c.im;
        return new Complexnum(newR, newIm);
    }

    // Multiplication
    public Complexnum multiply(Complexnum c) {
        double newR = this.r * c.r - this.im * c.im;
        double newIm = this.r * c.im + this.im * c.r;
        return new Complexnum(newR, newIm);
    }

    // Division
   public Complexnum divide(Complexnum c) {
    double denominator = c.r * c.r + c.im * c.im;

    if (denominator == 0) {
        System.out.println("Cannot divide by zero complex number!");
        return null; // indicate invalid division
    } else {
        double newR = (this.r * c.r + this.im * c.im) / denominator;
        double newIm = (this.im * c.r - this.r * c.im) / denominator;
        return new Complexnum(newR, newIm);
    }
}


    // Multiply by scalar
    public Complexnum multiplyScalar(double scalar) {
        return new Complexnum(this.r * scalar, this.im * scalar);
    }

    // Display
    public void print() {
     
    System.out.printf("%.2f %+.2fi%n", r, im);
    
    }

    // Main method
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);

        System.out.print("Enter real and imaginary parts of complex number one(C1): ");
        double r1 = in.nextDouble();
        double i1 = in.nextDouble();

        System.out.print("Enter real and imaginary parts of complex number two(C2): ");
        double r2 = in.nextDouble();
        double i2 = in.nextDouble();
        
        
        System.out.print("Which complex number do you like to multiply with (Enter: C1= 1 or for C2 = 2):");
        int choice = in.nextInt();

        System.out.print("Enter the scalar to multiply by: ");
        double scalarValue = in.nextDouble();

       System.out.println("---------------------------------------------------------------------------------");
       System.out.println("\n");
       
       
        Complexnum C1 = new Complexnum(r1, i1);
        Complexnum C2 = new Complexnum(r2, i2);

        Complexnum sum = C1.add(C2);
        System.out.print("Sum of the two complex number (C1+C2): ");
        sum.print();
        System.out.println("\n");

        
        Complexnum subtract = C1.subtract(C2);
        System.out.print("Difference of the two complex number (C1-C2): ");
        subtract.print();
        System.out.println("\n");
        

        Complexnum multiply = C1.multiply(C2);
        System.out.print("Product of the two complex number (C1*C2): ");
        multiply.print();
        System.out.println("\n");   
        
        Complexnum divide = C1.divide(C2);
        System.out.print("Division of the two complex number (C1/C2): ");
        divide.print();
        System.out.println("\n");
        
        Complexnum scalarResult;
        if (choice == 1) {
            scalarResult = C1.multiplyScalar(scalarValue);
            System.out.print("Scalar Multiplication (C1 * " + scalarValue + "): ");
        } else {
            scalarResult = C2.multiplyScalar(scalarValue);
            System.out.print("Scalar Multiplication (C2 * " + scalarValue + "): ");
        }
        scalarResult.print();
        

        // Copy test
        C1 = new Complexnum(C2);
        
        System.out.println("\n");
        System.out.print("After copying the values of C2 into a new Complexnum object, C1: ");
        C1.print();
    }
}


```
