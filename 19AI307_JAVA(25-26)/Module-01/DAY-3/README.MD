# Ex.No:1(C) LOOPING STATEMENT

## QUESTION:
Construct a right-angled triangle star pattern using for loop

## AIM:
To print a right-angled triangle star pattern using simple nested loops.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read an integer input from the user representing the triangle height.
4. Start a loop that runs from zero to one less than the input value.
5. For each row, run an inner loop to print stars equal to row index plus one.
6. After printing stars for a row, move the cursor to the next line.
7. Continue until all rows are printed, forming the required triangle pattern.

## PROGRAM:
 ```
/*
Program to implement a Looping Statement using Java
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
        int n=sc.nextInt();
        for(int i=0; i<n; i++)
        {
            for(int j=0; j<=i; j++)
            {
                System.out.print("* ");
            }
            System.out.println();
        }
    }
}
```

## OUTPUT:
| Input | Expected                                   | Got                                        | Status |
|-------|---------------------------------------------|---------------------------------------------|--------|
| 3     | *<br>* *<br>* * *                           | *<br>* *<br>* * *                           | ✓ |
| 5     | *<br>* * *<br>* * * *<br>* * * * *<br>* * * * * * | *<br>* * *<br>* * * *<br>* * * * *<br>* * * * * * | ✓ |
| 1     | *                                           | *                                           | ✓ |

**Passed all tests! ✓**


## RESULT:
Therefore, the program takes the number of rows and prints a right-angled star pattern correctly using nested loops.

