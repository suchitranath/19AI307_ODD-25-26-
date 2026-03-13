# Ex.No:1(C) LOOPING STATEMENT

## QUESTION:
Write a Java program to calculate the factorial of a number using a for loop. The factorial of n is the product of all positive integers less than or equal to n.

## AIM:
To write a Java program that calculates the factorial of a given number using a for loop. The factorial of a number n is defined as the product of all positive integers from 1 to n.


## ALGORITHM :
```
1. Start the program.
2. Create a Scanner object to read an integer from the user.
3. Read the input number 'a'.
4. Initialize a variable 'fact' to 1.
5. Use a for loop from i = 1 to i = a:
       Multiply 'fact' by 'i' in each iteration.
6. After the loop ends, print the factorial of the number.
7. Close the scanner.
8. End the program.

```
## PROGRAM:
 ```
/*
Program to implement a Looping Statement using Java
Developed by: SUCHITRA NATH
RegisterNumber: 212223220112
*/
```

```
import java.util.Scanner;
public class Main{
    public static void main(String[] args){
        Scanner scanner = new Scanner(System.in);
        
        int a = scanner.nextInt();
        
        int fact = 1;
        
        for(int i = 1; i <= a; i++){
            fact *= i;
        }
        
        System.out.println("Factorial of " + a + " is: " + fact);
        
        scanner.close();
    }
}

```







## OUTPUT:
<img width="965" height="355" alt="image" src="https://github.com/user-attachments/assets/08992ed6-2ef6-4e4a-959c-ce69bec93c21" />



## RESULT:
Thus, the Java program to calculate the factorial of a number using a for loop was executed successfully.


