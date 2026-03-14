# Ex.No:2(A) CLASS AND OBJECT

## QUESTION:
Create a class Calculator with methods:
add(a, b), subtract(a, b), multiply(a, b), divide(a, b)
that return the result of the operation.

Example:
Input:
10
2

Output:
12
8
20
5.0



## AIM:
To write a Java program that demonstrates the concept of classes and methods by creating a Calculator class with basic arithmetic operations: addition, subtraction, multiplication, and division.



## ALGORITHM :
1. Start the program.
2. Create a class 'prog' with the following methods:
       add(a, b)      → returns a + b
       subtract(a, b) → returns a - b
       multiply(a, b) → returns a * b
       divide(a, b)   → returns a / b as a double
3. In the main method:
       a. Create a Scanner object to read two integers from the user.
       b. Create an object of the 'prog' class.
       c. Call each method (add, subtract, multiply, divide)
          with the entered values.
       d. Print the results of each operation.
4. Close the scanner.
5. End the program.
	





## PROGRAM:
 ```
/*
Program to implement a Class and Objects using Java
Developed by: SUCHITRA NATH 
RegisterNumber: 212223220112
*/
```
```
import java.util.Scanner;

class prog {

    int add(int a, int b) {
        return a + b;
    }

    int subtract(int a, int b) {
        return a - b;
    }

    int multiply(int a, int b) {
        return a * b;
    }

    double divide(int a, int b) {
        return (double) a / b;
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        int a = scanner.nextInt();
        int b = scanner.nextInt();

        prog obj = new prog();

        System.out.println(obj.add(a, b));
        System.out.println(obj.subtract(a, b));
        System.out.println(obj.multiply(a, b));
        System.out.println(obj.divide(a, b));

        scanner.close();
    }
}

```


## OUTPUT:

<img width="950" height="678" alt="image" src="https://github.com/user-attachments/assets/394452c4-c9ca-4761-9066-48eae0959412" />


## RESULT:
Thus, the Java program demonstrating arithmetic operations using a Calculator class was executed successfully.



