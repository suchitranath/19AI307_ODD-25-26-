# Ex.No:4(C)  COMPOSITION IN JAVA

## QUESTION:
Implement a system where a Library contains multiple Book objects.
Each Book must be created inside the Library, meaning a Book cannot exist 
without the Library (Composition in OOP).

Input:
n
[BookTitle1]
[Author1]
[BookTitle2]
[Author2]
...

Output:
Books in Library:
- [Title] by [Author]


## AIM:
To implement the concept of Composition in Java by creating a Library class that owns and manages Book objects. Books are created only inside the Library 
and cannot exist independently.


## ALGORITHM :
1. Create a Book class with title and author as attributes, but make it usable 
   only inside the Library (inner class or created from Library).

2. Create a Library class that contains a list of Book objects.

3. Provide a method in Library to add new Book objects using title and author.

4. In the main method, read 'n' number of books and use the Library's method to 
   create and store Book objects.

5. Finally, display all books stored inside the Library.





## PROGRAM:
 ```
/*
Program to implement a Composition Concepts in Java
Developed by: SUCHITRA NATH
RegisterNumber: 212223220112
*/
```

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
    private List<Book> books = new ArrayList<>();  // Library owns the books

    public void addBook(String title, String author) {
        books.add(new Book(title, author));  // Composition: Book created inside Library
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
<img width="995" height="628" alt="image" src="https://github.com/user-attachments/assets/d7f39596-2115-4e2b-a387-087d825ba8a2" />



## RESULT:
The program successfully demonstrates Composition in Java.
All Book objects are created only inside the Library class and cannot exist independently. The library stores the list of books and displays them 
as required.

Thus, the Java program implementing Composition between Library and Book executed successfully.

