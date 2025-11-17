# Ex.No:5(C)  FILE HANDLING USING JAVA
## QUESTION:
Write a Java program to write a string to a text file named output.txt.
## AIM:
To write a sample text string into a file using FileWriter.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a FileWriter object pointing to a file named output.txt.
4. Use the write() method to store a sample string into the file.
5. Close the FileWriter to ensure the text is saved properly.
6. Display a success message or catch exceptions for error handling.





## PROGRAM:
 ```
/*
Program to implement a File Handling using Java
Developed by: Krithick Vivekananda 
RegisterNumber: 212223240075
*/
```

## SOURCE CODE:
```
import java.io.FileWriter;
import java.io.IOException;

public class WriteToFile {
    public static void main(String[] args) {
        try {
            FileWriter writer = new FileWriter("output.txt");
            writer.write("This is a sample text.");
            writer.close();
            System.out.println("Successfully wrote to the file.");
        } catch (IOException e) {
            System.out.println("An error occurred.");
        }
    }
}

```






## OUTPUT:
| Expected                              | Got                                  | Status |
|----------------------------------------|---------------------------------------|--------|
| Successfully wrote to the file.        | Successfully wrote to the file.       | ✓ |

**Passed all tests! ✓**



## RESULT:
Therefore, the program successfully writes the given string into output.txt and confirms the operation through a printed message.
