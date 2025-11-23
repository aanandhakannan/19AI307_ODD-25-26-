# Ex.No:5(B) SERIALIZATION AND DESERIALIZATION 

## QUESTION:
Write a program to demonstrate reading UTF strings using DataInputStream.

## **Aim**

To write a program that demonstrates how to read UTF-formatted strings from a data file using `DataInputStream`.


## **Algorithm**

1. Start the program.
2. Open a file input stream that points to the file containing UTF strings.
3. Wrap this file input stream inside a `DataInputStream`.
4. Use the `readUTF()` method of `DataInputStream` to read UTF-encoded strings from the file.
5. Store or display the UTF strings as they are read.
6. Repeat reading until the end of the file is reached or as required.
7. Close the `DataInputStream` and file input stream.
8. End the program.





## PROGRAM:
 ```
/*
Program to implement a Serialization and Deserialization using Java
Developed by: 
RegisterNumber:  
*/
```

## SOURCE CODE:

```
import java.io.*;
import java.util.Scanner;

public class DataInputStreamUTFExample {
    public static void main(String[] args) {
        String fileName = "utfdata.dat";
        Scanner scanner = new Scanner(System.in);

        try {
            // Take input from user
            String input = scanner.nextLine();

            // Write UTF string to file
            DataOutputStream dos = new DataOutputStream(new FileOutputStream(fileName));
            dos.writeUTF(input);
            dos.close();

            // Read UTF string from file
            DataInputStream dis = new DataInputStream(new FileInputStream(fileName));
            String readStr = dis.readUTF();
            dis.close();

            // Display result
            System.out.println("String read from file: " + readStr);

        } catch (IOException e) {
            System.out.println("Error: " + e.getMessage());
        } finally {
            scanner.close();
        }
    }
}
```





## OUTPUT:

<img width="991" height="247" alt="image" src="https://github.com/user-attachments/assets/84b1e323-f1fa-40ef-8e33-49d25df01912" />


## RESULT:
Thus java program executed successfully

