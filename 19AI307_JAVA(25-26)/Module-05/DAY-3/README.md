# Ex.No:5(C)  FILE HANDLING USING JAVA

## AIM:
To write a Java program that reads the contents of a file and counts the total number of words present in it.

## ALGORITHM :

1.Start the program.

2.Read the text and write it into a file.

3.Open the file and read its contents line by line.

4.Split each line into words using spaces as delimiters and count them.

5.Display the total number of words and stop the program.


## PROGRAM:
 ```
/*
Program to implement a File Handling using Java
Developed by:kirthick roshan j
RegisterNumber:  212223040097
*/
```

## SOURCE CODE:

```
import java.io.BufferedReader;
import java.io.FileReader;
import java.io.IOException;
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        String content = sc.nextLine();

        String fileName = "input.txt";

        try {
            
            java.io.FileWriter fw = new java.io.FileWriter(fileName);
            fw.write(content);
            fw.close();

            
            BufferedReader br = new BufferedReader(new FileReader(fileName));

            String line = br.readLine();
            int wordCount = 0;

            if (line != null) {
                String[] words = line.trim().split("\\s+");
                wordCount = words.length;
            }

            br.close();

            System.out.println("Number of words in the file: " + wordCount);

        } catch (IOException e) {
            System.out.println("Error occurred");
        }

        sc.close();
    }
}
```





## OUTPUT:

<img width="1052" height="227" alt="image" src="https://github.com/user-attachments/assets/7a02705c-d281-4ff0-95b6-cfb238432f70" />


## RESULT:
Thus, the program successfully reads the contents of a file and counts the total number of words present in it.
