# Ex.No:2(E) ACCESS MODIFIERS

## AIM:
To write a Java program to create a class with a final variable and display its value using an object.

## ALGORITHM :

1.Start the program.

2.Create a class College with a final variable universityName.

3.Create an object of the College class in the main() method.

4.Access and print the value of universityName using the object.

5.Stop the program.


## PROGRAM:
 ```
/*
Program to implement a Access Modifiers using Java
Developed by: KIRTHICK ROSHAN  J
RegisterNumber:  212223040097
*/
```

## SOURCE CODE:


```
import java.util.*;
class College {
    final String universityName = "Saveetha University";
}
class prog{
    public static void main(String[] args){
        College c = new College();
        System.out.println(c.universityName);
        
        
    }
}
```




## OUTPUT:

<img width="447" height="131" alt="image" src="https://github.com/user-attachments/assets/7089617b-ca04-417f-9f75-8975d9bb6fcf" />


## RESULT:

Thus, the class College with the final variable universityName was created successfully, and its value "Saveetha University" was displayed using an object.
