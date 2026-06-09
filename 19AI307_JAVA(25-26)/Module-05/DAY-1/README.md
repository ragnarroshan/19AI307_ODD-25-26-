# Ex.No:5(A) INPUTSTREAMREADER 

## AIM:

To write a Java program that simulates inter-thread communication using PipedInputStream and PipedOutputStream, where one thread writes user-provided data and another thread reads and displays it.

## ALGORITHM :

1.Start the program.

2.Create and connect a PipedOutputStream and a PipedInputStream.

3.Create a writer thread that accepts input from the user and writes it to the pipe.

4.Create a reader thread that reads data from the pipe and displays it.

5.Start both threads, complete the communication, and stop the program.


## PROGRAM:
 ```
/*
Program to implement a InputStreamReader using Java
Developed by: kirthick roshan j
RegisterNumber:  212223040097
*/
```

## SOURCE CODE:

```
import java.io.*;
import java.util.Scanner;

class WriterThread extends Thread {
    PipedOutputStream pos;
    String data;

    WriterThread(PipedOutputStream pos, String data) {
        this.pos = pos;
        this.data = data;
    }

    public void run() {
        try {
            pos.write(data.getBytes());
            pos.close();
        } catch (IOException e) {
            System.out.println("Writer error");
        }
    }
}

class ReaderThread extends Thread {
    PipedInputStream pis;

    ReaderThread(PipedInputStream pis) {
        this.pis = pis;
    }

    public void run() {
        try {
            int i;
            StringBuilder sb = new StringBuilder();

            while ((i = pis.read()) != -1) {
                sb.append((char) i);
            }

            System.out.println("ReaderThread received: " + sb.toString());

            pis.close();
        } catch (IOException e) {
            System.out.println("Reader error");
        }
    }
}

public class Main {
    public static void main(String[] args) {
        try {
            Scanner sc = new Scanner(System.in);
            String input = sc.nextLine();

            PipedOutputStream pos = new PipedOutputStream();
            PipedInputStream pis = new PipedInputStream(pos);

            ReaderThread rt = new ReaderThread(pis);
            WriterThread wt = new WriterThread(pos, input);

            rt.start();
            wt.start();

        } catch (IOException e) {
            System.out.println("Connection error");
        }
    }
}
```






## OUTPUT:
<img width="1158" height="127" alt="image" src="https://github.com/user-attachments/assets/fd9fdec4-03c7-49ce-bc67-a10185a7fa9e" />



## RESULT:
Thus, the program successfully demonstrates inter-thread communication using PipedInputStream and PipedOutputStream, where data written by one thread is received and displayed by another thread.
