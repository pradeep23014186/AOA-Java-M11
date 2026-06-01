# EX 1A Print All Numbers 
## DATE: 16/04/2026
## AIM:
To Write a Java program that takes an integer input N from the user and prints all the numbers from 1 to N, separated by spaces, on a single line..

## Algorithm
1. Start the program.
2. Read the integer value N from the user.
3. Check whether N is less than 0.
4. If N is negative, print "Invalid input".
5. Otherwise, use a loop to print numbers from 1 to N separated by spaces and stop the program.  

## Program:
```
Program to implement Reverse a String
Developed by: Krishna Prasad S
Register Number: 212223230108
```
```java
import java.util.Scanner;

public class Main
{
    public static void main(String args[])
    {
        Scanner sn = new Scanner(System.in);
        int n = sn.nextInt();
        if(n < 0){System.out.println("Invalid input");}
        else{
            for(int i=1; i<=n; i++)
                System.out.print(i + " ");
        }
    }
}
```

## Output:
<img width="440" height="160" alt="output1" src="https://github.com/user-attachments/assets/15e7d4a4-6095-4e17-a465-eedd205d1a23" />


## Result:
The program successfully print all the numbers from 1 to N. 
