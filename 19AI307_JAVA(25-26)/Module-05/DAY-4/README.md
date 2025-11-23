# Ex.No:5(D) THREAD PRIORITY

## QUESTION:

Write a java program for determine the priority and name of the current thread.


## **Aim**

To write a Java program that determines and displays the name and priority of the current executing thread.


## **Algorithm**

1. Start the program.
2. Obtain a reference to the current thread using `Thread.currentThread()`.
3. Retrieve the thread’s name using `getName()`.
4. Retrieve the thread’s priority using `getPriority()`.
5. Display the thread name and priority on the screen.
6. End the program.






## PROGRAM:
 ```
/*
Program to implement a Thread Priority Concept using Java
Developed by: 
RegisterNumber:  
*/
```

## SOURCE CODE:

```
import java.util.Scanner;

class MyThread extends Thread {
    public MyThread(String name) {
        super(name); // Set the thread name
    }

    @Override
    public void run() {
        // Display thread information
        System.out.println("Priority of Thread: " + this.getPriority());
        System.out.println("Name of Thread: " + this.getName());
        System.out.println(this.toString());
    }
}

public class ThreadInfoExample {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
       
        String threadName = sc.nextLine();
        
        // Create a thread with the input name
        MyThread t = new MyThread(threadName);
        
        // You can set a custom priority if desired (default is 5)
        t.setPriority(Thread.NORM_PRIORITY);
        
        // Start the thread
        t.start();
        
        sc.close();
    }
}

```





## OUTPUT:


<img width="758" height="220" alt="image" src="https://github.com/user-attachments/assets/b037bb25-2f91-4ade-aac4-a0bec3bd5fc7" />


## RESULT:

Thus java program executed successfully.
