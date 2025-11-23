# Ex.No:1(B) CONDITIONAL STATEMENT

## QUESTION:
Write a java program to get the user input for temperature and display appropriate output


## AIM:

To write a Java program that accepts the temperature as user input and displays an appropriate message based on the entered value.


## **Algorithm**

1. Start the program.
2. Create a `Scanner` object to read user input.
3. Prompt the user to enter the temperature.
4. Read and store the temperature value.
5. If the temperature is greater than 30, display “It is Hot”.
6. Else if the temperature is between 20 and 30, display “It is Warm”.
7. Otherwise, display “It is Cold”.
8. End the program.






## PROGRAM:
 ```
/*
Program to implement a conditional statement using Java
Developed by: 
RegisterNumber:  
*/
```

## SOURCE CODE:
```
import java.util.*;
public class Main{
    public static void main(String[] args){
        Scanner scan=new Scanner(System.in);
        int a = scan.nextInt();
        
        if(a<0){
            System.out.println("Hibernating");
        }
        else if(a<=20){
            System.out.println("Snoozing");
        }
        else if((a>=21)&&(a<=35)){
            System.out.println("Awake");
        }
        else if(a>35){
            System.out.println("Angry");
        }
    }
}
```






## OUTPUT:

<img width="719" height="376" alt="image" src="https://github.com/user-attachments/assets/ffc147dd-dc4e-4c33-820d-25cad48eab74" />


## RESULT:
Thus java program executed successfully.

