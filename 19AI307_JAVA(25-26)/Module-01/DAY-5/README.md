# Ex.No:1(E) STRINGS AND MATH FUNCTION

## QUESTION:
Write a Java program to convert a given camelCase string to snake_case.



## **Aim**

To write a Java program that converts a given camelCase string into snake_case format.

## **Algorithm**

1. Start the program.
2. Read the camelCase string from the user.
3. Create an empty result string to store the snake_case output.
4. Traverse each character of the input string.
5. If a character is uppercase:

   * Add an underscore `_` to the result.
   * Convert the uppercase character to lowercase and append it.
6. Otherwise, directly append the lowercase character to the result.
7. Display the final snake_case string.
8. End the program.





## PROGRAM:
 ```
/*
Program to implement a Strings and Math Function using Java
Developed by: 
RegisterNumber:  
*/
```

## SOURCE CODE:
```
import java.util.Scanner;
public class Main{
    public static void main(String[] args){
        Scanner scan = new Scanner(System.in);
        String a = scan.next();
        StringBuilder snake= new StringBuilder();
        snake.append('_');
        for(int i =0;i<a.length();i++){
            char c = a.charAt(i);
            if(Character.isUpperCase(c) && i>0){
                snake.append('_');
                
            }
            snake.append(Character.toLowerCase(c));
        }
        System.out.println("snake_case: "+snake.toString());
    }
}

 
```


## OUTPUT:

<img width="784" height="327" alt="image" src="https://github.com/user-attachments/assets/8bc582ea-5d70-41de-8277-614e387fa947" />



## RESULT:
Thus java program executed successfully
