# Ex.No:4(D) DESIGN PATTERN -- ABSTRACT FACTORY

## QUESTION:
You’re creating a cross-platform UI tool using the Abstract Factory pattern. Implement factories to create Button and Checkbox for "dark" and "light" themes. Let the user choose the theme, then generate UI components and display their types


## **Aim**

To implement the Abstract Factory design pattern for a cross-platform UI tool that creates Button and Checkbox components for "dark" and "light" themes, allowing the user to choose a theme and then generating and displaying the types of UI components created.



## **Algorithm**

1. Start the program.
2. Define abstract product interfaces for **Button** and **Checkbox**.
3. Create concrete product classes for both themes:

   * DarkButton and DarkCheckbox
   * LightButton and LightCheckbox
4. Define an **Abstract Factory** interface with methods to create a Button and a Checkbox.
5. Implement concrete factories:

   * **DarkThemeFactory** for dark UI components
   * **LightThemeFactory** for light UI components
6. Ask the user to choose a theme ("dark" or "light").
7. Based on the user’s choice, create the corresponding factory object.
8. Use the selected factory to create a Button and a Checkbox.
9. Display the type/theme of each created UI component.
10. End the program.





## PROGRAM:
 ```
/*
Program to implement a Abstract Factory Pattern using Java
Developed by: 
RegisterNumber:  
*/
```

## SOURCE CODE:

```
import java.util.Scanner;

interface Button {
    void assemble();
}
interface Checkbox {
    void assemble();
}

class Darkbutton implements Button {
    public void assemble() { System.out.println("Dark Button created"); }
}
class Lightbutton implements Button {
    public void assemble() { System.out.println("Light Button created"); }
}
class DarkcheckBox implements Checkbox {
    public void assemble() { System.out.println("Dark Checkbox created"); }
}
class LightcheckBox implements Checkbox {
    public void assemble() { System.out.println("Light Checkbox created"); }
}

interface VehicleFactory {
    Button createButton();
    Checkbox createCheckBox();
}

class DarkFactory implements VehicleFactory {
    public Button createButton() { return new Darkbutton(); }
    public Checkbox createCheckBox() { return new DarkcheckBox(); }
}

class LightFactory implements VehicleFactory {
    public Button createButton() { return new Lightbutton(); }
    public Checkbox createCheckBox() { return new LightcheckBox(); }
}

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String brand = scanner.nextLine().toLowerCase();

        VehicleFactory factory;
        if (brand.equals("dark")) factory = new DarkFactory();
        else if (brand.equals("light")) factory = new LightFactory();
        else {
            System.out.println("Invalid theme");
            return;
        }

        factory.createButton().assemble();
        factory.createCheckBox().assemble();
    }
}
```





## OUTPUT:

<img width="704" height="286" alt="image" src="https://github.com/user-attachments/assets/eca3bee2-2dd6-4a2a-b0cc-277f4d7bce78" />


## RESULT:

Thus java program executed successfully
