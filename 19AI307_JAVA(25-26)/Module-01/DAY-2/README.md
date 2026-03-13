# Ex.No:1(B) CONDITIONAL STATEMENT

## QUESTION:

A pirate ship has a code lock that only opens if:

The input code is even, and
        If it is less than 100, say "Weak Code".
        If it is between 100 and 999, say "Strong Code".
        If the code is odd, deny access.

For example:
Input 	Result

42      WEAK CODE


## AIM:
To write a Java program that reads a numeric code and checks whether it is an even or odd number.
The program should classify the code as Weak Code or Strong Code based on its range, and deny access for invalid or odd codes.

## ALGORITHM :

1. Start the program.
2. Create a Scanner object to read input from the user.
3. Read an integer value from the user.
4. Check if the number is even:
       a. If even and less than 100, print "WEAK CODE".
       b. If even and between 100 and 999, print "STRONG CODE".
       c. If even but greater than 999, print "ACCESS DENIED".
5. If the number is odd, print "ACCESS DENIED".
6. Close the scanner.
7. End the program.



## PROGRAM:
 ```
/*
Program to implement a conditional statement using Java
Developed by: SUCHITRA NATH
RegisterNumber: 212223220112
*/
```
```
import java.util.Scanner;
public class Main{
    public static void main(String[] args){
        Scanner scanner =  new Scanner(System.in);
        
        int a = scanner.nextInt();
        
        if(a<100){
            System.out.println("Weak Code");
        }else if(a%2!=0){
            System.out.println("Access Denied");
            }else if(a>999){
            System.out.println("Access Denied");
        }else{
            System.out.println("Strong Code");
        }
        
        scanner.close();
    }
}
```


## OUTPUT:

<img width="490" height="402" alt="image" src="https://github.com/user-attachments/assets/774f0c62-fade-498b-99d8-0f377bf8b741" />


## RESULT:
Thus, the Java program to check the pirate ship code and classify it as WEAK CODE, STRONG CODE, or ACCESS DENIED based on the given conditions was executed successfully.



