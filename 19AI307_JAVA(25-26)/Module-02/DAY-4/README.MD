# Ex.No:2(D) VARIABLE SCOPE AND CONSTRUCTOR

## QUESTION:
Write a class that uses a constructor to initialize variables and overrides toString() method.
## AIM:
To initialize object data using a constructor and display it using toString.
## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read the student’s name and age from the user using Scanner input.
4. Create an object by passing these values into the parameterized constructor.
5. Store the received values inside instance variables using the this keyword.
6. Override toString to return formatted details and print the object’s information.


## PROGRAM:
 ```
/*
Program to implement a Variable scope and Constructor using Java
Developed by: Krithick Vivekananda 
RegisterNumber: 212223240075
*/
```

## SOURCE CODE:
```
import java.util.*;
public class demo
{
    String name;
    int age;
    demo(String name, int age)
    {
        this.name=name;
        this.age=age;
    }
    public String toString()
    {
        return "Student{name='"+this.name+"', age="+this.age+"}";
    }
    public static void main(String[] args)
    {
        Scanner sc = new Scanner(System.in);
        String name = sc.next();
        int age = sc.nextInt();
        demo d = new demo(name,age);
        System.out.println(d.toString());
    }
}

```
## OUTPUT:

| Input        | Expected                                   | Got                                        | Status |
|--------------|---------------------------------------------|---------------------------------------------|--------|
| Manoj<br>25  | Student{name='Manoj', age=25}               | Student{name='Manoj', age=25}               | ✓ |
| Ram<br>20    | Student{name='Ram', age=20}                 | Student{name='Ram', age=20}                 | ✓ |
| Sam<br>23    | Student{name='Sam', age=23}                 | Student{name='Sam', age=23}                 | ✓ |

**Passed all tests! ✓**


## RESULT:
Therefore, the program initializes the object through its constructor and prints the formatted student details using the overridden toString method.
