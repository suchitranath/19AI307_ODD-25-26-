# Ex.No:5(C)  FILE HANDLING USING JAVA
## QUESTION:
Write a Java program to write a string to a text file named output.txt.
The user provides a single line of text, and the program writes it into the file.

## AIM:
To understand file handling in Java using FileWriter and to write user input into a text file.

## ALGORITHM :
1. Start the program.
2. Create a Scanner object to read input from the user.
3. Read a line of text (if available).
4. Create a FileWriter object with the filename "output.txt".
5. Write the input string into the file.
6. Close the FileWriter using try-with-resources.
7. Display a success message once writing is completed.
8. Handle any IOException errors.
9. End the program.





## PROGRAM:
 ```
/*
Program to implement a File Handling using Java
Developed by: SUCHITRA NATH
RegisterNumber: 212223220112
*/
```

```
import java.io.FileWriter;
import java.io.IOException;
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String text = "";

        // Read only if input exists
        if (sc.hasNextLine()) {
            text = sc.nextLine();
        }

        try (FileWriter writer = new FileWriter("output.txt")) {
            writer.write(text);
            System.out.println("Successfully wrote to the file.");
        } catch (IOException e) {
            System.out.println("An error occurred.");
        }
    }
}

```







## OUTPUT:
<img width="877" height="272" alt="image" src="https://github.com/user-attachments/assets/588ed801-2c2a-4263-93bc-5bb8f5d2a281" />



## RESULT:
The given text is successfully written into the file named output.txt.
Thus, writing a string to a file using FileWriter works correctly.
