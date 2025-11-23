# Ex.No:3(D)    INTERFACE 

## QUESTION:
You are programming bots that analyze weather data. Each bot must implement a common interface and give a prediction.


## **Aim**

To design multiple weather-analyzing bots where each bot implements a common interface and provides its own version of a weather prediction.



## **Algorithm**

1. Start the program.
2. Create an interface **WeatherBot** with an abstract method (e.g., `predictWeather()`).
3. Create multiple classes (e.g., `RainBot`, `HeatBot`, `WindBot`) that implement the WeatherBot interface.
4. In each class, provide a different implementation of the `predictWeather()` method.
5. In the main program, create objects of each bot class.
6. Call the `predictWeather()` method on each object to display different predictions.
7. End the program.




## PROGRAM:
 ```
/*
Program to implement a Interface using Java
Developed by: 
RegisterNumber:  
*/
```

## SOURCE CODE:

```
import java.util.*;

interface WeatherBot{
    String forecast(int temperature);
}

class SunnyBot implements WeatherBot{
    public String forecast(int temperature){
        return temperature > 30 ? "HOT" : "MODERATE";
    }
}

class RainyBot implements WeatherBot{
    public String forecast(int temperature){
        return temperature < 20 ? "COLD" : "WARM";
    }
}

public class prog {
    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);
        int temp = scan.nextInt();
        int type = scan.nextInt();
        WeatherBot W;
        if(type==1){
            W = new SunnyBot();
        }
        else{
            W = new RainyBot();
        }
        System.out.print(W.forecast(temp));
    }
}
```





## OUTPUT:

<img width="487" height="170" alt="image" src="https://github.com/user-attachments/assets/498abe09-4a1b-4eac-b5af-fc170ec0cb1a" />


## RESULT:

Thus java program executed successfully.

