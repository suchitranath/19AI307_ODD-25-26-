# Ex.No:2(E) ACCESS MODIFIERS

## QUESTION:
Create a class Calculator with:
1. One non-static method add(int a, int b) that returns the sum.
2. One static method info() that displays "Calculator is ready".

Read two integers from the user, call the static method using the class name, and call the non-static method using an object. Display the result.


## AIM:
To write a Java program that demonstrates the concept of static and non-static methods using a Calculator class. The Calculator class contains a static method info() to display the readiness message and a non-static method add(int a, int b) to return the sum of two integers. The program reads two integers from the user, calls the respective methods, and displays the output.


## ALGORITHM :
1. Start the program.
2. Create a class named Calculator.
3. Define a non-static method add(int a, int b) that returns the sum of two integers.
4. Define a static method info() that prints "Calculator is ready".
5. In the main class (prog), create a Scanner object to read two integers.
6. Call the static method info() using the class name Calculator.
7. Create an object of Calculator to access the non-static add() method.
8. Call the add() method with the user inputs and store the returned value.
9. Display the result.
10. Close the Scanner.
11. End the program.



## PROGRAM:
 ```
/*
Program to implement a Access Modifiers using Java
Developed by: SUCHITRA NATH
RegisterNumber: 212223220112
*/
```

```
import java.util.Scanner;

class Calculator {
    public int add(int a, int b) {
        return a + b;
    }

    public static void info() {
        System.out.println("Calculator is ready");
    }
}

class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int a = sc.nextInt();
        int b = sc.nextInt();

        Calculator.info();  // call static method

        Calculator calc = new Calculator();  // create object for non-static method
        int result = calc.add(a, b);

        System.out.println("Sum: " + result);

        sc.close();
    }
}

```








## OUTPUT:
<img width="930" height="414" alt="image" src="https://github.com/user-attachments/assets/78ada3c5-58ae-4f20-a8e5-69d866a8ccb1" />




## RESULT:
Thus, the Java program to demonstrate static and non-static methods using the Calculator class has been executed successfully.

