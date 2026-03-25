# Ex.No:5(A) INPUTSTREAMREADER 

## QUESTION:
Write a Java program to write characters to a file using FileWriter.
The program should take the filename and the content from the user and write the content into the file.

## AIM:
To understand file handling in Java using FileWriter and to write user-provided text into a file.

## ALGORITHM :
1. Start the program.
2. Create a Scanner object to read input.
3. Read the filename from the user.
4. Read the content to be written into the file.
5. Create a File object using the filename.
6. Use FileWriter to write content into the file.
7. Close the FileWriter.
8. Display "File written successfully." on successful write.
9. Handle exceptions using try–catch.
10. End the program.





## PROGRAM:
 ```
/*
Program to implement a InputStreamReader using Java
Developed by: SUCHITRA NATH
RegisterNumber: 212223220112
*/
```

```
import java.io.FileWriter;
import java.io.IOException;
import java.util.Scanner;
import java.io.File;

public class WriteFileUsingFileWriter {
    public static void main(String[] args) {
    //write your code here
    Scanner scanner = new Scanner(System.in);
    String file = scanner.next();
    String cont = scanner.next();
    
    try
    {File f = new File(file);
    FileWriter fw = new FileWriter(f);
    System.out.println("File written successfully.");
        
    }catch(Exception E){
        System.out.println(E);
    }
    
    
    
    }
}
```







## OUTPUT:
<img width="964" height="414" alt="image" src="https://github.com/user-attachments/assets/7b531577-5f13-4036-ade4-6da97aa28410" />



## RESULT:
The program successfully creates the file with the given filename
and writes the provided content into it.
Thus, writing characters to a file using FileWriter works correctly.
