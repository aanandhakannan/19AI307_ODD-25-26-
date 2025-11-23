# Ex.No:3(b) POLYMORPHISM

## QUESTION:
 Write a Java program to create a class Vehicle with a method called speedUp(). Create two subclasses Car and Bicycle. Override the speedUp() method in each subclass to increase the vehicle's speed differently.

## **Aim**

To create a superclass `Vehicle` with a `speedUp()` method and override this method in the subclasses `Car` and `Bicycle` so that each increases speed differently.



## **Algorithm**

1. Start the program.
2. Create a superclass **Vehicle** with a method `speedUp()`.
3. Create a subclass **Car** that extends Vehicle.
4. Override the `speedUp()` method inside Car to increase speed in its own way.
5. Create another subclass **Bicycle** that also extends Vehicle.
6. Override the `speedUp()` method in Bicycle with a different speed-increase logic.
7. Create objects of Car and Bicycle.
8. Call the overridden `speedUp()` method on both objects to demonstrate different behaviors.
9. End the program.





## PROGRAM:
 ```
/*
Program to implement a Polymorphism using Java
Developed by: 
RegisterNumber:  
*/
```

## SOURCE CODE:

```
import java.util.*;
class Vehicle{
    void speedUp(int a){
        System.out.println("Spped: ");
    }
}
class Car extends Vehicle{
    void speedUp(int a){
        System.out.println("Car speed increased to: "+(a*2)+" km/h");
    }
}
class Bicycle extends Vehicle{
    void speedUp(int a){
        System.out.println("Bicycle speed increased to: "+a+" km/h");
        
    }
}
public class prog{
    public static void main(String[] args){
        Scanner scan = new Scanner(System.in);
        String a = scan.next().toLowerCase();
        int b =scan.nextInt();
        if(a.equals("car")){
            Car obj = new Car();
            obj.speedUp(b);
        }
        else if(a.equals("bicycle")){
            Bicycle obj = new Bicycle();
            obj.speedUp(b);
            
        }
        else{
            System.out.println("Invalid type");
        }
    }
}
```






## OUTPUT:

<img width="870" height="314" alt="image" src="https://github.com/user-attachments/assets/281d1fa8-c50b-45c9-8e01-80508b1d96aa" />


## RESULT:
Thus java program executed successfully.
