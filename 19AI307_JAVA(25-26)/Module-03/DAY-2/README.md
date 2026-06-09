# Ex.No:3(b) POLYMORPHISM

## AIM:

To write a Java program that demonstrates method overriding using a base class Shape and subclasses Circle and Cylinder to calculate their respective areas.

## ALGORITHM :

1.Start the program.

2.Create a base class Shape with methods draw() and calculateArea().

3.Create subclasses Circle and Cylinder that override these methods.

4.Read the user's choice and the required dimensions, then create the appropriate object.

5.Call the overridden methods to display the shape and calculate its area, then stop the program.

## PROGRAM:
 ```
/*
Program to implement a Polymorphism using Java
Developed by: KIRTHICK ROSHAN J
RegisterNumber:  212223040097
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

class Shape {

    void draw() {
        System.out.println("Drawing Shape");
    }

    double calculateArea() {
        return 0;
    }
}

class Circle extends Shape {
    double radius;

    Circle(double radius) {
        this.radius = radius;
    }

    @Override
    void draw() {
        System.out.println("Drawing a circle...");
    }

    @Override
    double calculateArea() {
        return 3.14159 * radius * radius;
    }
}

class Cylinder extends Shape {
    double radius, height;

    Cylinder(double radius, double height) {
        this.radius = radius;
        this.height = height;
    }

    @Override
    void draw() {
        System.out.println("Drawing a cylinder...");
    }

    @Override
    double calculateArea() {
        return 2 * 3.14159 * radius * (radius + height);
    }
}

public class prog {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        String choice = sc.next();

        if (choice.equalsIgnoreCase("circle")) {

            double radius = sc.nextDouble();

            Circle c = new Circle(radius);

            c.draw();
            System.out.printf("Area: %.2f", c.calculateArea());

        }
        else if (choice.equalsIgnoreCase("cylinder")) {

            double radius = sc.nextDouble();
            double height = sc.nextDouble();

            Cylinder cy = new Cylinder(radius, height);

            cy.draw();
            System.out.printf("Area: %.2f", cy.calculateArea());
        }
        else {

            System.out.println("Invalid shape type.");
        }

        sc.close();
    }
}
```

## OUTPUT:
<img width="610" height="298" alt="image" src="https://github.com/user-attachments/assets/74b73189-7416-4332-aef5-a338dc33e835" />



## RESULT:
Thus, the program successfully demonstrates method overriding by calculating and displaying the area of a circle or the total surface area of a cylinder based on the user's choice.
