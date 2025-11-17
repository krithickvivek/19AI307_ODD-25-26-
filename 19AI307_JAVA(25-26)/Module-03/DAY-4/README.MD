# Ex.No:3(D)  INTERFACE 

## QUESTION:
You are programming bots that analyze weather data. Each bot must implement a common interface and give a prediction.
- Bot Types:
 - SunBot: Predicts "HOT" if temperature > 30, else "MODERATE".
 - RainBot: Predicts "COLD" if temperature < 20, else "WARM".


## AIM:
To predict weather conditions using different bot types through abstraction.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read the temperature and bot type from the user using Scanner input.
4. Create the correct WeatherBot object depending on whether the user selects SunBot or RainBot.
5. Call the predict method to generate a weather prediction based on temperature rules.
6. Print the prediction returned by the selected bot for the given temperature.

## PROGRAM:
 ```
/*
Program to implement a Interface using Java
Developed by: Krithick Vivekananda 
RegisterNumber: 212223240075
*/
```

## SOURCE CODE:
```
import java.util.*;

abstract class WeatherBot {
    abstract String predict(int temperature);
}
class SunBot extends WeatherBot {
    String predict(int temperature) {
        return (temperature > 30) ? "HOT" : "MODERATE";
    }
}
class RainBot extends WeatherBot {
    String predict(int temperature) {
        return (temperature < 20) ? "COLD" : "WARM";
    }
}
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int temperature = sc.nextInt();
        int botType = sc.nextInt();

        WeatherBot bot = (botType == 1) ? new SunBot() : new RainBot();
        System.out.println(bot.predict(temperature));
    }
}

```

## OUTPUT:

| Input      | Expected | Got  | Status |
|------------|----------|------|--------|
| 35&nbsp;1  | HOT      | HOT  | ✓ |

**Passed all tests! ✓**


## RESULT:
Therefore, the program selects the appropriate bot, processes the temperature, and prints a weather prediction according to the bot’s logic.
