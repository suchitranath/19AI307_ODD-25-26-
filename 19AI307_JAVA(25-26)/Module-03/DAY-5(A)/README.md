# Ex.No:3(E) INNER CLASS

## QUESTION:
Write a Java program to create an enum named Season with values 
WINTER, SPRING, SUMMER, and FALL.  
Read a season name from the user, convert it to uppercase, and use a switch statement to display a custom message based on the season.

WINTER → "It's cold outside. Stay warm!"  
SPRING → "Flowers are blooming. Enjoy the fresh air!"  
SUMMER → "It's sunny and hot. Time for the beach!"  
FALL   → "Leaves are falling. Autumn is beautiful!"


## AIM:
To implement an enum in Java and use a switch statement to display season-specific messages based on user input.


## ALGORITHM :
1. Start the program and define an enum Season with WINTER, SPRING, SUMMER, FALL.
2. Read a season name from the user and convert it to uppercase.
3. Convert the input string into an enum constant using Season.valueOf().
4. Use a switch(season) statement to print a custom message based on the enum value.
5. If the input does not match any enum value, display an "Invalid season" message.




## PROGRAM:
 ```
/*
Program to implement a InnerClass using Java
Developed by: SUCHITRA NATH
RegisterNumber: 212223220112
*/
```
```
import java.util.Scanner;

public class Main {

    // Enum declaration
    enum Season {
        WINTER, SPRING, SUMMER, FALL
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        // Take input and convert to uppercase to match enum names
        String input = sc.next().toUpperCase();

        try {
            Season season = Season.valueOf(input);

            // Switch statement for custom message
            switch (season) {
                case WINTER:
                    System.out.println("It's cold outside. Stay warm!");
                    break;
                case SPRING:
                    System.out.println("Flowers are blooming. Enjoy the fresh air!");
                    break;
                case SUMMER:
                    System.out.println("It's sunny and hot. Time for the beach!");
                    break;
                case FALL:
                    System.out.println("Leaves are falling. Autumn is beautiful!");
                    break;
            }
        } catch (IllegalArgumentException e) {
            System.out.println("Invalid season entered!");
        }
    }
}


```







## OUTPUT:
<img width="973" height="360" alt="image" src="https://github.com/user-attachments/assets/ac8b1422-44f1-4459-a262-e5a7ebff9163" />



## RESULT:
The program successfully reads a season name from the user, converts it to the corresponding enum constant, and displays the correct message using a switch statement.

Thus, the Java program using enums and switch-case to display season messages is executed successfully.


