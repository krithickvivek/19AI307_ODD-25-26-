# Ex.No:4(D) DESIGN PATTERN -- ABSTRACT FACTORY

## QUESTION:
You are asked to simulate a simple Shape Drawing Tool using the Factory Design Pattern in Java.

You will implement a Shape interface with concrete classes for different shapes (Circle, Square, Rectangle). Using a ShapeFactory, your program will take shape names from user input and draw them accordingly. If the shape is unknown, print an error message.

## AIM:
To draw shapes using a factory and handle unknown shape names.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read shape names one per line until the user types the word exit.
4. Convert the input to a normalized form and ask ShapeFactory for an object.
5. If factory returns a Shape, call its draw method to print output.
6. If factory returns null, print an “Invalid shape: <input>” error message.
## PROGRAM:
 ```
/*
Program to implement a Abstract Factory Pattern using Java
Developed by: Krithick Vivekananda 
RegisterNumber: 212223240075 
*/
```

## SOURCE CODE:
```
import java.util.*;

interface Shape
{
    void draw();
}

class Circle implements Shape
{
    public void draw()
    {
        System.out.println("Drawing Circle");
    }
}

class Square implements Shape
{
    public void draw()
    {
        System.out.println("Drawing Square");
    }
}

class Rectangle implements Shape
{
    public void draw()
    {
        System.out.println("Drawing Rectangle");
    }
}

class ShapeFactory
{
    public Shape getShape(String shapeType)
    {
        if (shapeType == null)
        {
            return null;
        }
        shapeType = shapeType.toLowerCase();
        if (shapeType.equals("circle"))
        {
            return new Circle();
        }
        else if (shapeType.equals("square"))
        {
            return new Square();
        }
        else if (shapeType.equals("rectangle"))
        {
            return new Rectangle();
        }
        else
        {
            return null;
        }
    }
}

public class prog
{
    public static void main(String[] args)
    {
        Scanner sc = new Scanner(System.in);
        ShapeFactory factory = new ShapeFactory();
        while (true)
        {
            if (!sc.hasNext())
            {
                break;
            }
            String input = sc.nextLine().trim();
            if (input.equalsIgnoreCase("exit"))
            {
                break;
            }
            Shape shape = factory.getShape(input);
            if (shape != null)
            {
                shape.draw();
            }
            else
            {
                System.out.println("Invalid shape: " + input);
            }
        }
    }
}

```

## OUTPUT:

| Input                                           | Expected                                                                 | Got                                                                     | Status |
|-------------------------------------------------|-------------------------------------------------------------------------|-------------------------------------------------------------------------|--------|
| circle<br>square<br>rectangle<br>exit           | Drawing Circle<br>Drawing Square<br>Drawing Rectangle                   | Drawing Circle<br>Drawing Square<br>Drawing Rectangle                   | ✓ |
| triangle<br>circle<br>hexagon<br>exit           | Invalid shape: triangle<br>Drawing Circle<br>Invalid shape: hexagon     | Invalid shape: triangle<br>Drawing Circle<br>Invalid shape: hexagon     | ✓ |
| Circle<br>SQUARE<br>RectAngle<br>Exit           | Drawing Circle<br>Drawing Square<br>Drawing Rectangle                   | Drawing Circle<br>Drawing Square<br>Drawing Rectangle                   | ✓ |

**Passed all tests! ✓**


## RESULT:
Therefore, the program uses a ShapeFactory to produce shape objects, draws known shapes, and reports unknown shapes as errors.
