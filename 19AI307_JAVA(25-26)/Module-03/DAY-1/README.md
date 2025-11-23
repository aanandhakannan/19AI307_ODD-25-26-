# Ex.No:3(A) INHERITANCE AND AGGREGATION

## QUESTION:
Create a Super class Person with fields name and age. Create a subclass Student that inherits from Person and adds a field marks (integer). Implement a method in Student called calculateGrade() which returns the grade based on the marks:


## **Aim**

To create a superclass `Person` with fields `name` and `age`, and a subclass `Student` that adds `marks` and implements a method `calculateGrade()` to return a grade based on the marks.




## **Algorithm**

1. Start the program.
2. Create a superclass **Person** with fields `name` and `age`.
3. Create a subclass **Student** that extends `Person`.
4. Add an additional field `marks` in the Student class.
5. Implement a method **calculateGrade()** in Student that:

   * Checks the value of `marks`.
   * Returns a grade based on mark ranges (e.g., A, B, C…).
6. Create an object of Student and assign name, age, and marks.
7. Call the `calculateGrade()` method to get the grade.
8. End the program.






## PROGRAM:
 ```
/*
Program to implement a Inheritance and Aggregation using Java
Developed by: 
RegisterNumber:  
*/
```

## SOURCE CODE:


```
import java.util.Scanner;


class Person {
    String name;
    int age;


    Person(String name, int age) {
        this.name = name;
        this.age = age;
    }
}

class Student extends Person {
    int marks;

    
    Student(String name, int age, int marks) {
        super(name, age);
        this.marks = marks;
    }

    
    String calculateGrade() {
        if (marks >= 90) {
            return "A";
        } else if (marks >= 75) {
            return "B";
        } else if (marks >= 50) {
            return "C";
        } else {
            return "F";
        }
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        
        String name = sc.nextLine();
        int age = sc.nextInt();
        int marks = sc.nextInt();

      
        Student s = new Student(name, age, marks);

 
        System.out.println("Name: " + s.name);
        System.out.println("Age: " + s.age);
        System.out.println("Marks: " + s.marks);
        System.out.println("Grade: " + s.calculateGrade());
    }
}

```




## OUTPUT:
<img width="565" height="574" alt="image" src="https://github.com/user-attachments/assets/a971f8d6-3e00-4a62-9390-9dabc903eb1a" />



## RESULT:

Thus java program executes successfully.
