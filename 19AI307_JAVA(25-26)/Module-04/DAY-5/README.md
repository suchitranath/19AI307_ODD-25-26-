# Ex.No:4(D) DESIGN PATTERN  ---- BEHAVIOUR PATTERN

## QUESTION:
Design a program where a Product model stores item info, and the view displays it. Implement a controller to update product price and refresh the view automatically.

## AIM:
To develop a Java application that implements the MVC design pattern, enabling separation of concerns between data (Model), user interface (View), and update logic (Controller) by updating product price dynamically and reflecting the changes through the view.

## ALGORITHM :
1. Start the program.
2. Read the product name, price, and code from the user.
3. Read the new price to be updated.
4. Create a Product object with the given details.
5. Create a ProductView object to display product information.
6. Create a ProductController object by passing Model and View.
7. Call updateView() to display initial product details.
8. Call updatePrice() to modify the product price.
9. The controller refreshes the view automatically and displays updated price.
10. End the program.





## PROGRAM:
 ```
/*
Program to implement a Behaviour Pattern using Java
Developed by: SUCHITRA NATH
RegisterNumber: 212223220112
*/
```

```
import java.util.Scanner;

public class ProductManagementSystem {

    // ===== Model =====
    static class Product {
        private String name;
        private double price;
        private String code;

        public Product(String name, double price, String code) {
            this.name = name;
            this.price = price;
            this.code = code;
        }

        public String getName() {
            return name;
        }

        public double getPrice() {
            return price;
        }

        public String getCode() {
            return code;
        }

        public void setPrice(double price) {
            this.price = price;
        }
    }

    // ===== View =====
    static class ProductView {
        public void displayProduct(String name, double price, String code) {
            System.out.println("--- Product Details ---");
            System.out.println("Name : " + name);
            System.out.println("Price: " + price);
            System.out.println("Code : " + code);
        }
    }

    // ===== Controller =====
    static class ProductController {
        private Product product;
        private ProductView view;

        public ProductController(Product product, ProductView view) {
            this.product = product;
            this.view = view;
        }

        public void updateView() {
            view.displayProduct(product.getName(), product.getPrice(), product.getCode());
        }

        public void updatePrice(double newPrice) {
            product.setPrice(newPrice);
            updateView();
        }
    }

    // ===== Main Method =====
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String name = sc.nextLine();
        double price = sc.nextDouble();
        sc.nextLine(); // consume newline
        String code = sc.nextLine();
        double newPrice = sc.nextDouble();

        Product product = new Product(name, price, code);
        ProductView view = new ProductView();
        ProductController controller = new ProductController(product, view);

        controller.updateView();         // display initial details
        controller.updatePrice(newPrice); // update price and refresh view

        sc.close();
    }
}

```







## OUTPUT:
<img width="860" height="427" alt="image" src="https://github.com/user-attachments/assets/535b84cd-a777-44c2-89d8-3c4f578e7010" />



## RESULT:
The program successfully displays the initial product details and updates the price.
After updating, the controller refreshes the view and prints the new price.
Thus, the MVC-based product management system executes correctly.

