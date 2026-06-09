# Ex.No:5(D) THREAD PRIORITY

## AIM:
To write a Java program that creates a thread, assigns a user-specified name and priority, and displays the thread details.

## ALGORITHM :

1.Start the program.

2.Read the thread name and priority from the user.

3.Create a new thread object.

4.Set the thread's name and priority using setName() and setPriority().

5.Display the thread name and priority, then stop the program.


## PROGRAM:
 ```
/*
Program to implement a Thread Priority Concept using Java
Developed by: kirthick roshan j
RegisterNumber: 212223040097
*/
```

## SOURCE CODE:

```
import java.util.Scanner;

class MyThread extends Thread {
    MyThread(String name, int priority) {
        super(name);
        setPriority(priority);
    }
}

public class Main {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        String threadName = sc.nextLine();
        int priority = Integer.parseInt(sc.nextLine().trim());

        MyThread t = new MyThread(threadName, priority);

        System.out.println("Thread " + t.getName() + " priority is " + t.getPriority());

        sc.close();
    }
}
```





## OUTPUT:
<img width="737" height="297" alt="image" src="https://github.com/user-attachments/assets/9f30c4ca-2459-469e-85bc-e07ede24ff3e" />



## RESULT:
Thus, the program successfully creates a thread, assigns the specified name and priority, and displays the thread information.
