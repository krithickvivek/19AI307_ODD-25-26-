# Ex.No:2(E) ACCESS MODIFIERS

## QUESTION:
Create a class Utility with a static method square(int num) that returns the square of a number. Call the method without creating an object. 
## AIM:
To compute the square of a number using a static utility method.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read an integer value from the user using the Scanner class input.
4. Call the static square method from Utility directly without creating an object.
5. Inside the method, multiply the given number by itself and return result.
6. Print the returned squared value to display the final output clearly.

## PROGRAM:
 ```
/*
Program to implement a Access Modifiers using Java
Developed by: Krithick Vivekananda 
RegisterNumber: 212223240075
*/
```

## SOURCE CODE:
```
import java.util.Scanner;
class Utility
{
    static int square(int num)
    {
        return num*num;
    }
}
class prog
{
    public static void main(String[] args)
    {
        Scanner sc = new Scanner(System.in);
        int num = sc.nextInt();
        System.out.println(Utility.square(num));
    }
}
```
## OUTPUT:
| Input | Expected | Got | Status |
|-------|----------|-----|--------|
| 5     | 25       | 25  | ✓ |
| 0     | 0        | 0   | ✓ |
| -8    | 64       | 64  | ✓ |

**Passed all tests! ✓**



## RESULT:
Therefore, the program uses a static method to calculate and print the square of the given number without needing any object.
