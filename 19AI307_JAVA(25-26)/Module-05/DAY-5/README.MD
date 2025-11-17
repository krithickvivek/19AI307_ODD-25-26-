# Ex.No:5(E) MULTITHREADING -SYNCHRONIZATION

## QUESTION:
Maintain two int variables a and b, read their initial values from user. Use synchronized block to swap them and print swapped values.

## AIM:
To swap two integers safely using a synchronized block in Java.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read two integer values from the user representing variables a and b.
4. Create a lock object to use inside the synchronized block.
5. Enter the synchronized block and swap values of a and b using a temporary variable.
6. Print the swapped values of both variables after exiting the synchronized block.


## PROGRAM:
 ```
/*
Program to implement a Synchronization concept using Java
Developed by: Krithick Vivekananda 
RegisterNumber: 212223240075
*/
```

## SOURCE CODE:

```
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int a = sc.nextInt();
        int b = sc.nextInt();

        Object lock = new Object();

        synchronized(lock) {
            int temp = a;
            a = b;
            b = temp;
        }

        System.out.println("a = " + a);
        System.out.println("b = " + b);
    }
}

```

## OUTPUT:
| Input        | Expected        | Got             | Status |
|--------------|-----------------|------------------|--------|
| 5<br>10      | a = 10<br>b = 5 | a = 10<br>b = 5  | ✓ |
| 100<br>200   | a = 200<br>b = 100 | a = 200<br>b = 100 | ✓ |
| -1<br>8      | a = 8<br>b = -1 | a = 8<br>b = -1  | ✓ |

**Passed all tests! ✓**



## RESULT:
Therefore, the program safely swaps the values of a and b inside a synchronized block and prints the updated results.
