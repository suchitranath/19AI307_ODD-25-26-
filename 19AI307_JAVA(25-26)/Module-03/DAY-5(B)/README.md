# Ex.No:3(F) WRAPPER CLASS

## QUESTION:
Write a Java program to check whether a given number is an Armstrong number.  Use Math.pow() for power calculation and use the Integer wrapper class to convert the number to a string to count digits.  Take the number as input from the user.



## AIM:
To write a Java program that determines whether a number is an Armstrong number using Math.pow() for exponent calculation and Integer wrapper class for digit count.



## ALGORITHM :
1. Start the program and read the input number from the user.
2. Convert the number to a string using Integer.toString() to determine the number of digits.
3. Extract each digit of the number using modulo and division operations.
4. Use Math.pow(digit, number_of_digits) to compute powered sum of each digit.
5. Compare the computed sum with the original number and print whether it is
   an Armstrong number or not.



## PROGRAM:
 ```
/*
Program to implement a Wrapper Class using Java
Developed by: SUCHITRA NATH
RegisterNumber: 212223220112
*/
```
```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        // Take input
        int num = sc.nextInt();
        int original = num;

        // Convert to String using Integer wrapper class to find length
        int digits = Integer.toString(num).length();

        int sum = 0;
        while (num > 0) {
            int digit = num % 10;
            sum += Math.pow(digit, digits); // use Math.pow()
            num /= 10;
        }

        if (sum == original)
            System.out.println(original + " is an Armstrong number.");
        else
            System.out.println(original + " is not an Armstrong number.");
    }
}

```






## OUTPUT:
<img width="806" height="345" alt="image" src="https://github.com/user-attachments/assets/db5bb914-dd89-4295-b4ba-a10d2bfdb191" />



## RESULT:
The program successfully takes a number as input and calculates the sum of its digits 
raised to the power of the total number of digits. If this sum matches the original 
number, it prints that the number is an Armstrong number.

Thus, the Java program to check for Armstrong number using Math.pow() and 
Integer wrapper class is executed successfully.


