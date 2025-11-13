# Ex.No:1(E) STRINGS AND MATH FUNCTION

## QUESTION:


## AIM:
To reverse a user-given string using a simple character-by-character loop.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read the input string from the user using the Scanner object.
4. Create an empty string to store the reversed characters step by step.
5. Loop from the last character to the first and keep appending each one.
6. Print the fully reversed string after completing the loop operation.

## PROGRAM:
 ```
/*
Program to implement a Strings and Math Function using Java
Developed by: Krithick Vivekananda 
RegisterNumber: 212223240075
*/
```

## SOURCE CODE:
```import java.util.*;
public class A
{
    public static void main(String[] args)
    {
        Scanner sc = new Scanner(System.in);
        String str = sc.next();
        String reversed = "";
        for (int i = str.length() - 1; i >= 0; i--) {
            reversed += str.charAt(i);
        }
        System.out.println("Reversed string: "+reversed);
    }
}
```

## OUTPUT:
| Input   | Expected                        | Got                             | Status |
|---------|----------------------------------|----------------------------------|--------|
| hello   | Reversed string: olleh          | Reversed string: olleh          | ✓ |
| welcome | Reversed string: emoclew        | Reversed string: emoclew        | ✓ |
| orange  | Reversed string: egnaro         | Reversed string: egnaro         | ✓ |

**Passed all tests! ✓**



## RESULT:
Therefore, the program takes the input string, reverses it using a backward loop, and displays the reversed output correctly.
