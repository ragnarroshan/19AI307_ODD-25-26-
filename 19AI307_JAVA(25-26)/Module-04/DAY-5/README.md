# Ex.No:4(D) DESIGN PATTERN  ---- BEHAVIOUR PATTERN

## AIM:
To write a Java program that implements the Mediator Design Pattern for an Air Traffic Control System, where airplanes request landing through a central control tower.

## ALGORITHM :

1.Start the program.

2.Create a mediator (Air Traffic Control) to manage landing requests.

3.Create airplane objects and register them with the mediator.

4.When an airplane requests landing, the mediator checks runway availability.

5.Grant or deny landing accordingly and display the result.



## PROGRAM:
 ```
/*
Program to implement a Behaviour Pattern using Java
Developed by: KIRTHICK ROSHAN J
RegisterNumber:  212223040097
*/
```

## SOURCE CODE:

```
import java.util.*;

class AirTrafficControl {
    private boolean autoRelease;
    private boolean firstLandingDone = false;
    private boolean runwayBusy = false;

    public AirTrafficControl(boolean autoRelease) {
        this.autoRelease = autoRelease;
    }

    public void requestLanding(Airplane airplane) {

        
        if (!firstLandingDone) {
            firstLandingDone = true;

            System.out.println(airplane.getName() + " granted landing.");
            System.out.println(airplane.getName() + " landed successfully.");

            if (!autoRelease) {
                runwayBusy = true;
            }
            return;
        }

        
        if (autoRelease) {
            System.out.println(airplane.getName() + " granted landing.");
            System.out.println(airplane.getName() + " landed successfully.");
        } else {
            
            if (runwayBusy) {
                System.out.println(airplane.getName()
                        + " denied landing. Runway busy.");
            }
        }
    }
}

class Airplane {
    private String name;
    private AirTrafficControl atc;

    public Airplane(String name, AirTrafficControl atc) {
        this.name = name;
        this.atc = atc;
    }

    public String getName() {
        return name;
    }

    public void requestLanding() {
        atc.requestLanding(this);
    }
}

public class AirTrafficSystem {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();
        boolean runwayFree = sc.nextBoolean();
        sc.nextLine();

        AirTrafficControl atc = new AirTrafficControl(runwayFree);

        List<Airplane> airplanes = new ArrayList<>();

        for (int i = 0; i < n; i++) {
            String name = sc.nextLine();
            airplanes.add(new Airplane(name, atc));
        }

        for (Airplane airplane : airplanes) {
            airplane.requestLanding();
        }

        sc.close();
    }
}
```



## OUTPUT:


<img width="881" height="467" alt="image" src="https://github.com/user-attachments/assets/8a0b85cf-5155-4a23-b8de-1c1afac7fccd" />


## RESULT:
Thus, the program successfully implements the Mediator Behavioral Design Pattern, where the Air Traffic Control acts as a central mediator to coordinate landing requests from multiple airplanes.
