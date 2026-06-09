# Ex.No:3(A) INHERITANCE AND AGGREGATION


## AIM:
To write a Java program that demonstrates inheritance by creating a superclass Person and a subclass Student, and calculates the grade based on the student's marks.

## ALGORITHM :

1.Start the program.

2.Create a superclass Person with fields name and age.

3.Create a subclass Student that inherits from Person and adds a field marks.

4.Implement the calculateGrade() method to determine the grade based on the marks obtained.

5.Display the grade and stop the program.




## PROGRAM:
 ```
/*
Program to implement a Inheritance and Aggregation using Java
Developed by: KIRTHICK ROSHAN  J
RegisterNumber:  212223040097
*/
```

## SOURCE CODE:

```
import java.util.*;
class Person {
    String name;
    int age;
}
class Student extends Person {
    int marks;
    void calculateGrade(int marks) {
        if (marks >= 90) {
            System.out.println("Grade: A");
        } 
        else if (marks >= 75) {
            System.out.println("Grade: B");
        } 
        else if (marks >= 50) {
            System.out.println("Grade: C");
        } 
        else {
            System.out.println("Grade: F");
        }
    }
}
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Student s = new Student();
        s.name = sc.next();
        s.age = sc.nextInt();
        s.marks = sc.nextInt();
        System.out.println("Name: " + s.name);
        System.out.println("Age: " + s.age);
        System.out.println("Marks: " + s.marks);
        s.calculateGrade(s.marks);
    }
}
```



## OUTPUT:

<img width="427" height="513" alt="image" src="https://github.com/user-attachments/assets/8789d753-20e1-49fb-9d39-a1e3c01c7c91" />


## RESULT:
Thus, the superclass Person and subclass Student were created successfully, and the grade was calculated based on the student's marks using the calculateGrade() method.
