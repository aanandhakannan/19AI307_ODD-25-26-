# Ex.No:3(F) WRAPPER CLASS

## QUESTION:

Write a Java program to check if a number is an Armstrong number using Math.pow() and the Integer wrapper class. Take input from the user.

## **Aim**

To write a Java program that checks whether a given number is an Armstrong number using `Math.pow()` and the `Integer` wrapper class while taking input from the user.


## **Algorithm**

1. Start the program.
2. Read a number from the user.
3. Convert the number to a string using the `Integer` wrapper class to determine the total number of digits.
4. Initialize a sum variable to 0.
5. Extract each digit of the number using a loop.
6. For each digit, compute `Math.pow(digit, number_of_digits)` and add it to the sum.
7. After processing all digits, compare the sum with the original number.
8. If both are equal, the number is an Armstrong number; otherwise, it is not.
9. End the program.






## PROGRAM:
 ```
/*
Program to implement a Wrapper Class using Java
Developed by: 
RegisterNumber:  
*/
```

## SOURCE CODE:

```
import java.util.Scanner;

public class ArmstrongCheck {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
       
        int number = scanner.nextInt();
        int original = number;
        
       
        int digits = Integer.toString(number).length();
        
        int sum = 0;
        int temp = number;
        
      
        while (temp > 0) {
            int digit = temp % 10;
            sum += (int) Math.pow(digit, digits);
            temp /= 10;
        }
        
        // Check Armstrong condition
        if (sum == original) {
            System.out.println(original + " is an Armstrong number.");
        } else {
            System.out.println(original + " is not an Armstrong number.");
        }
    }
}

```





## OUTPUT:

<img width="838" height="250" alt="image" src="https://github.com/user-attachments/assets/3001ea96-e78a-4ba7-9445-09c7d30de0cd" />


## RESULT:
Thus java program executed successfully

