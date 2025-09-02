import java.util.*;



public class Main {
    public static void main(String[] args) {
        
        Scanner scanner = new Scanner(System.in);
         
        System.out.println("Enter a:");
        double a = scanner.nextDouble();  
        
        
        
        System.out.println("Enter b:");
         double b = scanner.nextDouble();  
        
       
        
        System.out.println("Enter c:");
        double c = scanner.nextDouble();  
        
       
        
        
        double discriminant= b*b-4*a*c;
        
        double x1=0;
        double x2=0;
        
        if(discriminant<0){
            System.out.println("no real solutions");
        }else{
           x1= (-b+Math.sqrt(discriminant)) / (2*a);
           x2= (-b-Math.sqrt(discriminant)) / (2*a);
           
        System.out.printf("X1: %.2f\n", x1);
        System.out.printf("X2: %.2f\n", x2);
         
        }
        
         
         
        }
        
        
    }

