# Ex.No:3(A) INHERITANCE AND AGGREGATION

## QUESTION:
Create a Super class Person with fields name and age. Create a subclass Student that inherits from Person and adds a field marks (integer). Implement a method in Student called calculateGrade() which returns the grade based on the marks:
- Marks ≥ 90: Grade A
- Marks ≥ 75 and < 90: Grade B
- Marks ≥ 50 and < 75: Grade C
- Marks < 50: Grade F
## AIM:
To calculate a student’s grade using inheritance and a simple grading method.
## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read the student’s name, age, and marks from user input using Scanner.
4. Create a Student object that calls the Person constructor using super.
5. Use calculateGrade to determine grade by checking the student’s marks range.
6. Call the display method to print name, age, marks, and calculated grade.

## PROGRAM:
 ```
/*
Program to implement a Inheritance and Aggregation using Java
Developed by: Krithick Vivekananda 
RegisterNumber: 212223240075
*/
```

## SOURCE CODE:
```
import java.util.*;
class Person {
    String name;
    int age;

    Person(String name, int age) {
        this.name = name;
        this.age = age;
    }
}

class Student extends Person {
    int marks;

    Student(String name, int age, int marks) {
        super(name, age);
        this.marks = marks;
    }

    String calculateGrade() {
        if (marks >= 90) {
            return "A";
        } else if (marks >= 75) {
            return "B";
        } else if (marks >= 50) {
            return "C";
        } else {
            return "F";
        }
    }

    void display() {
        System.out.println("Name: " + name);
        System.out.println("Age: " + age);
        System.out.println("Marks: " + marks);
        System.out.println("Grade: " + calculateGrade());
        System.out.println();
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Student s1 = new Student(sc.next(),sc.nextInt(),sc.nextInt());
        s1.display();

    }
}

```

## OUTPUT:
| Test   | Input                     | Expected                                                    | Got                                                         | Status |
|--------|---------------------------|--------------------------------------------------------------|--------------------------------------------------------------|--------|
| Jeeva  | Jeeva<br>18<br>95         | Name: Jeeva<br>Age: 18<br>Marks: 95<br>Grade: A             | Name: Jeeva<br>Age: 18<br>Marks: 95<br>Grade: A             | ✓ |
| Alice  | Alice<br>20<br>80         | Name: Alice<br>Age: 20<br>Marks: 80<br>Grade: B             | Name: Alice<br>Age: 20<br>Marks: 80<br>Grade: B             | ✓ |
| Bob    | Bob<br>19<br>60           | Name: Bob<br>Age: 19<br>Marks: 60<br>Grade: C               | Name: Bob<br>Age: 19<br>Marks: 60<br>Grade: C               | ✓ |
| Eve    | Eve<br>21<br>45           | Name: Eve<br>Age: 21<br>Marks: 45<br>Grade: F               | Name: Eve<br>Age: 21<br>Marks: 45<br>Grade: F               | ✓ |

**Passed all tests! ✓**


## RESULT:
Therefore, the program creates a Student object using inheritance, computes the grade from marks, and prints all the student details correctly.
