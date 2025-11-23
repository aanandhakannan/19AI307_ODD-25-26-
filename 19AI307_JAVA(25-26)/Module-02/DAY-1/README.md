# Ex.No:2(A) CLASS AND OBJECT

## QUESTION:
Create a class Vehicle with attributes as number, type and owner.

## **Aim**

To create a Java class named **Vehicle** that stores basic information about a vehicle, including its number, type, and owner.


## **Algorithm**

1. Start the program.
2. Define a class named **Vehicle**.
3. Declare three attributes:

   * `number` to store the vehicle number
   * `type` to store the vehicle type
   * `owner` to store the owner’s name
4. Provide a constructor to initialize these attributes.
5. (Optional) Add methods to display or access the vehicle details.
6. End the program.


## PROGRAM:
 ```
/*
Program to implement a Class and Objects using Java
Developed by: 
RegisterNumber:  
*/
```

## SOURCE CODE:

```
import java.util.Scanner;
class Vehicle{
    String number;
    String type;
    String owner;
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String Vehicle;

        Vehicle v1 = new Vehicle();
        v1.number = sc.next();
        v1.type = sc.next();
        v1.owner = sc.next();

        Vehicle v2 = new Vehicle();
        v2.number = sc.next();
        v2.type = sc.next();
        v2.owner = sc.next();

        System.out.println(v1.number + " | " + v1.type + " | " + v1.owner);
        System.out.println(v2.number + " | " + v2.type + " | " + v2.owner);

        sc.close();
    }
}

```





## OUTPUT:

<img width="1055" height="269" alt="image" src="https://github.com/user-attachments/assets/b099d80c-fcb2-433d-b845-8ad94104e72e" />


## RESULT:
Thus java program executed successfully.

