# Ex.No:1(D) ARRAYS

## AIM:
To write a Java program to count the number of elements in an array that are divisible by 3 or 5.

## ALGORITHM :

1.Start the program.

2.Read the size of the array and its elements.

3.Initialize a counter variable to 0.

4.Traverse the array and check if each element is divisible by 3 or 5; if true, increment the counter.

5.Display the count and stop the program.


## PROGRAM:
 ```
/*
Program to implement a Array concept using Java
Developed by: KIRTHICK ROSAHN J
RegisterNumber:  212223040097
*/
```

## SOURCE CODE:

```
import java.util.Scanner;

public class DivisibilityCount {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int n = scanner.nextInt();
        int[] arr = new int[n];
        for (int i = 0; i < n; i++) {
            arr[i] = scanner.nextInt();
        }
        int count = 0;
        for (int i = 0; i < n; i++) {
            if (arr[i] % 3 == 0 || arr[i] % 5 == 0) {
                count++;
            }
        }
        System.out.println(count);
        
        scanner.close();
    }
}
```

## OUTPUT:

<img width="332" height="497" alt="image" src="https://github.com/user-attachments/assets/1e9e760f-3bc4-42d0-8bf8-53ab47ad4b6f" />


## RESULT:
Thus, the program successfully counts and displays the number of array elements that are divisible by 3 or 5.
