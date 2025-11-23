# Ex.No:2(B) METHODS

## QUESTION:
Write a method int cube(int x) that calls a method int square(int x) internally to calculate the cube as x * square(x).

## **Aim**

To write a method `cube(int x)` that calculates the cube of a number by internally calling another method `square(int x)`.



## **Algorithm**

1. Start the program.
2. Define a method `square(int x)` that returns the value of `x * x`.
3. Define another method `cube(int x)`.
4. Inside `cube()`, call `square(x)` to compute the square of `x`.
5. Multiply the returned square value by `x` to get the cube.
6. Return the cube value.
7. End the program.




## PROGRAM:
 ```
/*
Program to implement a Methods using Java
Developed by: 
RegisterNumber:  
*/
```

## SOURCE CODE:


```
import java.util.*;
public class Main{
    int square(int x){
        return (int) Math.pow(x,2);
    }
    public static void main(String [] args){
        Scanner scan = new Scanner(System.in);
        int num= scan.nextInt();
        Main obj = new Main();
        int cube = obj.square(num)*num;
        System.out.println(cube);
    }
}
```




## OUTPUT:

<img width="582" height="181" alt="image" src="https://github.com/user-attachments/assets/7c66211f-481e-45b4-8cf7-701ca6982921" />


## RESULT:

Thus java program executed successfully.
