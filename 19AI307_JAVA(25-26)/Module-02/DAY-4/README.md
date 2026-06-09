# Ex.No:2(D) VARIABLE SCOPE AND CONSTRUCTOR

## AIM:
To write a Java program to access a static variable using both the class name and an object.

## ALGORITHM :
1.Start the program.

2.Create a class with a static variable.

3.Read the value for the static variable.

4.Access and display the static variable using the class name and an object.

5.Stop the program.


## PROGRAM:
 ```
/*
Program to implement a Variable scope and Constructor using Java
Developed by: KIRTHICK ROSHAN J
RegisterNumber:  212223040097
*/
```

## SOURCE CODE:
```
import java.util.Scanner;
class Demo {
    static int number;
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Demo.number = sc.nextInt();
        System.out.println("Accessing using class name: " + Demo.number);
        Demo obj = new Demo();
        System.out.println("Accessing using object: " + obj.number);

        sc.close();
    }
}
```





## OUTPUT:

<img width="675" height="263" alt="image" src="https://github.com/user-attachments/assets/5ab1caea-0526-4be1-bbee-abaac85aca04" />


## RESULT:
Thus, the program successfully accesses and displays the static variable using both the class name and an object.
