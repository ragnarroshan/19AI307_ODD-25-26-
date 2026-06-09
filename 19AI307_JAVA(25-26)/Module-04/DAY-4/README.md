# Ex.No:4(D) DESIGN PATTERN -- ABSTRACT FACTORY

## AIM:
To write a Java program that implements the Abstract Factory Design Pattern to create families of animals from different regions (Africa and Asia) and display their interaction.

## ALGORITHM :

1.Start the program.

2.Create abstract interfaces/classes for Herbivore and Carnivore.

3.Create concrete animal classes for Africa (Wildebeest, Lion) and Asia (Elephant, Tiger).

4.Create abstract and concrete factory classes to generate the appropriate animal family based on the region.

5.Create the animals using the selected factory, display the interaction result, and stop the program.




## PROGRAM:
 ```
/*
Program to implement a Abstract Factory Pattern using Java
Developed by: KIRTHICK ROSHAN J
RegisterNumber:  212223040097
*/
```

## SOURCE CODE:

```
import java.util.Scanner;

interface Herbivore {}

interface Carnivore {
    void eat(Herbivore h);
}

class Wildebeest implements Herbivore {}

class Buffalo implements Herbivore {}

class Lion implements Carnivore {
    public void eat(Herbivore h) {
        System.out.println("Lion eats Wildebeest");
    }
}

class Tiger implements Carnivore {
    public void eat(Herbivore h) {
        System.out.println("Tiger eats Buffalo");
    }
}

interface AnimalFactory {
    Herbivore createHerbivore();
    Carnivore createCarnivore();
}

class AfricaFactory implements AnimalFactory {
    public Herbivore createHerbivore() {
        return new Wildebeest();
    }

    public Carnivore createCarnivore() {
        return new Lion();
    }
}

class AsiaFactory implements AnimalFactory {
    public Herbivore createHerbivore() {
        return new Buffalo();
    }

    public Carnivore createCarnivore() {
        return new Tiger();
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String region = sc.nextLine().toLowerCase();

        AnimalFactory factory;

        if (region.equals("africa")) {
            factory = new AfricaFactory();
        } else if (region.equals("asia")) {
            factory = new AsiaFactory();
        } else {
            System.out.println("Invalid region");
            return;
        }

        Carnivore carnivore = factory.createCarnivore();
        Herbivore herbivore = factory.createHerbivore();

        carnivore.eat(herbivore);
    }
}
```





## OUTPUT:

<img width="516" height="207" alt="image" src="https://github.com/user-attachments/assets/07553aab-37ee-45b5-b788-e5d96b352d8f" />



## RESULT:
Thus, the program successfully implements the Abstract Factory Design Pattern and displays the correct interaction between the carnivore and herbivore based on the selected region.
