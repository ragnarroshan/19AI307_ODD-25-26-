# Ex.No:5(B) SERIALIZATION AND DESERIALIZATION 

## AIM:
To write a Java program that serializes an ArrayList<Student> into a file and then deserializes it back to retrieve and display the stored student objects.

## ALGORITHM :

1.Start the program.

2.Create a Student class that implements the Serializable interface.

3.Read student details from the user and store them in an ArrayList<Student>.

4.Serialize the ArrayList into a file using ObjectOutputStream, then deserialize it using ObjectInputStream.

5.Display the deserialized student objects and stop the program.

## PROGRAM:
 ```
/*
Program to implement a Serialization and Deserialization using Java
Developed by: kirthick roshan j
RegisterNumber:  212223040097
*/
```

## SOURCE CODE:

```
import java.io.*;
import java.util.*;

class Student implements Serializable {
    private static final long serialVersionUID = 1L;

    private int id;
    private String name;
    private double marks;

    public Student(int id, String name, double marks) {
        this.id = id;
        this.name = name;
        this.marks = marks;
    }

    @Override
    public String toString() {
        return "Student{id=" + id + ", name='" + name + "', marks=" + marks + "}";
    }
}

public class StudentSerializationUserInput {

    
    public static void serializeStudents(List<Student> students, String fileName) {
        try (ObjectOutputStream oos = new ObjectOutputStream(new FileOutputStream(fileName))) {
            oos.writeObject(students);
            System.out.println("Students serialized successfully into: " + fileName);
        } catch (IOException e) {
            System.out.println("Error during serialization: " + e.getMessage());
        }
    }

    
    @SuppressWarnings("unchecked")
    public static List<Student> deserializeStudents(String fileName) {
        List<Student> students = null;
        try (ObjectInputStream ois = new ObjectInputStream(new FileInputStream(fileName))) {
            students = (List<Student>) ois.readObject();
            System.out.println("Students deserialized successfully from: " + fileName);
        } catch (IOException | ClassNotFoundException e) {
            System.out.println("Error during deserialization: " + e.getMessage());
        }
        return students;
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        List<Student> students = new ArrayList<>();

        int n = scanner.nextInt();
        scanner.nextLine();

        for (int i = 0; i < n; i++) {
            int id = scanner.nextInt();
            scanner.nextLine();

            String name = scanner.nextLine();

            double marks = scanner.nextDouble();
            scanner.nextLine();

            students.add(new Student(id, name, marks));
        }

        String fileName = "students.dat";

        serializeStudents(students, fileName);

        List<Student> deserializedStudents = deserializeStudents(fileName);

        
        if (deserializedStudents != null) {
            System.out.println("\nDeserialized Students:");
            for (Student s : deserializedStudents) {
                System.out.println(s);
            }
        }

        scanner.close();
    }
}
```





## OUTPUT:

<img width="1153" height="433" alt="image" src="https://github.com/user-attachments/assets/f123161e-48ea-420d-bb3f-6b2e9ab3a655" />


## RESULT:
Thus, the program successfully serializes and deserializes a collection of Student objects using Java object streams and displays the retrieved data correctly.
