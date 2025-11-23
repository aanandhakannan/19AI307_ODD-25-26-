# Ex.No:2(C) ACCESS SPECIFIERS

## QUESTION:
Write a Java program to create a class called Person with private instance variables name, age. and country. Provide public getter and setter methods to access and modify these variables.

## **Aim**

To create a Java class `Person` with private instance variables `name`, `age`, and `country`, and to provide public getter and setter methods to access and modify these variables.



## **Algorithm**

1. Start the program.
2. Define a class named **Person**.
3. Declare three private instance variables: `name`, `age`, and `country`.
4. Create public **setter methods** to assign values to each variable.
5. Create public **getter methods** to return the values of each variable.
6. Use these methods to access and modify person details as needed.
7. End the program.






## PROGRAM:
 ```
/*
Program to implement a Access Specifiers using Java
Developed by: 
RegisterNumber:  
*/
```

## SOURCE CODE:
```
import java.util.*;
class Person{
    private String name;
    private int age;
    private String country;
    public String getName(){
        return name;
    }
    public void setName(String name){
        this.name=name;
    }
    public int getAge(){
        return age;
    }
    public void setAge(int age){
        this.age=age;
    }
    public String getCountry(){
        return country;
    }
    public void setCountry(String country){
        this.country=country;
    }
}
public class Main{
    public static void main(String[] args){
        Scanner scan = new Scanner(System.in);
        String name=scan.nextLine();
        int age = scan.nextInt();
        String country= scan.next();
        
        Person obj1 = new Person();
        obj1.setName(name);
        obj1.setAge(age);
        obj1.setCountry(country);
        System.out.println("Person 1");
        System.out.println("Name: "+obj1.getName());
        System.out.println("Age: "+obj1.getAge());
        System.out.println("Country: "+obj1.getCountry());
        
    }
}


```





## OUTPUT:

<img width="816" height="466" alt="image" src="https://github.com/user-attachments/assets/a04e1144-6cfb-4a09-ab96-a717f9f23d9d" />


## RESULT:
Thus java program executed successfully
