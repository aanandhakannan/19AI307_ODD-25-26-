# Ex.No:4(C)  COMPOSITION IN JAVA

## QUESTION:

Implement a system where a Library contains multiple Book objects. Each Book is created inside the Library. Books can't exist independently

## **Aim**

To implement a system where a `Library` contains multiple `Book` objects, ensuring that each Book is created within the Library and cannot exist independently.



## **Algorithm**

1. Start the program.
2. Create a class **Library** to represent the collection of books.
3. Inside the Library class, define an inner class **Book**, so that Book objects can only be created through the Library.
4. Add attributes to the Book class such as title, author, or ID.
5. Provide a method inside Library (e.g., `addBook()`) that creates and stores new Book objects.
6. Maintain a list or array inside Library to store all created Book objects.
7. Ensure that Book objects cannot be created outside the Library by keeping the Book class private or nested.
8. Access and display the list of books through Library methods.
9. End the program.





## PROGRAM:
 ```
/*
Program to implement a Composition Concepts in Java
Developed by: 
RegisterNumber:  
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
    private Book[] books;
    private int count;

    public Library() {
        books = new Book[100];  
        count = 0;
    }

    public void addBook(String title, String author) {
        if (count < books.length) {
            books[count] = new Book(title, author);  
            count++;
        } else {
            System.out.println("Library is full, cannot add more books.");
        }
    }

    public void showBooks() {
        System.out.println("Books in Library:");
        for (int i = 0; i < count; i++) {
            System.out.println("- " + books[i].getDetails());
        }
    }
}

```





## OUTPUT:
<img width="905" height="532" alt="image" src="https://github.com/user-attachments/assets/6e50efc6-51c7-4988-a06d-d9029ae3e488" />



## RESULT:

Thus java program executed successfully
