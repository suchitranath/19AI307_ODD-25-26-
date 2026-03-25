# Ex.No:5(B) SERIALIZATION AND DESERIALIZATION 

## QUESTION:
Write a Java program to serialize a collection of objects (ArrayList<Student>) into a file.
The program should take student details as input, serialize them into "students.dat",then deserialize the file and display the student objects.

## AIM:
To understand object serialization and deserialization in Java by storing and retrievinga list of Student objects using ObjectOutputStream and ObjectInputStream.


## ALGORITHM :
1. Start the program.
2. Create a Student class implementing Serializable.
3. Create methods to serialize and deserialize a List<Student>.
4. Read the number of students from the user.
5. For each student, read id, name, and marks, then add the Student object to ArrayList.
6. Serialize the ArrayList<Student> into a file named "students.dat".
7. Deserialize the file to retrieve the list of students.
8. Print the deserialized student details.
9. Handle IO and ClassNotFound exceptions.
10. End the program.




## PROGRAM:
 ```
/*
Program to implement a Serialization and Deserialization using Java
Developed by: SUCHITRA NATH
RegisterNumber: 212223220112
*/
```
```
import java.io.*;
import java.util.*;

// Student class must implement Serializable
class Student implements Serializable {
    private static final long serialVersionUID = 1L;

    private int id;
    private String name;
    private double marks;

    public Student(int id, String name, double marks) {
        this.id = id;
        this.name = name;
        this.marks = marks;
    }

    @Override
    public String toString() {
        return "Student{id=" + id + ", name='" + name + "', marks=" + marks + "}";
    }
}

public class StudentSerializationUserInput {

    // Serialize list of students
    public static void serializeStudents(List<Student> students, String fileName) {
        try (ObjectOutputStream oos = new ObjectOutputStream(new FileOutputStream(fileName))) {
            oos.writeObject(students);
            System.out.println("Students serialized successfully into: " + fileName);
        } catch (IOException e) {
            System.out.println("Error during serialization: " + e.getMessage());
        }
    }

    // Deserialize list of students
    @SuppressWarnings("unchecked")
    public static List<Student> deserializeStudents(String fileName) {
        List<Student> students = null;
        try (ObjectInputStream ois = new ObjectInputStream(new FileInputStream(fileName))) {
            students = (List<Student>) ois.readObject();
            System.out.println("Students deserialized successfully from: " + fileName);
        } catch (IOException | ClassNotFoundException e) {
            System.out.println("Error during deserialization: " + e.getMessage());
        }
        return students;
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        List<Student> students = new ArrayList<>();

        int n = scanner.nextInt();
        scanner.nextLine(); // consume newline

        
        
for (int i = 0; i < n; i++) {
            int id = scanner.nextInt();
            String name = scanner.next();
            double marks = scanner.nextDouble();
            students.add(new Student(id, name, marks));
        }

        serializeStudents(students, "students.dat");
        List<Student> deserializedStudents = deserializeStudents("students.dat");
        // Display deserialized data
        if (deserializedStudents != null) {
            System.out.println("\nDeserialized Students:");
            for (Student s : deserializedStudents) {
                System.out.println(s);
            }
        }

        scanner.close();
    }
}

```







## OUTPUT:
<img width="1250" height="536" alt="image" src="https://github.com/user-attachments/assets/9454f3f9-d8ac-47dc-be5f-7a5b8f6b921c" />



## RESULT:
The student objects are successfully serialized into students.dat
and later deserialized from the file. The deserialized details are displayed correctly.
Thus, serialization and deserialization of a collection of objects is implemented successfully.
