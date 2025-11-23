# Ex.No:2(D) VARIABLE SCOPE AND CONSTRUCTOR

## QUESTION:
Write a java code to implement a parameterised constructor that will initialize the id,name,age,gender,doj,dob of the student and print the details using user defined function.

## **Aim**

To write a Java program that uses a parameterized constructor to initialize a student’s id, name, age, gender, date of joining (doj), and date of birth (dob), and prints these details using a user-defined function.



## **Algorithm**

1. Start the program.
2. Create a class named **Student**.
3. Declare instance variables: `id`, `name`, `age`, `gender`, `doj`, and `dob`.
4. Define a **parameterized constructor** that accepts these values as parameters and assigns them to the instance variables.
5. Create a **user-defined method** (e.g., `displayDetails()`) to print all student details.
6. In the main method, create an object of the Student class by passing the required values to the constructor.
7. Call the user-defined method to display the student information.
8. End the program.






## PROGRAM:
 ```
/*
Program to implement a Variable scope and Constructor using Java
Developed by: 
RegisterNumber:  
*/
```

## SOURCE CODE:

```
import java.util.Scanner;
class Details{
    long id;
    String name;
    int age;
    String gender;
    String join;
    String birth;
    
    Details(long id,String name,int age,String gender,String join,String birth){
        this.id=id;
        this.name=name;
        this.age=age;
        this.gender=gender;
        this.join=join;
        this.birth=birth;
        
    }
    void display(){
        System.out.println("--- Student Details ---");
        System.out.println("ID: "+id);
        System.out.println("Name: "+name);
        System.out.println("Age: "+age);
        System.out.println("Gender: "+gender);
        System.out.println("Date of Joining: "+join);
        System.out.println("Date of Birth: "+birth);
    }
}
public class Main{
    public static void main(String[] args){
        Scanner scan = new Scanner(System.in);
        long id=scan.nextLong();
        String name=scan.next();
        int age=scan.nextInt();
        String gender=scan.next();
        String join=scan.next();
        String birth=scan.next();
        Details det=new Details(id,name,age,gender,join,birth);
        det.display();
        
        
    }
}
```





## OUTPUT:

<img width="816" height="682" alt="image" src="https://github.com/user-attachments/assets/d2308a3f-3b02-4277-8ee7-a2ae5324a0d6" />


## RESULT:

Thus java program executed successfully
