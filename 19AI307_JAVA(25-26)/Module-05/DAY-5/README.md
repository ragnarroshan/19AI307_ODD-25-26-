# Ex.No:5(E) MULTITHREADING -SYNCHRONIZATION

## AIM:
To write a Java program that swaps two integer values using a synchronized block and displays the swapped values.

## ALGORITHM :

1.Start the program.

2.Read two integer values a and b from the user.

3.Create a lock object for synchronization.

4.Use a synchronized block to swap the values of a and b.

5.Display the swapped values and stop the program.



## PROGRAM:
 ```
/*
Program to implement a Synchronization concept using Java
Developed by: kirthick roshan j
RegisterNumber:  212223040097
*/
```

## SOURCE CODE:

```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int a = sc.nextInt();
        int b = sc.nextInt();

        final Object lock = new Object();

        synchronized (lock) {
            int temp = a;
            a = b;
            b = temp;
        }

        System.out.println("a = " + a);
        System.out.println("b = " + b);
    }
}
```





## OUTPUT:
<img width="347" height="300" alt="image" src="https://github.com/user-attachments/assets/a5f51bf8-85ca-4c59-8e22-085eef821ec5" />



## RESULT:
Thus, the program successfully swaps the values of two integers using a synchronized block and displays the swapped values.
