# Ex.No:4(A) EXCEPTION HANDLING

## QUESTION:
Write a Java program that reads two integers from the user and divides the first number by the second. Handle the case when the second number is zero using 
exception handling so the program does not crash. If division by zero occurs, display an appropriate error message.


## AIM:
To write a Java program that performs division between two integers and uses exception handling (try–catch) to safely manage division by zero.


## ALGORITHM :
1. Start the program and read two integers from the user.
2. Place the division operation inside a try block.
3. Attempt to divide the first number by the second.
4. If b is zero, an ArithmeticException will be thrown and caught in the catch block.
5. Print the result if division is valid; otherwise print an error message for division by zero.




## PROGRAM:
 ```
/*
Program to implement a Exception Handling using Java
Developed by: SUCHITRA NATH
RegisterNumber: 212223220112
*/
```

```
import java.util.Scanner;

public class DivideNumbers {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        // Read two integers
        int a = scanner.nextInt();
        int b = scanner.nextInt();
        
        try {
            int result = a / b;
            System.out.println("Result: " + result);
        } catch (ArithmeticException e) {
            System.out.println("Error: Division by zero");
        }
    }
}

```







## OUTPUT:
<img width="855" height="410" alt="image" src="https://github.com/user-attachments/assets/a29c08bd-36e4-44a5-a6f4-f47efb491e2d" />



## RESULT:
The program successfully reads two integers and attempts to divide them.
If the second number is non-zero, the division result is displayed.
If division by zero occurs, the program catches the exception and prints:

Error: Division by zero

Thus, the Java program that handles division with exception handling 
executes successfully.

