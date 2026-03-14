# Ex.No:2(B) METHODS

## QUESTION:
Write a class with one static method and one non-static method. 
Call both from the main() method.

When staticMethod() is called, it should print "I am static".
When nonStaticMethod() is called, it should print "I am non-static".

Example Output:
I am static
I am non-static



## AIM:
To write a Java program that demonstrates the use of static and non-static methods inside a class and to call both methods from the main() function.



## ALGORITHM :
1. Start the program.
2. Import the necessary package 'java.util' (if needed).
3. Create a class named 'prog'.
4. Inside the class, define a static method staticMethod() that prints "I am static".
5. Define a non-static method nonStaticMethod() that prints "I am non-static".
6. In the main() method:
     a. Call the static method using the class name.
     b. Create an object for the class.
     c. Call the non-static method using the object.
7. End the program.





## PROGRAM:
 ```
/*
Program to implement a Methods using Java
Developed by: SUCHITRA NATH
RegisterNumber: 212223220112
*/
```
```
public class prog{
    static void staticMethod(){
        System.out.println("I am static");
    }

    void nonStatic(){
        System.out.println("I am non-static");
    }
    
    public static void main(String[] args){
        prog.staticMethod();
        prog obj = new prog();
        obj.nonStatic();
    }
}

```

## OUTPUT:
<img width="809" height="278" alt="image" src="https://github.com/user-attachments/assets/67b76152-9476-4bda-aa9e-788e9f8325cd" />



## RESULT:
Thus, the Java program to demonstrate static and non-static methods was executed successfully.

