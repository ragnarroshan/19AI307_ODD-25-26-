# Ex.No:3(C) ABSTRACTION

## AIM:
To write a Java program using an abstract class Advisor and its subclasses StrategicAdvisor and EmergencyAdvisor to determine the appropriate advisory level based on the given conditions.

## ALGORITHM :

1.Start the program.

2.Create an abstract class Advisor with an abstract method adviseLevel().

3.Create subclasses StrategicAdvisor and EmergencyAdvisor that override the adviseLevel() method according to the given rules.

4.Read the advisor type and the required input values, then create the corresponding object.

5.Call the adviseLevel() method, display the advisory level (Minimal, Balanced, or Critical), and stop the program.


## PROGRAM:
 ```
/*
Program to implement a Abstraction using Java
Developed by:  KIRTHICK ROSAHN J
RegisterNumber:  212223040097
*/
```

## SOURCE CODE:

```
import java.util.*;
abstract class Advisor {
    abstract String adviseLevel();
}
class StrategicAdvisor extends Advisor {
    int unrestLevel;

    StrategicAdvisor(int unrestLevel) {
        this.unrestLevel = unrestLevel;
    }

    @Override
    String adviseLevel() {
        if (unrestLevel < 3)
            return "Minimal";
        else if (unrestLevel <= 6)
            return "Balanced";
        else
            return "Critical";
    }
}
class EmergencyAdvisor extends Advisor {
    int dangerLevel;
    int disasterCount;

    EmergencyAdvisor(int dangerLevel, int disasterCount) {
        this.dangerLevel = dangerLevel;
        this.disasterCount = disasterCount;
    }

    @Override
    String adviseLevel() {
        if (dangerLevel + disasterCount >= 15)
            return "Critical";
        else if (dangerLevel >= 7)
            return "Balanced";
        else
            return "Minimal";
    }
}
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int type = sc.nextInt();
        Advisor advisor;

        if (type == 1) {
            int unrestLevel = sc.nextInt();
            advisor = new StrategicAdvisor(unrestLevel);
        } else {
            int dangerLevel = sc.nextInt();
            int disasterCount = sc.nextInt();
            advisor = new EmergencyAdvisor(dangerLevel, disasterCount);
        }

        System.out.println(advisor.adviseLevel());
        sc.close();
    }
}
```





## OUTPUT:

<img width="331" height="210" alt="image" src="https://github.com/user-attachments/assets/b9273826-9d78-4924-9f9c-45c97bbdc258" />


## RESULT:
Thus, the program successfully uses abstraction and method overriding to determine and display the correct advisory level based on the input conditions.
