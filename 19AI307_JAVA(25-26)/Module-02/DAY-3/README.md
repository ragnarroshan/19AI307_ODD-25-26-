# Ex.No:2(C) ACCESS SPECIFIERS

## AIM:
To create a Java program that demonstrates encapsulation using a Student class with private variables, getter and setter methods, and grade validation.

## ALGORITHM :

1.Start the program.

2.Create a Student object and read student ID, name, and grade.

3.Set the student ID and name using setter methods.

4.Validate and add the grade using the addGrade() method.

5.Display the student details if the grade is valid; otherwise, display an error message.



## PROGRAM:
 ```
/*
Program to implement a Access Specifiers using Java
Developed by: KIRTHICK ROSHAN J
RegisterNumber:  212223040097
*/
```

## SOURCE CODE:

```
import java.util.Scanner;

class Student {
    private int student_id;
    private String student_name;
    private int grade; 
    public void setStudentId(int student_id) {
        this.student_id = student_id;
    }

    public void setStudentName(String student_name) {
        this.student_name = student_name;
    }
    public int getStudentId() {
        return student_id;
    }

    public String getStudentName() {
        return student_name;
    }

    public int getGrade() {
        return grade;
    }
    public boolean addGrade(int grade) {
        if (grade >= 0 && grade <= 100) {
            this.grade = grade;
            return true;
        } else {
            return false;
        }
    }

    public void display() {
        System.out.println("Student ID: " + student_id);
        System.out.println("Student Name: " + student_name);
        System.out.println("Grade: " + grade);
        System.out.println("-----------------------");
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        Student s = new Student();

        int id = sc.nextInt();
        sc.nextLine(); 
        String name = sc.nextLine();
        int grade = sc.nextInt();

        s.setStudentId(id);
        s.setStudentName(name);

        boolean isValid = s.addGrade(grade);

        if (isValid) {
            s.display();
        } else {
            System.out.println("Invalid grade. Please enter a value between 0 and 100.");
        }

        sc.close();
    }
}
```





## OUTPUT:
<img width="1152" height="482" alt="image" src="https://github.com/user-attachments/assets/848c3e97-1296-4335-a17c-bfa53d33b07b" />



## RESULT:
Thus, the Student class with private variables, getter and setter methods, and grade validation through the addGrade() method was implemented successfully.
