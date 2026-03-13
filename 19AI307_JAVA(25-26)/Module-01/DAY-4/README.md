# Ex.No:1(D) ARRAYS

## QUESTION:
```
Write a Java Program to Find the Average of Array Elements.

Example:
Input:
5
10
20
30
40
50

Output:
The average of elements is 30.00

```


## AIM:
To write a Java program that reads 'n' array elements, calculates their sum, and computes the average of the elements using loops.



## ALGORITHM :
1. Start the program.
2. Create a Scanner object to read input from the user.
3. Read the size of the array.
4. Create an integer array of the given size.
5. Use a for loop to input array elements from the user.
6. Initialize a variable 'sum' to 0.
7. Use another for loop to add all array elements to 'sum'.
8. Calculate the average by dividing sum by the size.
9. Print the average value using formatted output.
10. Close the scanner.
11. End the program.





## PROGRAM:
 ```
/*
Program to implement a Array concept using Java
Developed by: SUCHITRA NATH
RegisterNumber: 212223220112
*/
```
```
import java.util.Scanner;
public class Main{
    public static void main(String[] args){
        Scanner scanner = new Scanner(System.in);
        
        int size = scanner.nextInt();
        float sum = 0;
        
        int[] elements = new int[size];
        
        for(int i = 0; i < elements.length; i++){
            elements[i] = scanner.nextInt();
        }
        
        for(int j = 0; j < elements.length; j++){
            sum += elements[j];
        }
        
        System.out.printf("The average of elements is %.2f", sum / size);
        
        scanner.close();
    }
}

```

## OUTPUT:

<img width="832" height="573" alt="image" src="https://github.com/user-attachments/assets/e7a8c28b-09d3-4a87-9e8a-d3e0b6fb57cd" />


## RESULT:
Thus, the Java program to calculate the average of array elements was executed successfully.



