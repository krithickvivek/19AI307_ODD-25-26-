# Ex.No:4(B)  IMPLEMENT SOLID PRINCIPLES IN JAVA PROGRAM 

## QUESTION:
In a gaming lounge, there is only one master console power switch that controls all gaming consoles. Whenever a player turns on any console, it internally triggers the master power. The master switch must ensure only one instance is ever created, regardless of how many times it's accessed, to prevent power fluctuations.

Every time a player accesses the master switch, it logs an access count. Since the switch is Singleton, the count should increment globally and reflect shared state.
## AIM:
To demonstrate a shared master switch using the Singleton pattern with access tracking.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read how many players will access the master switch and prepare the loop.
4. Retrieve the single MasterPowerSwitch instance using getInstance to ensure one object.
5. For each player name, call logAccess to increment and return global access count.
6. Print a message showing the player’s access and the updated shared access count.

## PROGRAM:
 ```
/*
Program to implement a SOLID Principles in Java Program
Developed by: Krithick Vivekananda 
RegisterNumber: 212223240075
*/
```

## SOURCE CODE:
```
import java.util.*;

class MasterPowerSwitch {
    private static MasterPowerSwitch instance = null;
    private int accessCount = 0;

    private MasterPowerSwitch() {}

    public static MasterPowerSwitch getInstance() {
        if (instance == null) {
            instance = new MasterPowerSwitch();
        }
        return instance;
    }

    public int logAccess() {
        accessCount++;
        return accessCount;
    }
}

public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        sc.nextLine();
        MasterPowerSwitch power = MasterPowerSwitch.getInstance();
        for (int i = 0; i < n; i++) {
            String player = sc.nextLine();
            int count = power.logAccess();
            System.out.println(player + " accessed Master Power Switch. Total accesses so far: " + count);
        }
    }
}
```
## OUTPUT:

| Input                   | Expected                                                                                              | Got                                                                                                   | Status |
|-------------------------|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|--------|
| 3<br>Alice<br>Bob<br>Charlie | Alice accessed Master Power Switch. Total accesses so far: 1<br>Bob accessed Master Power Switch. Total accesses so far: 2<br>Charlie accessed Master Power Switch. Total accesses so far: 3 | Alice accessed Master Power Switch. Total accesses so far: 1<br>Bob accessed Master Power Switch. Total accesses so far: 2<br>Charlie accessed Master Power Switch. Total accesses so far: 3 | ✓ |
| 1<br>Zara               | Zara accessed Master Power Switch. Total accesses so far: 1                                            | Zara accessed Master Power Switch. Total accesses so far: 1                                            | ✓ |

**Passed all tests! ✓**


## RESULT:
Therefore, the program ensures only one master switch exists, tracks every access globally, and displays the total count each time a player uses it.
