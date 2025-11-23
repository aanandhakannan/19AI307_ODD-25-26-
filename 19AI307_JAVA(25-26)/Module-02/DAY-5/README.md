# Ex.No:2(E) ACCESS MODIFIERS

## QUESTION:
Create a class Employee with method display(). Inside display(), return the current object using this. Create another method that calls display().printName()



## **Aim**

To create a Java class `Employee` where the `display()` method returns the current object using `this`, and another method calls `display().printName()` to access a method of the returned object.



## **Algorithm**

1. Start the program.
2. Create a class named **Employee**.
3. Declare a method **printName()** to print the employee name.
4. Define a method **display()** that returns the current object using `return this;`.
5. Create another method (e.g., `callMethods()`) that invokes `display().printName()`.
6. In the main method, create an object of the Employee class.
7. Call the method that uses `display().printName()` to execute the chain of calls.
8. End the program.



## PROGRAM:
 ```
/*
Program to implement a Access Modifiers using Java
Developed by: 
RegisterNumber:  
*/
```

## SOURCE CODE:

```
import java.util.Scanner;
class Employee{
    String name;
    
    void setName(String name){
        this.name=name;
        
    }
    String display(){
        return name;
    }
    void printName(){
        System.out.println("Employee Name: "+name);
    }
}
class prog{
    public static void main(String [] args){
        Scanner scan= new Scanner(System.in);
        String name=scan.next();
        Employee emp=new Employee();
        emp.setName(name);
        emp.printName();
    }
}
```





## OUTPUT:

<img width="758" height="252" alt="image" src="https://github.com/user-attachments/assets/e46458af-c855-4115-8804-ae3f7c100633" />


## RESULT:
Thus java program executed successfully

