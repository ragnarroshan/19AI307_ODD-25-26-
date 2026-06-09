# Ex.No:1(E) STRINGS AND MATH FUNCTION

## AIM:
To write a Java program to count the number of vowels present in a given string.

## ALGORITHM :

1.Start the program.

2.Read the input string from the user.

3.Initialize a counter variable to 0.

4.Traverse each character of the string and check whether it is a vowel (a, e, i, o, u in either case); if true, increment the counter.

5.Display the total number of vowels and stop the program.

## PROGRAM:
 ```
/*
Program to implement a Strings and Math Function using Java
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

        String str = sc.nextLine();
        int count = 0;

        for (int i = 0; i < str.length(); i++) {
            char ch = Character.toLowerCase(str.charAt(i));

            if (ch == 'a' || ch == 'e' || ch == 'i' || ch == 'o' || ch == 'u') {
                count++;
            }
        }

        System.out.println("Number of vowels: " + count);

        sc.close();
    }
}

```



## OUTPUT:

<img width="583" height="233" alt="image" src="https://github.com/user-attachments/assets/0f369479-677c-4874-b5dd-2afb45c75484" />


## RESULT:
Thus, the program successfully counts and displays the number of vowels present in the given string.
