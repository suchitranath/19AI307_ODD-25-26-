# Ex.No:1(E) STRINGS AND MATH FUNCTION

## QUESTION:
Write a Java program to reverse a given string.

Example:
Input:
welcome

Output:
Reversed string: emoclew



## AIM:
To write a Java program that reads a string from the user and reverses it by traversing the characters in reverse order.



## ALGORITHM :
1. Start the program.
2. Create a Scanner object to read input from the user.
3. Read a string input from the user.
4. Initialize an empty string 'newstr' to store the reversed string.
5. Loop from the last character of the input string to the first:
       Append each character to 'newstr'.
6. Print the reversed string.
7. Close the scanner.
8. End the program.





## PROGRAM:
 ```
/*
Program to implement a Strings and Math Function using Java
Developed by: SUCHITRA NATH
RegisterNumber: 212223220112
*/
```

```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        String str = scanner.next();
        String newstr = "";

        for (int i = str.length() - 1; i >= 0; i--) {
            newstr += str.charAt(i);
        }

        System.out.println("Reversed string: " + newstr);

        scanner.close();
    }
}

```

## OUTPUT:
<img width="822" height="358" alt="image" src="https://github.com/user-attachments/assets/92835d9d-2d51-4fd2-8f4f-e6f988948fad" />



## RESULT:
Thus, the Java program to reverse a given string was executed successfully.



