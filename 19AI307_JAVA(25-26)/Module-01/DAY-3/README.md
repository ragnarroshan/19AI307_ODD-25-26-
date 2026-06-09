# Ex.No:1(C) LOOPING STATEMENT

## AIM:
To write a Java program to find the sum of the digits of a given non-negative integer using a while loop.

## ALGORITHM :

1.Start the program.

2.Read a non-negative integer from the user.

3.Initialize a variable sum to 0.

4.Use a while loop to extract each digit using % 10, add it to sum, and remove the digit using / 10.

5.Display the sum of digits and stop the program.

## PROGRAM:
 ```
/*
Program to implement a Looping Statement using Java
Developed by: KIRTHICK ROSAHN J
RegisterNumber:  212223040097
*/
```

## SOURCE CODE:

```
import java.util.Scanner;

public class SumOfDigits {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int num = sc.nextInt();

        int sum = 0;

        while (num > 0) {
            int digit = num % 10; 
            sum = sum + digit;   
            num = num / 10;     
        }

        System.out.println("Sum of digits: " + sum);
    }
}
```


## OUTPUT:

<img width="517" height="245" alt="image" src="https://github.com/user-attachments/assets/8a6b5978-0d31-4406-a4e2-65678ed1f04a" />


## RESULT:
Thus, the program successfully reads a non-negative integer and calculates the sum of its digits using a while loop.
