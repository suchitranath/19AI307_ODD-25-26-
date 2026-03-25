# Ex.No:4(B)  IMPLEMENT SOLID PRINCIPLES IN JAVA PROGRAM 

## QUESTION:
In a gaming lounge, there is only one master console power switch that controls
all gaming consoles. Whenever a player turns on any console, it internally triggers
the master power. The master switch must ensure only one instance is ever created
to prevent power fluctuations, hence it must follow the Singleton pattern.

Every time a player accesses the master switch, it must increment a global access count.
Since the switch is Singleton, the count should be shared across all players.

Input Format:
n
[Player1]
[Player2]
...

Output each line as:
[PlayerName] accessed Master Power Switch. Total accesses so far: [count]


## AIM:
To implement the Singleton design pattern in Java to ensure only one instance ofthe master power switch exists, and to maintain a shared access counter that
increments each time any player accesses the switch.


## ALGORITHM :
1. Define a Singleton class MasterSwitch with a private instance and a private 
   constructor to restrict object creation.

2. Provide a public static getInstance() method that returns the single instance 
   of MasterSwitch (creates it only once).

3. Inside the Singleton class, maintain a global access counter and increment it
   each time a player accesses the switch through an access() method.

4. In the main program, read the number of players and their names, and obtain 
   the same Singleton instance for each access.

5. For every player, call the access() method and print the player name along 
   with the updated count.



## PROGRAM:
 ```
/*
Program to implement a SOLID Principles in Java Program
Developed by: SUCHITRA NATH
RegisterNumber: 212223220112
*/
```

```
import java.util.*;

class MasterPowerSwitch {
    private static MasterPowerSwitch instance = null;
    private int accessCount = 0;

    // Private constructor prevents new instance creation
    private MasterPowerSwitch() {}

    // Static method to get the only instance (Singleton)
    public static MasterPowerSwitch getInstance() {
        if (instance == null) {
            instance = new MasterPowerSwitch();
        }
        return instance;
    }

    // Method to increment and return global access count
    public int logAccess() {
        accessCount++;
        return accessCount;
    }
}

public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        sc.nextLine();

        for (int i = 0; i < n; i++) {
            String player = sc.nextLine();
            MasterPowerSwitch power = MasterPowerSwitch.getInstance();
            int count = power.logAccess();
            System.out.println(player + " accessed Master Power Switch. Total accesses so far: " + count);
        }
    }
}

```








## OUTPUT:
<img width="1248" height="400" alt="image" src="https://github.com/user-attachments/assets/7f9bbd56-84d8-4fd6-b519-56a5513c752d" />




## RESULT:
The program successfully demonstrates the Singleton design pattern.
Only one MasterSwitch object is created, and every player access increases the
shared global counter. The output displays the player names along with the
updated number of total accesses.

Thus, the Java program using Singleton with a global access counter is executed successfully.

