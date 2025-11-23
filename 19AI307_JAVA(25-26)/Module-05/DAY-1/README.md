# Ex.No:5(A) INPUTSTREAMREADER 

## QUESTION:
Write a program to create a log file where every user input is stored with a timestamp.


## **Aim**

To create a program that records every user input into a log file along with the current timestamp, ensuring all inputs are sequentially stored for tracking and auditing.



## **Algorithm**

1. Start the program.
2. Create or open a log file in append mode so old data is not overwritten.
3. Prompt the user to enter some input.
4. Read the user input from the console.
5. Get the current timestamp using the system’s date and time functions.
6. Write the timestamp followed by the user input into the log file.
7. Ask the user if they want to enter more data.
8. If yes, repeat steps 3–7; otherwise, stop logging.
9. Close the log file.
10. End the program.





## PROGRAM:
 ```
/*
Program to implement a InputStreamReader using Java
Developed by: 
RegisterNumber:  
*/
```

## SOURCE CODE:

```
import java.util.*;
import java.time.*;
import java.time.format.DateTimeFormatter;
import java.io.*;

public class Main{
    public static void main(String[] args){
        Scanner scan = new Scanner(System.in);
        String fileName = "user_log.txt";
        DateTimeFormatter dtf = DateTimeFormatter.ofPattern("yyyy-MM-dd HH:mm:ss");
        try{
            FileWriter fw = new FileWriter(fileName,true);
            BufferedWriter bw = new BufferedWriter(fw);
            PrintWriter pw = new PrintWriter(bw);
            
            while(true){
                String input = scan.nextLine();
                if(input.equalsIgnoreCase("exit")){
                    System.out.println("Logging stopped. Check user_log.txt");
                    break;
                } else {
                    String time = dtf.format(LocalDateTime.now());
                    pw.println(time+"-"+input);
                }
            }
            bw.close();
        }
        catch(IOException e){
            e.printStackTrace();
        }
        finally{
            scan.close();
        }
    }
}
```





## OUTPUT:

<img width="1041" height="394" alt="image" src="https://github.com/user-attachments/assets/e5776249-c778-4dc8-a773-85346350a35c" />


## RESULT:

Thus java program executed successfully.
