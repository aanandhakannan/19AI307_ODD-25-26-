# Ex.No:4(A) EXCEPTION HANDLING

## QUESTION:
If an Integer object is set to null, and you attempt to call .toString() on it, what happens? How can you prevent your code from throwing an exception in such cases?

## **Aim**

To understand what happens when calling `.toString()` on a null Integer object and to learn how to prevent a NullPointerException by safely handling null values in Java.

-
## **Algorithm**

1. Start the program.
2. Declare an `Integer` object and assign it a value or null.
3. Before calling `.toString()`, check whether the object is null.
4. If the object is not null, safely call `.toString()` and display the result.
5. If the object is null, print a message indicating that the value is null or use `String.valueOf()` to avoid exceptions.
6. Continue program execution without throwing an error.
7. End the program.



## PROGRAM:
 ```
/*
Program to implement a Exception Handling using Java
Developed by: 
RegisterNumber:  
*/
```

## SOURCE CODE:

```
import java.util.*;

public class Main{
    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);
        String input = scan.nextLine();
        Integer num = null;
        if(!input.isEmpty() && !input.equals("0")){
            num = Integer.parseInt(input);
        }
        try{
            System.out.println(num.toString());
        }
        catch(Exception e){
            System.out.println("Null Integer");
        }
    }
}
```





## OUTPUT:

<img width="690" height="291" alt="image" src="https://github.com/user-attachments/assets/67c722f9-7124-403e-9eaa-09a776ca5b14" />


## RESULT:
Thus java program executed successfully

