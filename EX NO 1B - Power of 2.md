
# EX 1B Power of 2
## DATE: 17/04/2026
## AIM:
To write a Java program to for given constraints.Given an integer n, return true if it is a power of two. Otherwise, return false.

An integer n is a power of two, if there exists an integer x such that n == 2x.

## Algorithm
1. Start the program.
2. Read the integer value n from the user.
3. Use the bitwise AND operation (n & (n-1)) to check whether n is a power of 2.
4. If the result is 0, print true; otherwise, print false.
5. Stop the program. 

## Program:
```
Program to implement Reverse a String
Developed by: Krishna Prasad S
Register Number: 212223230108
```
```java
import java.util.Scanner;

public class Solution 
{
    public boolean isPowerOfTwo(int n) 
    {
        return ((n & (n-1)) == 0);
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        Solution sol = new Solution();
        int n = scanner.nextInt();

        boolean result = sol.isPowerOfTwo(n);
        System.out.println(result);

        scanner.close();
    }
}

```

## Output:

<img width="395" height="209" alt="output2" src="https://github.com/user-attachments/assets/640b970b-4179-4510-9628-7dcfb00c67aa" />

## Result:
The program successfully implemented and the expected output is verified.
