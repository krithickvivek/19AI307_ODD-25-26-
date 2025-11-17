# Ex.No:3(b) POLYMORPHISM

## QUESTION:
Write a Java program that calculates the area of different shapes using method overloading. Create a class AreaCalculator with:
- area(int side) for square
- area(int length, int breadth) for rectangle
- area(double radius) for circle

## AIM:
To compute areas of multiple shapes using method overloading in Java.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read inputs for the square side, rectangle dimensions, and circle radius from user.
4. Create an AreaCalculator object to access overloaded area methods.
5. Call the correct area method based on parameters for each shape input.
6. Print the calculated areas for square, rectangle, and circle in separate lines.

## PROGRAM:
 ```
/*
Program to implement a Polymorphism using Java
Developed by: Krithick Vivekananda 
RegisterNumber: 212223240075
*/
```

## SOURCE CODE:

```
import java.util.Scanner;

class AreaCalculator {
    public int area(int side) {
        return side * side;
    }

    public int area(int length, int breadth) {
        return length * breadth;
    }

    public double area(double radius) {
        return Math.PI * radius * radius;
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        AreaCalculator calc = new AreaCalculator();

        int squareSide = sc.nextInt();
        int rectLength = sc.nextInt();
        int rectBreadth = sc.nextInt();
        double circleRadius = sc.nextDouble();

        System.out.println("Area of square: " + calc.area(squareSide));
        System.out.println("Area of rectangle: " + calc.area(rectLength, rectBreadth));
        System.out.println("Area of circle: " + calc.area(circleRadius));

        sc.close();
    }
}

```


## OUTPUT:
| Input                  | Expected                                                                 | Got                                                                      | Status |
|------------------------|---------------------------------------------------------------------------|---------------------------------------------------------------------------|--------|
| 4<br>5<br>6<br>3.0     | Area of square: 16<br>Area of rectangle: 30<br>Area of circle: 28.274333882308138 | Area of square: 16<br>Area of rectangle: 30<br>Area of circle: 28.274333882308138 | ✓ |
| 7<br>2<br>3<br>2.5     | Area of square: 49<br>Area of rectangle: 6<br>Area of circle: 19.634954084936208  | Area of square: 49<br>Area of rectangle: 6<br>Area of circle: 19.634954084936208  | ✓ |
| 5<br>3<br>9<br>9.8     | Area of square: 25<br>Area of rectangle: 27<br>Area of circle: 301.7185584507638  | Area of square: 25<br>Area of rectangle: 27<br>Area of circle: 301.7185584507638  | ✓ |

**Passed all tests! ✓**



## RESULT:
Therefore, the program uses overloaded methods to calculate and display the areas of a square, rectangle, and circle based on the user’s inputs.
