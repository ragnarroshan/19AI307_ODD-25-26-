# Ex.No:3(E) INNER CLASS


## AIM:
To write a Java program that creates an inner class and accesses its method from the outer class.

## ALGORITHM :

1.Start the program.

2.Create an outer class and define an inner class inside it.

3.Read the user's name as input.

4.Create an object of the inner class through the outer class and call its method.

5.Display the greeting message and stop the program.



## PROGRAM:
 ```
/*
Program to implement a InnerClass using Java
Developed by:  KIRTHICK ROSHAN J
RegisterNumber:  212223040097
*/
```

## SOURCE CODE:

```
import java.util.Scanner;

class prog {

    class Inner {
        void display(String name) {
            System.out.println("Hello, " + name + "! This message is from the Inner Class.");
        }
    }

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        String name = sc.nextLine();

        prog obj = new prog();
        prog.Inner in = obj.new Inner();

        in.display(name);
    }
}
```






## OUTPUT:


<img width="1013" height="207" alt="image" src="https://github.com/user-attachments/assets/f9dd9863-0f06-4b21-b595-f7d8acf0181a" />


## RESULT:

Thus, the program successfully creates an inner class and accesses it from the outer class to display the required message.
