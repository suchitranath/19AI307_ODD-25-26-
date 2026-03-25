# Ex.No:5(E) MULTITHREADING -SYNCHRONIZATION

## QUESTION:
QUESTION :
Create a Java program that reads a thread name and a priority (1–10), assigns both toa newly created thread, and then prints the thread name along with its priority.



## AIM:
To understand how to set a thread's name and priority in Java and retrieve those values.

## ALGORITHM :
1. Start the program and create a Scanner object for reading input.
2. Read the thread name as a string from the user.
3. Read the thread priority (1–10) as an integer.
4. Create a new Thread object with a simple lambda runnable.
5. Set the name and priority of the thread using setName() and setPriority().
6. Print the thread name and priority using getName() and getPriority().
7. End the program.




## PROGRAM:
 ```
/*
Program to implement a Synchronization concept using Java
Developed by: SUCHITRA NATH
RegisterNumber: 212223220112
*/
```

```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        String threadName = sc.nextLine();
        int priority = sc.nextInt();

        Thread t = new Thread(() -> {
            // thread work (empty for this task)
        });

        t.setName(threadName);
        t.setPriority(priority);

        System.out.println("Thread " + t.getName() + " priority is " + t.getPriority());
    }
}

```







## OUTPUT:

<img width="959" height="413" alt="image" src="https://github.com/user-attachments/assets/ff8a911f-bf26-43b2-a0a8-39d0a7a8d585" />



## RESULT:
The program successfully reads the thread name and priority,sets them to a new thread, and prints:
Thread <name> priority is <priority>
Thus, thread property assignment is demonstrated successfully.
