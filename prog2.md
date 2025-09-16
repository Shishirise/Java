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
    public double getReal() { return r; }
    public double getImaginary() { return im; }

    // Setters
    public void setReal(double r) { this.r = r; }
    public void setImaginary(double im) { this.im = im; }

// Add this inside the Complexnum class
    public Complexnum add(Complexnum c) {
    double newR = this.r + c.r;
    double newIm = this.im + c.im;
    return new Complexnum(newR, newIm);
}

    public Complexnum subtract(Complexnum c) {
    double newR = this.r - c.r;
    double newIm = this.im - c.im;
    return new Complexnum(newR, newIm);
}

    public Complexnum multiply(Complexnum c) {
    double newR = this.r * c.r;
    double newIm = this.im * c.im;
    return new Complexnum(newR, newIm);
}

    public Complexnum divide(Complexnum c) {
    double newR = this.r / c.r;
    double newIm = this.im / c.im;
    return new Complexnum(newR, newIm);
    
}

 public Complexnum multiplyScalar(double scalar) {
        return new Complexnum(this.r * scalar, this.im * scalar);
    }
    // Display
    public void display() {
        System.out.println("Complex number: " + r + " + " + im + "i");
    }

    // Main method
    public static void main(String[] args) {
        Complexnum C1 = new Complexnum(3,4);
        Complexnum C2 = new Complexnum(1,2); // using copy constructor

        
        Complexnum sum = C1.add(C2);
        sum.display();
        
        Complexnum subtract = C1.subtract(C2);
        subtract.display();
        
        Complexnum multiply = C1.multiply(C2);
        multiply.display();
        
        Complexnum divide = C1.divide(C2);
        divide.display();
        
       
        Complexnum scalar = C1.multiplyScalar(2);
        scalar.display();
    }
}
