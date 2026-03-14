# Ex.No:2(C) ACCESS SPECIFIERS

## QUESTION:
```
Write a Java program to create a class called Smartphone with private instance variables brand, model, and storageCapacity. Provide public getter and setter methods to access and modify these variables. Add a method called increaseStorage() that takes an integer value and increases the storageCapacity by that value.

import java.util.Scanner;

class Smartphone {
    private String brand;
    private String model;
    private int storageCapacity;

    
    public String getBrand() {
        return brand;
    }

    public String getModel() {
        return model;
    }

    public int getStorageCapacity() {
        return storageCapacity;
    }

    
    public void setBrand(String brand) {
        this.brand = brand;
    }

    public void setModel(String model) {
        this.model = model;
    }

    public void setStorageCapacity(int storageCapacity) {
        this.storageCapacity = storageCapacity;
    }

   
    public void increaseStorage(int value) {
        if (value > 0) {
            this.storageCapacity += value;
        }
    }

    
    public void display() {
        System.out.println("Brand: " + brand);
        System.out.println("Model: " + model);
        System.out.println("Updated Storage Capacity: " + storageCapacity + " GB");
        System.out.println("------------------------------");
    }
}

//continue your code here
```


## AIM:
To write a Java program that demonstrates the concept of encapsulation  by using private instance variables and public getter and setter  methods. Additionally, to implement a method that increases the storage  capacity of a smartphone.



## ALGORITHM :
1. Start the program.
2. Create a class named Smartphone with private variables:
       brand, model, storageCapacity.
3. Provide public getter and setter methods for each variable.
4. Create a method increaseStorage(int value) to increase storageCapacity.
5. Create a method display() to print smartphone details.
6. In the main() method:
       a. Create an object of Smartphone.
       b. Read brand, model, storage capacity, and extra storage 
          from the user.
       c. Set the values using setter methods.
       d. Call increaseStorage() to update the storage.
       e. Call display() to show the updated details.
7. Close the scanner.
8. End the program.




## PROGRAM:
 ```
/*
Program to implement a Access Specifiers using Java
Developed by: SUCHITRA NATH
RegisterNumber: 212223220112
*/
```
```
import java.util.Scanner;

class Smartphone {
    private String brand;
    private String model;
    private int storageCapacity;

    public String getBrand() {
        return brand;
    }

    public String getModel() {
        return model;
    }

    public int getStorageCapacity() {
        return storageCapacity;
    }

    public void setBrand(String brand) {
        this.brand = brand;
    }

    public void setModel(String model) {
        this.model = model;
    }

    public void setStorageCapacity(int storageCapacity) {
        this.storageCapacity = storageCapacity;
    }

    public void increaseStorage(int value) {
        if (value > 0) {
            this.storageCapacity += value;
        }
    }

    public void display() {
        System.out.println("Brand: " + brand);
        System.out.println("Model: " + model);
        System.out.println("Updated Storage Capacity: " + storageCapacity + " GB");
        System.out.println("------------------------------");
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        Smartphone phone = new Smartphone();

        String brand = scanner.nextLine();
        phone.setBrand(brand);

        String model = scanner.nextLine();
        phone.setModel(model);

        int storage = scanner.nextInt();
        phone.setStorageCapacity(storage);

        int extraStorage = scanner.nextInt();
        phone.increaseStorage(extraStorage);

        phone.display();

        scanner.close();
    }
}

```
## OUTPUT:
<img width="1054" height="557" alt="image" src="https://github.com/user-attachments/assets/a4ed0220-6e9f-4ea9-b3b0-e27ffde43228" />

## RESULT:
Thus, the Java program implementing encapsulation using getter and setter methods, and increasing smartphone storage capacity, was executed successfully.



