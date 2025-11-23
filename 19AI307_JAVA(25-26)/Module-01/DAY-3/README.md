# Ex.No:1(C) LOOPING STATEMENT

## QUESTION:
Write a Java program to calculate the factorial of a number using a for loop. The factorial of n is the product of all positive integers less than or equal to n.




## **Aim**

To write a Java program that calculates the factorial of a given number using a for loop.


## **Algorithm**

1. Start the program.
2. Read the number `n` from the user.
3. Initialize a variable `factorial` to 1.
4. Use a for loop from 1 to `n`.
5. Multiply `factorial` by each loop value.
6. After the loop ends, display the final factorial value.
7. End the program.


## PROGRAM:
 ```
/*
Program to implement a Looping Statement using Java
Developed by: 
RegisterNumber:  
*/
```

## SOURCE CODE:


```
import java.util.Scanner;
public class Main {
    public static void main(String[] args){
        Scanner scan = new Scanner(System.in);
        int Factorial = scan.nextInt();
        int Fact=1;
        if(Factorial==0){
            Fact=1;
        }
        else{
            for(int i=1;i<=Factorial;i++)
            {
                Fact*=i;
            }
        }
        System.out.println("Factorial of "+Factorial+" is: "+Fact);
    }
    }
```




## OUTPUT:
<img width="764" height="252" alt="image" src="https://github.com/user-attachments/assets/c6566496-753f-496b-8362-56a10f267463" />



## RESULT:
Thus java program executed successfully.

