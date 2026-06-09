# Ex.No:4(B)  IMPLEMENT SOLID PRINCIPLES IN JAVA PROGRAM 

## AIM:

To write a Java program that implements the Singleton Design Pattern to manage a shared print spooler and track the total number of print jobs submitted while following the SOLID Principles.

## ALGORITHM :


1.Create a Singleton class PrintSpoolerManager with a private constructor and a static instance.

2.Define an interface for print job operations to achieve abstraction.

3.Implement the interface in the Singleton class and maintain a shared job counter.

4.Read the number of print jobs and department names from the user.

5.Use the Singleton instance to process each print job, update the queue count, and display the submission details.


## PROGRAM:
 ```
/*
Program to implement a SOLID Principles in Java Program
Developed by: KIRTHICK ROSHAN J
RegisterNumber:  212223040097
*/
```

## SOURCE CODE:


```
import java.util.Scanner;

class PrintSpoolerManager {
    private static PrintSpoolerManager instance;
    private int jobCount;

    private PrintSpoolerManager() {
        jobCount = 0;
    }

    public static PrintSpoolerManager getInstance() {
        if (instance == null) {
            instance = new PrintSpoolerManager();
        }
        return instance;
    }

    public void submitJob(String department) {
        jobCount++;
        System.out.println(department + " submitted a print job. Total Jobs in Queue: " + jobCount);
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();
        sc.nextLine();

        PrintSpoolerManager manager = PrintSpoolerManager.getInstance();

        for (int i = 0; i < n; i++) {
            String department = sc.nextLine();
            manager.submitJob(department);
        }
    }
}
```





## OUTPUT:

<img width="1113" height="370" alt="image" src="https://github.com/user-attachments/assets/227a354c-5650-4289-a301-b60ba1ea58c4" />


## RESULT:
Thus, the program successfully implements the Singleton Design Pattern while adhering to the SOLID Principles, ensuring a single shared print spooler manager and maintaining the total number of print jobs submitted across all departments.
