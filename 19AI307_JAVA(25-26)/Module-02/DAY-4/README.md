# Ex.No:2(D) VARIABLE SCOPE AND CONSTRUCTOR

## QUESTION:
Write a program to access a static variable using both class name 
and object.

Example:
Input:
48

Output:
Accessing using class name: 48
Accessing using object: 48


## AIM:
To write a Java program that demonstrates how to access a static method (or static variable) using both the class name and an object of the class.



## ALGORITHM :
1. Start the program.
2. Create a class named 'prog'.
3. Inside the class, define a static method display(int n) that returns n.
4. In the main() method:
       a. Create a Scanner object to read input.
       b. Read an integer from the user.
       c. Call the static method using the class name.
       d. Create an object of the class.
       e. Call the same static method using the object.
5. Print outputs accordingly.
6. Close the scanner.
7. End the program.





## PROGRAM:
 ```
/*
Program to implement a Variable scope and Constructor using Java
Developed by: SUCHITRA NATH
RegisterNumber: 212223220112
*/
```
```
import java.util.Scanner;

class prog {
    static int display(int n) {
        return n;
    }
    
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        int num = scanner.nextInt();
        
        System.out.println("Accessing using class name: " + prog.display(num));
        
        prog obj = new prog();
        System.out.println("Accessing using object: " + obj.display(num));
        
        scanner.close();
    }
}

```

## OUTPUT:
<img width="885" height="422" alt="image" src="https://github.com/user-attachments/assets/998efae8-7709-4bb9-9835-1780c898457d" />

## RESULT:
Thus, the Java program to access a static method using both class name and object was executed successfully.



