# Ex.No:4(C)  COMPOSITION IN JAVA

## QUESTION:
Implement a system where a Library contains multiple Book objects. Each Book is created inside the Library. Books can't exist independently (Composition).
## AIM:
To demonstrate composition by creating books inside a library that owns them.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read the number of books and loop to input each title and author.
4. Use the library object to add new books, creating them inside the library.
5. Store each created Book in the library’s internal list representing composition.
6. Display all stored books by printing their details from the library object.

## PROGRAM:
 ```
/*
Program to implement a Composition Concepts in Java
Developed by: Krithick Vivekananda 
RegisterNumber: 212223240075
*/
```

## SOURCE CODE:
```
import java.util.*;

public class CompositionExample {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Library library = new Library();
        int n = sc.nextInt();
        sc.nextLine();
        for (int i = 0; i < n; i++) {
            String title = sc.nextLine();
            String author = sc.nextLine();
            library.addBook(title, author);
        }
        library.showBooks();
        sc.close();
    }
}

class Book {
    private String title;
    private String author;

    Book(String title, String author) {
        this.title = title;
        this.author = author;
    }

    String getDetails() {
        return "- " + title + " by " + author;
    }
}

class Library {
    private List<Book> books;

    Library() {
        books = new ArrayList<>();
    }

    void addBook(String title, String author) {
        books.add(new Book(title, author));
    }

    void showBooks() {
        System.out.println("Books in Library:");
        for (Book b : books)
            System.out.println(b.getDetails());
    }
}
```
## OUTPUT:
| Input | Expected | Got | Status |
|-------|----------|------|--------|
| 2<br>Java<br>James Gosling<br>Python<br>Guido Van Rossum | Books in Library:<br>- Java by James Gosling<br>- Python by Guido Van Rossum | Books in Library:<br>- Java by James Gosling<br>- Python by Guido Van Rossum | ✓ |
| 1<br>Machine Learning<br>Andrew Ng | Books in Library:<br>- Machine Learning by Andrew Ng | Books in Library:<br>- Machine Learning by Andrew Ng | ✓ |
| 3<br>C<br>Dennis Ritchie<br>C++<br>Bjarne Stroustrup<br>Rust<br>Graydon | Books in Library:<br>- C by Dennis Ritchie<br>- C++ by Bjarne Stroustrup<br>- Rust by Graydon | Books in Library:<br>- C by Dennis Ritchie<br>- C++ by Bjarne Stroustrup<br>- Rust by Graydon | ✓ |

**Passed all tests! ✓**



## RESULT:
Therefore, the program shows how a library fully owns its books through composition and prints every book added.
