# Ex.No:2(A) CLASS AND OBJECT

## QUESTION:
Create a class Person with attributes name and age. Write a method greet() that prints: Hello, my name is <name> and I am <age> years old.

## AIM:
To create a Person class and display a greeting using attributes.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read the user’s name and age using Scanner and store the inputs.
4. Create a Person object by passing the name and age to the constructor.
5. Inside the constructor, assign the received values to the class attributes.
6. Call the greet method to print a message showing the person’s details.

## PROGRAM:
 ```
/*
Program to implement a Class and Objects using Java
Developed by: Krithick Vivekananda 
RegisterNumber:  212223240075
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

class prog {
    String name;
    int age;

    prog(String name, int age) {
        this.name = name;
        this.age = age;
    }

    void greet() {
       System.out.println("Hello, my name is "+this.name+" and I am "+this.age+" years old.");
    }

public static void main(String[] args) {
    Scanner sc = new Scanner(System.in);
    
    String name = sc.nextLine();
    int age = sc.nextInt();
    prog p = new prog(name,age);
    p.greet();
    }


}
```
## OUTPUT:
| Input        | Expected                                                             | Got                                                                  | Status |
|--------------|----------------------------------------------------------------------|-----------------------------------------------------------------------|--------|
| John<br>25   | Hello, my name is John and I am 25 years old.                       | Hello, my name is John and I am 25 years old.                       | ✓ |
| Alice<br>30  | Hello, my name is Alice and I am 30 years old.                      | Hello, my name is Alice and I am 30 years old.                      | ✓ |
| Saveeetha<br>20 | Hello, my name is Saveeetha and I am 20 years old.               | Hello, my name is Saveeetha and I am 20 years old.                  | ✓ |

**Passed all tests! ✓**

## RESULT:
Therefore, the program creates a Person object with the given details and prints a greeting message using its attributes.

