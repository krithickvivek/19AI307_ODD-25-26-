# Ex.No:4(A) EXCEPTION HANDLING

## QUESTION:
Write a program that reads two integers and divides the first by the second. Handle the case when division by zero occurs.
## AIM:
To divide two integers and safely handle division by zero errors.
## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read two integer values from the user using the Scanner class input.
4. Use a try block to perform the division of the first number by the second.
5. If division by zero occurs, catch the ArithmeticException and print an error message.
6. If no exception occurs, print the computed result clearly to the user.

## PROGRAM:
 ```
/*
Program to implement a Exception Handling using Java
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
        int a , b;
        a = sc.nextInt();
        b = sc.nextInt();
        
        try
        {
            int c = a/b;
            System.out.println("Result: "+c);
        }
        catch( ArithmeticException e)
        {
            System.out.println("Error: Division by zero");
        }
        
    }
}
```


## OUTPUT:

| Test | Input        | Expected                   | Got                        | Status |
|------|--------------|----------------------------|----------------------------|--------|
| ✓    | 10<br>2      | Result: 5                  | Result: 5                  | ✓ |
| ✓    | 5<br>0       | Error: Division by zero    | Error: Division by zero    | ✓ |
| ✓    | 8<br>4       | Result: 2                  | Result: 2                  | ✓ |

**Passed all tests! ✓**


## RESULT:
Therefore, the program divides the given numbers and displays the result, or shows an error message when the second number is zero.
