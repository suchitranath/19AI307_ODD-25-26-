# Ex.No:5(D) THREAD PRIORITY

## QUESTION:
Write a Java program to implement multithreading by extending the Thread class.
The thread should print numbers from 1 to 5, while the main thread prints a completion message.

## AIM:
To understand how to create and start a thread in Java using the Thread class
and implement concurrent execution.

## ALGORITHM :
1. Create a class MyThread that extends the Thread class.
2. Override the run() method to print numbers from 1 to 5.
3. Inside the loop, add Thread.sleep() to slow down execution for clarity.
4. In the main() method, create an object of MyThread.
5. Start the thread using start().
6. Print a message from the main thread to show concurrent execution.
7. End the program.





## PROGRAM:
 ```
/*
Program to implement a Thread Priority Concept using Java
Developed by: SUCHITRA NATH
RegisterNumber: 212223220112
*/
```

```
class MyThread extends Thread {

    public void run() {
        // Print numbers 1 to 5
        for (int i = 1; i <= 5; i++) {
            System.out.println("Thread: " + i);
            try {
                Thread.sleep(100); // Small delay for clean output
            } catch (InterruptedException e) {
                System.out.println(e);
            }
        }

        
    }
}

public class Main {

    public static void main(String[] args) {

        MyThread t = new MyThread();

        // Start the thread
        t.start();

        // Main thread message printed instantly
        System.out.println("Main thread finished");
    }
}

```






## OUTPUT:


<img width="702" height="382" alt="image" src="https://github.com/user-attachments/assets/32babf3e-a3c6-402c-9db3-29a5eb57e2cb" />



## RESULT:
The custom thread prints the numbers 1 to 5 with a delay,while the main thread immediately prints "Main thread finished".
This demonstrates successful multithreading using the Thread class.
