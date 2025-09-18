```java
public class Main {
    public static class Frac {
        private int num;
        private int den;

        // Default constructor    
        public Frac() {
            this.num = 1;
            this.den = 1;
        }

        // Non-default constructor
        public Frac(int n, int d) {
            if(d == 0) {
                throw new IllegalArgumentException("Denominator cannot be zero.");
            }
            this.num = n;
            this.den = d;
        }

        // Mutators / setters
        public void setNum(int n) {
            this.num = n;
        }

        public void setDen(int d) {
            if(d == 0) {
                throw new IllegalArgumentException("Denominator cannot be zero.");
            }
            this.den = d;
        }

        public void setFrac(int n, int d) {
            if(d == 0) {
                throw new IllegalArgumentException("Denominator cannot be zero.");
            }
            this.num = n;
            this.den = d;
        }

        // Accessors / getters
        public int getNum() {
            return this.num;
        }

        public int getDen() {
            return this.den;
        }

        // Mathematical Operations
        public Frac multiply(Frac f) {
            return new Frac(this.num * f.num, this.den * f.den);
        }

        public Frac add(Frac f) {
            int newNum = this.num * f.den + f.num * this.den;
            int newDen = this.den * f.den;
            return new Frac(newNum, newDen);
        }

        // Display
        public void display() {
            System.out.println(this.num + "/" + this.den);
        }
    }

    // Testing the class
    public static void main(String[] args) {
        Frac f1 = new Frac(2, 3);
        Frac f2 = new Frac(3, 4);

        Frac sum = f1.add(f2);
        Frac product = f1.multiply(f2);

        System.out.print("Sum: ");
        sum.display(); // 17/12

        System.out.print("Product: ");
        product.display(); // 6/12
    }
}
```
