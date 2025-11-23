# Ex.No:3(E) INNER CLASS

## QUESTION:
Write a Java program to create an enum called Day with constants for all days of the week, and print each day using a loop.


## **Aim**

To create an enum named `Day` containing constants for all days of the week and print each day using a loop.



## **Algorithm**

1. Start the program.
2. Define an enum **Day** with constants for all seven days of the week.
3. In the main method, access all enum values using `Day.values()`.
4. Use a loop (such as a for-each loop) to iterate through the enum values.
5. Print each day inside the loop.
6. End the program.





## PROGRAM:
 ```
/*
Program to implement a InnerClass using Java
Developed by: 
RegisterNumber:  
*/
```

## SOURCE CODE:
```
import java.util.*;
enum Day{
    SUNDAY,MONDAY,TUESDAY,WEDNESDAY,THURSDAY,FRIDAY,SATURDAY;
}
public class prog{
    public static void main(String[] args){
        Scanner scan = new Scanner(System.in);
        int a = scan.nextInt();
        Day[] days = Day.values();
        for(int i =0;i<a;i++){
            System.out.println(days[i]);
        }
    }
}
```






## OUTPUT:
<img width="496" height="586" alt="image" src="https://github.com/user-attachments/assets/d4747262-6e1d-4be3-b47c-0599306986a6" />



## RESULT:
Thus java program executed successfully
