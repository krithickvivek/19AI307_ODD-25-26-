# Ex.No:5(B) SERIALIZATION AND DESERIALIZATION 

## QUESTION:
Write a Java program to serialize a collection of objects (like ArrayList<Student>) into a file.
## AIM:
To serialize and deserialize a list of student objects using Java I/O.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read student details from user input and store them in an ArrayList.
4. Use ObjectOutputStream to serialize and save the entire list into a file.
5. Use ObjectInputStream to read the file and deserialize the stored student list.
6. Print each restored Student object to confirm successful serialization and retrieval.
## PROGRAM:
 ```
/*
Program to implement a Serialization and Deserialization using Java
Developed by: Krithick Vivekananda 
RegisterNumber:  212223240075
*/
```

## SOURCE CODE:
```
import java.io.*;
import java.util.*;

// Student class must implement Serializable
class Student implements Serializable {
    private static final long serialVersionUID = 1L;

    private int id;
    private String name;
    private double marks;

    public Student(int id, String name, double marks) {
        this.id = id;
        this.name = name;
        this.marks = marks;
    }

    @Override
    public String toString() {
        return "Student{id=" + id + ", name='" + name + "', marks=" + marks + "}";
    }
}

public class StudentSerializationUserInput {

    // Serialize list of students
    public static void serializeStudents(List<Student> students, String fileName) {
        try (ObjectOutputStream oos = new ObjectOutputStream(new FileOutputStream(fileName))) {
            oos.writeObject(students);
            System.out.println("Students serialized successfully into: " + fileName);
        } catch (IOException e) {
            System.out.println("Error during serialization: " + e.getMessage());
        }
    }

    // Deserialize list of students
    @SuppressWarnings("unchecked")
    public static List<Student> deserializeStudents(String fileName) {
        List<Student> students = null;
        try (ObjectInputStream ois = new ObjectInputStream(new FileInputStream(fileName))) {
            students = (List<Student>) ois.readObject();
            System.out.println("Students deserialized successfully from: " + fileName);
        } catch (IOException | ClassNotFoundException e) {
            System.out.println("Error during deserialization: " + e.getMessage());
        }
        return students;
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        List<Student> students = new ArrayList<>();

        int n = scanner.nextInt();
        scanner.nextLine(); // consume newline

        for(int i=0 ; i<n ; i++)
        {
            int id = scanner.nextInt();
            scanner.nextLine();
            String name = scanner.nextLine();
            double marks = scanner.nextDouble();
            scanner.nextLine();
            students.add(new Student(id,name,marks));
        }
        
        String fileName = "students.dat";
        serializeStudents(students,fileName);
        List<Student> deserializedStudents = deserializeStudents(fileName);
        // Display deserialized data
        if (deserializedStudents != null) {
            System.out.println("\nDeserialized Students:");
            for (Student s : deserializedStudents) {
                System.out.println(s);
            }
        }

        scanner.close();
    }
}

```






## OUTPUT:
| Input | Expected | Got | Status |
|-------|----------|------|--------|
| 2<br>101<br>Alice<br>89.5<br>102<br>Bob<br>92.0 | Students serialized successfully into: students.dat<br>Students deserialized successfully from: students.dat<br><br>Deserialized Students:<br>Student{id=101, name='Alice', marks=89.5}<br>Student{id=102, name='Bob', marks=92.0} | Students serialized successfully into: students.dat<br>Students deserialized successfully from: students.dat<br><br>Deserialized Students:<br>Student{id=101, name='Alice', marks=89.5}<br>Student{id=102, name='Bob', marks=92.0} | ✓ |
| 1<br>1<br>Manoj<br>95.6 | Students serialized successfully into: students.dat<br>Students deserialized successfully from: students.dat<br><br>Deserialized Students:<br>Student{id=1, name='Manoj', marks=95.6} | Students serialized successfully into: students.dat<br>Students deserialized successfully from: students.dat<br><br>Deserialized Students:<br>Student{id=1, name='Manoj', marks=95.6} | ✓ |
| 0 | Students serialized successfully into: students.dat<br>Students deserialized successfully from: students.dat<br><br>Deserialized Students: | Students serialized successfully into: students.dat<br>Students deserialized successfully from: students.dat<br><br>Deserialized Students: | ✓ |
| 3<br>101<br>Alice<br>89.5<br>102<br>Bob<br>92.0<br>103<br>Charlie<br>76.3 | Students serialized successfully into: students.dat<br>Students deserialized successfully from: students.dat<br><br>Deserialized Students:<br>Student{id=101, name='Alice', marks=89.5}<br>Student{id=102, name='Bob', marks=92.0}<br>Student{id=103, name='Charlie', marks=76.3} | Students serialized successfully into: students.dat<br>Students deserialized successfully from: students.dat<br><br>Deserialized Students:<br>Student{id=101, name='Alice', marks=89.5}<br>Student{id=102, name='Bob', marks=92.0}<br>Student{id=103, name='Charlie', marks=76.3} | ✓ |

**Passed all tests! ✓**



## RESULT:
Therefore, the program successfully stores a collection of Student objects in a file through serialization and later retrieves them correctly using deserialization, demonstrating persistent object storage.

