# Ex.No:2(B) METHODS

## AIM:
To write a Java program that defines a method square(int number) to calculate and return the square of a given number.

## ALGORITHM :

1.Start the program.

2.Define a method square(int number) that returns number * number.

3.Read the input number from the user.

4.Call the square() method and store the returned value.

5.Display the square of the number and stop the program.

## PROGRAM:
 ```
/*
Program to implement a Methods using Java
Developed by: KIRTHICK ROSHAN J
RegisterNumber:  212223040097
*/
```

## SOURCE CODE:

```
import java.util.Scanner;

class prog {

    int square(int number) {
        return number * number;
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int number = sc.nextInt();

        prog obj = new prog();
        int result = obj.square(number);

        System.out.println(result);
    }
}
```


## OUTPUT:

<img width="326" height="148" alt="image" src="https://github.com/user-attachments/assets/555041cd-bf19-41d6-8099-3de57300a6b0" />


## RESULT:
Thus, the method square(int number) was created successfully and returns the square of the given number.
