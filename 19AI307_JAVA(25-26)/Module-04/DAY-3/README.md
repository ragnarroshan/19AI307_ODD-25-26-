# Ex.No:4(C)  COMPOSITION IN JAVA

## AIM:
To write a Java program that demonstrates Composition by implementing a Library class that contains multiple Book objects.

## ALGORITHM :

1.Start the program.

2.Create Book and Library classes.

3.Read the number of books, along with their titles and authors.

4.Add each book to the library using the addBook() method.

5.Display all books in the library using the showBooks() method and stop the program.





## PROGRAM:
 ```
/*
Program to implement a Composition Concepts in Java
Developed by: KIRTHICK ROSHAN J
RegisterNumber:  212223040097
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

    public Book(String title, String author) {
        this.title = title;
        this.author = author;
    }

    public String getDetails() {
        return title + " by " + author;
    }
}

class Library {
    private List<Book> books = new ArrayList<>();

    public void addBook(String title, String author) {
        books.add(new Book(title, author));
    }

    public void showBooks() {
        System.out.println("Books in Library:");
        for (Book book : books) {
            System.out.println("- " + book.getDetails());
        }
    }
}
```






## OUTPUT:

<img width="787" height="472" alt="image" src="https://github.com/user-attachments/assets/b12ebf32-8317-4bc4-997c-40d300fa6183" />



## RESULT:
Thus, the program successfully demonstrates Composition, where a Library contains multiple Book objects and displays their details.
