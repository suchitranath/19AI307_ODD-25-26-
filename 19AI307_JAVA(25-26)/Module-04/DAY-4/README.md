# Ex.No:4(D) DESIGN PATTERN -- ABSTRACT FACTORY

## QUESTION:
You are creating a cross-platform UI tool using the Abstract Factory design pattern.
Implement factories to create UI components (Button and Checkbox) for two themes:
"dark" and "light".

The user selects a theme, after which the corresponding factory should generate
a Button and a Checkbox and display their creation messages.

dark theme:
Dark Button created
Dark Checkbox created

light theme:
Light Button created
Light Checkbox created


## AIM:
To implement the Abstract Factory design pattern in Java that creates related UI components (Button and Checkbox) for multiple themes (Dark and Light) without 
specifying their concrete classes directly in the main code.


## ALGORITHM :
1. Define abstract product interfaces (Button, Checkbox) containing a render() method.
2. Create concrete product classes for both themes: DarkButton, DarkCheckbox,
   LightButton, LightCheckbox.
3. Define an abstract factory interface (UIFactory) with methods to create a 
   Button and a Checkbox.
4. Implement two concrete factories: DarkThemeFactory and LightThemeFactory, 
   each returning theme-specific components.
5. In the main method, read the theme from the user, instantiate the correct 
   factory, create the UI components, and render them.
	





## PROGRAM:
 ```
/*
Program to implement a Abstract Factory Pattern using Java
Developed by: SUCHITRA NATH
RegisterNumber: 212223220112
*/
```

```
import java.util.Scanner;

// Product interfaces
interface Button {
    void render();
}

interface Checkbox {
    void render();
}

// Concrete Products for Dark Theme
class DarkButton implements Button {
    public void render() {
        System.out.println("Dark Button created");
    }
}

class DarkCheckbox implements Checkbox {
    public void render() {
        System.out.println("Dark Checkbox created");
    }
}

// Concrete Products for Light Theme
class LightButton implements Button {
    public void render() {
        System.out.println("Light Button created");
    }
}

class LightCheckbox implements Checkbox {
    public void render() {
        System.out.println("Light Checkbox created");
    }
}

// Abstract Factory
interface UIFactory {
    Button createButton();
    Checkbox createCheckbox();
}

// Concrete Factories
class DarkThemeFactory implements UIFactory {
    public Button createButton() {
        return new DarkButton();
    }
    public Checkbox createCheckbox() {
        return new DarkCheckbox();
    }
}

class LightThemeFactory implements UIFactory {
    public Button createButton() {
        return new LightButton();
    }
    public Checkbox createCheckbox() {
        return new LightCheckbox();
    }
}

// Main class
public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String theme = scanner.nextLine().toLowerCase();

        UIFactory factory;
        if (theme.equals("dark")) {
            factory = new DarkThemeFactory();
        } else if (theme.equals("light")) {
            factory = new LightThemeFactory();
        } else {
            System.out.println("Invalid theme");
            return;
        }

        factory.createButton().render();
        factory.createCheckbox().render();
    }
}

```






## OUTPUT:
<img width="741" height="390" alt="image" src="https://github.com/user-attachments/assets/d5ab6014-bbac-4299-875b-fff96a2633cd" />



## RESULT:
The program successfully demonstrates the Abstract Factory design pattern.
Based on the user-selected theme, the correct factory is created and generates the appropriate Button and Checkbox components.

Thus, the Java program using the Abstract Factory Pattern for UI theme selection is executed successfully.

