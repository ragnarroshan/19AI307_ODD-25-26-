# Ex.No:3(F) WRAPPER CLASS

## AIM:

To write a Java program that converts a string to an integer using a wrapper class and performs addition.

## ALGORITHM :

1.Start the program.

2.Read the string input from the user.

3.Convert the string into an integer using the Integer wrapper class (Integer.parseInt()).

4.Add the converted integer value with itself and store the result.

5.Display the sum and stop the program.




## PROGRAM:
 ```
/*
Program to implement a Wrapper Class using Java
Developed by: KIRTHICK ROSHAN J
RegisterNumber:  212223040097
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

class prog {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        String str1 = sc.nextLine();
        String str2 = sc.nextLine();

        int num1 = Integer.parseInt(str1);
        int num2 = Integer.parseInt(str2);

        int sum = num1 + num2;

        System.out.println("Sum = " + sum);
    }
}
```






## OUTPUT:


<img width="347" height="270" alt="image" src="https://github.com/user-attachments/assets/7e4d2ef9-46de-43e1-ab4a-f6aab8434092" />



## RESULT:

Thus, the program successfully converts a string to an integer using the Integer wrapper class and performs the addition operation.
