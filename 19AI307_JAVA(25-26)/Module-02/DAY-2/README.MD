# Ex.No:2(B) METHODS

## QUESTION:
Write a method named displayMessage() that prints "Welcome to Java Methods!". Call this method from the main() method.
## AIM:
To create and call a method that prints a welcome message clearly.
## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Define a method named displayMessage that prints a fixed welcome message.
4. Inside the main method, create an object of the demo class.
5. Use the created object to call the displayMessage method from main.
6. Execute the program to show the printed welcome message on the screen.
## PROGRAM:
 ```
/*
Program to implement a Methods using Java
Developed by: Krithick Vivekananda 
RegisterNumber: 212223240075
*/
```

## SOURCE CODE:
```
public class demo
{
    void displayMessage()
    {
        System.out.println("Welcome to Java Methods!");
    }
    public static void main(String[] args)
    {
        demo d = new demo();
        d.displayMessage();
    }
}
```
## OUTPUT:

| Expected                     | Got                          | Status |
|-----------------------------|-------------------------------|--------|
| Welcome to Java Methods!    | Welcome to Java Methods!      | ✓ |

**Passed all tests! ✓**


## RESULT:
Therefore, the program successfully calls the displayMessage method and prints the welcome message as intended.

