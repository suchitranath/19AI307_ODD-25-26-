# Ex.No:3(D)    INTERFACE 

## QUESTION:
You are programming bots that analyze weather data. Each bot must implement a 
common interface and give a prediction.

Bot Types:
1. SunBot: Predicts "HOT" if temperature > 30, else "MODERATE".
2. RainBot: Predicts "COLD" if temperature < 20, else "WARM".

Input:
temperature
botType (1 for SunBot, 2 for RainBot)

Output:
Print the prediction string based on the selected bot.



## AIM:
To develop a Java program that uses interfaces and polymorphism to generate weather predictions using different types of bots (SunBot and RainBot).



## ALGORITHM :
1. Start the program and read the temperature and bot type from the user.
2. Based on botType, create an object of either SunBot or RainBot.
3. Each bot implements the WeatherBot interface with its own predict() method.
4. Call the predict() method using the bot reference, passing the temperature.
5. Display the prediction returned by the selected bot.




## PROGRAM:
 ```
/*
Program to implement a Interface using Java
Developed by: SUCHITRA NATH
RegisterNumber: 212223220112
*/
```

```
import java.util.*;

interface WeatherBot {
    String predict(int temperature);
}

class SunBot implements WeatherBot {
    @Override
    public String predict(int temperature) {
        if (temperature > 30)
            return "HOT";
        else
            return "MODERATE";
    }
}

class RainBot implements WeatherBot {
    @Override
    public String predict(int temperature) {
        if (temperature < 20)
            return "COLD";
        else
            return "WARM";
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int temperature = sc.nextInt();
        int botType = sc.nextInt();

        WeatherBot bot;
        if (botType == 1) {
            bot = new SunBot();
        } else {
            bot = new RainBot();
        }

        System.out.println(bot.predict(temperature));
        sc.close();
    }
}

```







## OUTPUT:
<img width="942" height="263" alt="image" src="https://github.com/user-attachments/assets/edc3713c-6372-4f62-81c8-a422b76cbd50" />




## RESULT:
The program successfully reads the temperature and selects the correct bot 
based on user input. Using interface implementation, the selected bot predicts 
the weather condition and displays:

HOT / MODERATE / COLD / WARM

Thus, the Java program using interfaces and polymorphism for weather prediction 
executed successfully.


