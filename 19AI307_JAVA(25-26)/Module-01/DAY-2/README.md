# Ex.No:1(B) CONDITIONAL STATEMENT

## AIM: 
To write a Java program to determine whether the first player can win the Chocolate Game based on the given dimensions of the chocolate bar.

## ALGORITHM :

1.Start the program.

2.Read the values of n and m from the user.

3.Calculate the product n × m.

4.If the product is even, print "yes"; otherwise, print "no".

5.Stop the program.

## PROGRAM:
 ```
/*
Program to implement a conditional statement using Java
Developed by: KIRTHICK ROSAHN J
RegisterNumber:  212223040097
*/
```

## SOURCE CODE:

```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();
        int m = sc.nextInt();

        if ((n * m) % 2 == 0) {
            System.out.println("yes");
        } else {
            System.out.println("no");
        }
    }
}
```

## OUTPUT:

<img width="328" height="203" alt="image" src="https://github.com/user-attachments/assets/61b6da9c-aea0-43cb-b0b2-9753190e0e8d" />


## RESULT:
Thus, the program successfully reads the dimensions of the chocolate bar and determines whether the first player can guarantee a win by displaying "yes" or "no" accordingly.
