# Ex.No:2(A) CLASS AND OBJECT

## AIM:
To write a Java program that creates a class with a method and invokes the method using an object.

## ALGORITHM :

1.Start the program.

2.Create a class prog with a method speak().

3.Inside the speak() method, print "I am an animal".

4.Create an object of the class in the main() method and call speak().

5.Display the output and stop the program.


## PROGRAM:
 ```
/*
Program to implement a Class and Objects using Java
Developed by: KIRTHICK ROSAHN J
RegisterNumber:  21222300097
*/
```

## SOURCE CODE:
```
class prog {
    void speak() {
        System.out.println("I am an animal");
    }

    public static void main(String[] args) {
        prog obj = new prog();
        obj.speak();
    }
}
```

## OUTPUT:

<img width="397" height="148" alt="image" src="https://github.com/user-attachments/assets/c4b1ff40-f801-474b-bd9d-38bd5e314286" />


## RESULT:

Thus, the class prog with the method speak() was created successfully, and the message "I am an animal" was displayed using an object.
