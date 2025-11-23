# Ex.No:5(C)  FILE HANDLING USING JAVA
## QUESTION:

Write a program to count the number of words in a file


## **Aim**

To write a program that reads a file and counts the total number of words contained in it.



## **Algorithm**

1. Start the program.
2. Open the target file using a file reader or input stream.
3. Read the file content line by line.
4. For each line, split the text into words using space or whitespace delimiters.
5. Count the number of words in each line and add it to a total word counter.
6. Continue until the end of the file is reached.
7. Display the total word count.
8. Close the file.
9. End the program.





## PROGRAM:
 ```
/*
Program to implement a File Handling using Java
Developed by: 
RegisterNumber:  
*/
```

## SOURCE CODE:

```
import java.io.*;
import java.util.Scanner;

public class WordCountInFile {
    public static void main(String[] args) {
        String fileName = "words.txt";
        Scanner scanner = new Scanner(System.in);

        try {
            // Take input from user
            String input = scanner.nextLine();

            // Write input to file
            FileWriter writer = new FileWriter(fileName);
            writer.write(input);
            writer.close();

            // Read file and count words
            BufferedReader reader = new BufferedReader(new FileReader(fileName));
            String line;
            int wordCount = 0;

            while ((line = reader.readLine()) != null) {
                String[] words = line.trim().split("\\s+");
                if (!line.trim().isEmpty()) {
                    wordCount += words.length;
                }
            }
            reader.close();

            // Display result
            System.out.println("Number of words in the file: " + wordCount);

        } catch (IOException e) {
            System.out.println("Error: " + e.getMessage());
        } finally {
            scanner.close();
        }
    }
}
```





## OUTPUT:

<img width="1072" height="253" alt="image" src="https://github.com/user-attachments/assets/01bf9f02-d764-42d4-8f66-8fab2de36bcb" />


## RESULT:

Thus java program executes successfully.
