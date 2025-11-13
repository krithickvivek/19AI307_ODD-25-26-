# Ex.No:1(A) INTRODUCTION TO JAVA PROGRAMMING, DATA TYPES, VARIABLES AND OPERATORS

## QUESTION:
Lovely has just started learning Java and is very excited about how to display messages on the screen. Her first mission is to understand how different types of print statements work 
- System.out.print() → prints on the same line
- System.out.println() → prints and moves to the next line
- System.out.printf() → prints formatted output
Your task is to help Lovely write a program that
## AIM:
To display user details using different Java print statement methods clearly.

## ALGORITHM :
1.	Read the user’s name, age, and decimal number using Scanner inputs.
2. Use print to show a greeting message without moving to next line.
3. Add a newline using println to display the user’s age clearly.
4. Use printf to format and print the favorite number with two decimals.
5. Ensure all outputs demonstrate correct usage of print, println, and printf methods.

## PROGRAM:
 ```
/*
Program to implement variables and Operators using Java
Developed by: Krithick Vivekananda
RegisterNumber: 212223240075
*/ 
```

## Sourcecode.java:

```
import java.util.*;
public class demo
{
    public static void main(String[] args)
    {
        Scanner sc = new Scanner(System.in);
        String name = sc.nextLine();
        int age = sc.nextInt();
        double fav = sc.nextDouble();
        System.out.print("Hello, "+name);
        System.out.println();
        System.out.println("You are "+age+" years old");
        System.out.printf("Your favorite number is %.2f",fav);
    }
}
```





## OUTPUT:
<img width="780" height="373" alt="image" src="https://github.com/user-attachments/assets/a441070f-76b2-4f28-861b-03b78fd694b8" />

## RESULT:
Therefore, the program successfully reads the user’s name, age, and decimal number, then displays a greeting using print, shows the age using println, and prints the favorite number in a formatted style using printf.
