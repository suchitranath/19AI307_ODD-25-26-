# Ex.No:3(A) INHERITANCE AND AGGREGATION

## QUESTION:
Create a superclass Person with fields name and age.
Create a subclass Student that inherits from Person and adds a field marks (integer).

Implement a method calculateGrade() inside Student that returns the grade based on marks:

Marks ≥ 90 → Grade A

Marks ≥ 75 and < 90 → Grade B

Marks ≥ 50 and < 75 → Grade C

Marks < 50 → Grade F

Write a Java program to read the student details and display Name, Age, Marks, and Grade.


## AIM:
To write a Java program using single inheritance, where the subclass Student extends the superclass Person, and calculates the student’s grade based on marks using conditional statements.

## ALGORITHM :
1. Start the program and read the user's input: name, age, and marks.
2. Create a Student object using the given name, age, and marks.
3. Inside the Student class, compare the marks using conditions to determine the grade (A, B, C, or F).
4. Call the calculateGrade() method to get the student’s grade.
5. Display the student's name, age, marks, and calculated grade.




## PROGRAM:
 ```
/*
Program to implement a Inheritance and Aggregation using Java
Developed by: SUCHITRA NATH
RegisterNumber: 212223220112
*/
```

```
import java.util.Scanner;

// Superclass Person
class Person {
    String name;
    int age;

    Person(String name, int age) {
        this.name = name;
        this.age = age;
    }
}

// Subclass Student
class Student extends Person {
    int marks;

    Student(String name, int age, int marks) {
        super(name, age);
        this.marks = marks;
    }

    String calculateGrade() {
        if (marks >= 90) {
            return "A";
        } else if (marks >= 75) {
            return "B";
        } else if (marks >= 50) {
            return "C";
        } else {
            return "F";
        }
    }
}

// Main class
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String name = sc.nextLine();
        int age = sc.nextInt();
        int marks = sc.nextInt();

        Student s = new Student(name, age, marks);

        System.out.println("Name: " + s.name);
        System.out.println("Age: " + s.age);
        System.out.println("Marks: " + s.marks);
        System.out.println("Grade: " + s.calculateGrade());
    }
}

```


## OUTPUT:
<img width="764" height="674" alt="image" src="https://github.com/user-attachments/assets/c1a44f8b-2c23-4a50-8c06-57c1f21dc3fd" />



## RESULT:
Thus, the Java program to calculate the student's grade using inheritance is executed successfully.

