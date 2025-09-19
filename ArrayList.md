```java
import java.util.ArrayList;


public class Main{
    public static void main(String[]args){
        
        ArrayList<Integer> names= new ArrayList<>();  // No int only (Integer) names= variable for to ArrayList<Integer> object
        
        
        names.add(1);
        names.add(2);
        
        names.remove(1);
        
        
        for(int name:names){// name= Temperory variable for loop
            System.out.println(name);
        }
    }
}
```
