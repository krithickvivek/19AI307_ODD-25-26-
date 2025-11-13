# Ex.No:1(B) CONDITIONAL STATEMENT

## QUESTION:
A dragon wakes based on temperature:
- If temperature < 0, it hibernates.
- If 0 ≤ temp ≤ 20, it snoozes.
- If 21 ≤ temp ≤ 35, it wakes.
- If temp > 35, it gets angry.
Write a java program to get the user input for temperature and display appropriate output.

## AIM:
To display the dragon’s state based on temperature using conditional checks.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read the temperature value from the user using Scanner input.
4. Check if temperature is below zero and print dragon is hibernating.
5. Check if temperature is between zero and twenty and print dragon snoozing.
6. Check if temperature lies between twenty-one and thirty-five and print awake.
7. If temperature exceeds thirty-five, print dragon becomes angry based on condition.

## PROGRAM:
 ```
/*
Program to implement a conditional statement using Java
Developed by: Krithick Vivekananda 
RegisterNumber: 212223240075
*/
```

## SOURCE CODE:
```
import java.util.*;
public class demo
{
    public static void main(String[] args)
    {
        Scanner sc = new Scanner(System.in);
        int temp = sc.nextInt();
        if(temp<0) System.out.println("Hibernating");   
        else if(temp>=0 && temp<=20) System.out.println("Snoozing");
        else if(temp>=21 && temp<=35) System.out.println("Awake");
        else System.out.println("Angry");
    }
}
```

## OUTPUT:
| Input | Expected   | Got         | Status |
|-------|------------|-------------|--------|
| -5    | Hibernating | Hibernating | ✓ |
| 15    | Snoozing    | Snoozing    | ✓ |
| 25    | Awake       | Awake       | ✓ |
| 40    | Angry       | Angry       | ✓ |

**Passed all tests! ✓**


## RESULT:
Therefore, the program reads the temperature and correctly displays the dragon’s state according to the given conditions.



