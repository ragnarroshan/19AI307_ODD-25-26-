# Ex.No:3(D)    INTERFACE 

## AIM:
To write a Java program using an interface and implementing classes SunBot and RainBot to predict weather conditions based on the given temperature.

## ALGORITHM :


1.Start the program.

2.Create an interface with a method predict().

3.Implement the interface in SunBot and RainBot classes with their respective prediction logic.

4.Read the temperature and bot type from the user, then create the corresponding bot object.

5.Call the predict() method, display the prediction, and stop the program.


## PROGRAM:
 ```
/*
Program to implement a Interface using Java
Developed by: KIRTHICK ROSHAN J
RegisterNumber:  212223040097
*/
```

## SOURCE CODE:

```
import java.util.*;
interface bot{
    void type(int n);
}
class sun implements bot{
    public void type(int n){
        if(n>30)
        System.out.println("HOT");
        else 
        System.out.println("MODERATE");
    }
}
class rain implements bot{
    public void type(int n){
        if(n<20)
        System.out.println("COLD");
        else
        System.out.println("WARM");
    }
}
class prog{
    public static void main(String[] args){
        Scanner sc=new Scanner(System.in);
        int n=sc.nextInt();
        int m=sc.nextInt();
        bot b;
        if(m==1)
        b=new sun();
        else
        b=new rain();
        b.type(n);
    }
}
```





## OUTPUT:
<img width="283" height="133" alt="image" src="https://github.com/user-attachments/assets/ceac0654-7ddc-4d8e-b387-83f49050850d" />



## RESULT:

Thus, the program successfully uses an interface and implementing classes to predict and display the weather condition based on the temperature and selected bot type.
