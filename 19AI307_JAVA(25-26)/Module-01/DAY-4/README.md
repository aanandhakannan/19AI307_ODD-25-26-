# Ex.No:1(D) ARRAYS

## QUESTION:
Write a Java program to count how many elements in an array are divisible by 3 or 5


## **Aim**

To develop a Java program that counts how many elements in an array are divisible by 3 or 5.


## **Algorithm**

1. Start the program.
2. Read the size of the array from the user.
3. Input all elements of the array.
4. Initialize a counter to 0.
5. Traverse each element of the array using a loop.
6. For each element, check if it is divisible by 3 or divisible by 5.
7. If the condition is true, increment the counter.
8. After the loop ends, display the count.
9. End the program.





## PROGRAM:
 ```
/*
Program to implement a Array concept using Java
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
        int a =scan.nextInt();
        int[] arr=new int[a];
        int count = 0;
        for(int i =0;i<a;i++){
            arr[i]=scan.nextInt();
            if((arr[i]%3==0) || (arr[i] %5==0)){
                count++;
            }
        }
        System.out.println(count);
    }
}
```





## OUTPUT:
<img width="464" height="583" alt="image" src="https://github.com/user-attachments/assets/ff5bf651-ebc2-4296-b8bb-036468f6094c" />



## RESULT:
Thus java program executed successfully.

