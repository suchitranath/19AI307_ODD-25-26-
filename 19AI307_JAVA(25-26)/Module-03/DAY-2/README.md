# Ex.No:3(b) POLYMORPHISM

## QUESTION:
Write a Java program that calculates the area of different shapes using method overloading.
Create a class AreaCalculator with the following overloaded methods:

1. area(int side) → calculates area of a square  
2. area(int length, int breadth) → calculates area of a rectangle  
3. area(double radius) → calculates area of a circle  

Read inputs for side, length & breadth, and radius, then display the areas accordingly.




## AIM:
To write a Java program that demonstrates method overloading by calculatingthe area of a square, rectangle, and circle using different versions of the area() method.




## ALGORITHM :
1. Start the program and read inputs for square side, rectangle dimensions,
   and circle radius.
2. Create an object of the AreaCalculator class.
3. Invoke area(side) to compute the area of the square.
4. Invoke area(length, breadth) to compute the area of the rectangle.
5. Invoke area(radius) to compute the area of the circle and display all results.





## PROGRAM:
 ```
/*
Program to implement a Polymorphism using Java
Developed by: SUCHITRA NATH
RegisterNumber: 212223220112
*/
```
```
import java.util.Scanner;

class AreaCalculator {
    public int area(int side) {
        return side * side;
    }

    public int area(int length, int breadth) {
        return length * breadth;
    }

    public double area(double radius) {
        return Math.PI * radius * radius;
    }
}

public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        AreaCalculator ac = new AreaCalculator();

        int side = sc.nextInt();
        System.out.println("Area of square: " + ac.area(side));

        int length = sc.nextInt();
        int breadth = sc.nextInt();
        System.out.println("Area of rectangle: " + ac.area(length, breadth));

        double radius = sc.nextDouble();
        System.out.println("Area of circle: " + ac.area(radius));

        sc.close();
    }
}

```

## OUTPUT:

<img width="971" height="489" alt="image" src="https://github.com/user-attachments/assets/f969dc5a-6384-4de2-b6fd-c7edfe4ba4d8" />


## RESULT:
Thus, the Java program using method overloading to calculate areas is executed successfully.

