# Ex.No:4(B)  IMPLEMENT SOLID PRINCIPLES IN JAVA PROGRAM 

## QUESTION:
Welcome to MatchIt – a dating app that automatically notifies users when their preferred type of match joins the platform.


## **Aim**

To design a system for the MatchIt dating app that automatically notifies users when a new user joins the platform who matches their preferred criteria.



## **Algorithm**

1. Start the program.
2. Allow each user to set their preferred match criteria (e.g., age range, gender, interests).
3. Store user preferences in the system.
4. Whenever a new user registers, collect and store their profile details.
5. Compare the new user’s details with the stored preferences of all existing users.
6. For every user whose preference matches the new user, generate a notification event.
7. Send an automated notification to those users indicating a new potential match.
8. End the program.
	





## PROGRAM:
 ```
/*
Program to implement a SOLID Principles in Java Program
Developed by: 
RegisterNumber:  
*/
```

## SOURCE CODE:

```
import java.util.*;

interface Observer {
    void notifyNewUser(String newusername, String type);
    String getPreference();
}

class User implements Observer {
    //Type your code
    String name;
    String preference;
    
    public User(String name,String preference){
        this.name=name;
        this.preference=preference;
    }
    
    public String getPreference(){
        return preference;
    }
    public void notifyNewUser(String newusername,String type){
        System.out.println(name+": Omg! A new "+type+"? MatchIt, you know me too well! (It’s "+newusername+"!)");
    }
}


class MatchItServer {
    private List<Observer> users = new ArrayList<>();
    public void register(Observer user){
        users.add(user);
    }
    public void newSignup(String newusername,String type){
        System.out.println("New User Joined: "+newusername+" - Type: "+type);
        for(Observer u :users){
            if(u.getPreference().equalsIgnoreCase(type)){
                u.notifyNewUser(newusername,type);
            }
        }
    }
    
}

public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        MatchItServer server = new MatchItServer();

        int n = sc.nextInt();
        for (int i = 0; i < n; i++) {
            String name = sc.next();
            String pref = sc.next();
            server.register(new User(name,pref));
        }

        int m = sc.nextInt();
        for (int i = 0; i < m; i++) {
            String newUser = sc.next();
            String type = sc.next();
            server.newSignup(newUser,type);
        }
    }
}
import java.util.*;

interface Observer {
    void notifyNewUser(String newusername, String type);
    String getPreference();
}

class User implements Observer {
    //Type your code
    String name;
    String preference;
    
    public User(String name,String preference){
        this.name=name;
        this.preference=preference;
    }
    
    public String getPreference(){
        return preference;
    }
    public void notifyNewUser(String newusername,String type){
        System.out.println(name+": Omg! A new "+type+"? MatchIt, you know me too well! (It’s "+newusername+"!)");
    }
}


class MatchItServer {
    private List<Observer> users = new ArrayList<>();
    public void register(Observer user){
        users.add(user);
    }
    public void newSignup(String newusername,String type){
        System.out.println("New User Joined: "+newusername+" - Type: "+type);
        for(Observer u :users){
            if(u.getPreference().equalsIgnoreCase(type)){
                u.notifyNewUser(newusername,type);
            }
        }
    }
    
}

public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        MatchItServer server = new MatchItServer();

        int n = sc.nextInt();
        for (int i = 0; i < n; i++) {
            String name = sc.next();
            String pref = sc.next();
            server.register(new User(name,pref));
        }

        int m = sc.nextInt();
        for (int i = 0; i < m; i++) {
            String newUser = sc.next();
            String type = sc.next();
            server.newSignup(newUser,type);
        }
    }
}

```





## OUTPUT:

<img width="860" height="404" alt="image" src="https://github.com/user-attachments/assets/24d7a4ef-62a0-4597-a210-dcf23d33097d" />

<img width="718" height="404" alt="image" src="https://github.com/user-attachments/assets/a09b1b54-1d15-4181-9f31-fb1cb20b7701" />

## RESULT:
Thus java program executed successfully
