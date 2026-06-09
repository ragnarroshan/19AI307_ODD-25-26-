# Ex.No:4(A) EXCEPTION HANDLING

## AIM:

To write a Java program that uses a custom exception to reject negative numbers entered by the user.

## ALGORITHM :

1.Start the program.

2.Create a custom exception class (e.g., NegativeNumberException) that extends Exception.

3.Read an integer from the user.

4.If the number is negative, throw the custom exception with an appropriate message; otherwise, accept the number.

5.Catch the exception, display the error message, and stop the program.


## PROGRAM:
 ```
/*
Program to implement a Exception Handling using Java
Developed by:KIRTHICK ROSHAN J
RegisterNumber:  212223040097
*/
```

## SOURCE CODE:

```
import java.util.Scanner;

class NegativeNumberException extends Exception {
    NegativeNumberException(String message) {
        super(message);
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        try {
            int num = sc.nextInt();

            if (num < 0) {
                throw new NegativeNumberException("Negative numbers are not allowed");
            }

            System.out.println("Valid input: " + num);

        } catch (NegativeNumberException e) {
            System.out.println(e.getMessage());
        }
    }
}
```






## OUTPUT:

<img width="750" height="246" alt="image" src="https://github.com/user-attachments/assets/51688c28-88ff-4e1f-b5c6-3b73279d3b53" />



## RESULT:

Thus, the program successfully uses a custom exception to detect and handle negative numbers by displaying an appropriate error message when a negative value is entered.
