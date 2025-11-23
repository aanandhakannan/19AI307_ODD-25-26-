# Ex.No:5(E) MULTITHREADING -SYNCHRONIZATION

## QUESTION:

Maintain two int variables a and b, read their initial values from user. Use synchronized block to swap them and print swapped values.

## **Aim**

To write a Java program that maintains two integer variables `a` and `b`, reads their initial values from the user, and uses a synchronized block to safely swap their values and display the swapped results.

---

## **Algorithm**

1. Start the program.
2. Read two integer values from the user and assign them to variables `a` and `b`.
3. Create an object to use as a lock for synchronization.
4. Enter a `synchronized` block using the lock object.
5. Inside the synchronized block, perform the swap using a temporary variable.
6. After swapping, print the new values of `a` and `b`.
7. End the program.






## PROGRAM:
 ```
/*
Program to implement a Synchronization concept using Java
Developed by: 
RegisterNumber:  
*/
```

## SOURCE CODE:

```
import java.util.Scanner;

public class SwapSynchronized {
    private int a;
    private int b;
    private final Object lock = new Object(); // lock object for synchronization

    public SwapSynchronized(int a, int b) {
        this.a = a;
        this.b = b;
    }

    public void swap() {
        // Synchronized block to safely swap values
        synchronized (lock) {
            int temp = a;
            a = b;
            b = temp;
        }
    }

    public void printValues() {
        System.out.println("a = " + a);
        System.out.println("b = " + b);
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        // Read initial values
        int a = Integer.parseInt(sc.nextLine().trim());
        int b = Integer.parseInt(sc.nextLine().trim());

        SwapSynchronized obj = new SwapSynchronized(a, b);

        // Swap and print
        obj.swap();
        obj.printValues();
    }
}


```





## OUTPUT:


<img width="548" height="326" alt="image" src="https://github.com/user-attachments/assets/fcd5b199-1c37-40a7-90cc-d416dd9ecb5e" />


## RESULT:

Thus java program executed successfully.

