
# EX 1C Valid Pairs using Brute Force Approach
## DATE: 17/04/2026
## AIM:
To write a Java program to for given constraints.
Given an integer array nums and an integer k, return the number of pairs (i, j) where i < j such that |nums[i] - nums[j]| == k.

The value of |x| is defined as:

x if x >= 0.
-x if x < 0.

## Algorithm
1. Start the program and read the size of the array n.
2. Read the array elements and the value of k from the user.
3. Use a HashMap to store the frequency of elements encountered.
4. For each element, check whether (n + k) or (n - k) exists in the map and update the count of valid pairs.
5. Print the total number of valid pairs and stop the program.  

## Program:
```
Program to implement Reverse a String
Developed by: Krishna Prasad S
Register Number: 212223230108
```
```
import java.util.*;
public class CountPairsWithDifference 
{
    public static int countKDifference(int[] nums, int k) 
    {
        int count = 0;
        Map<Integer, Integer> map = new HashMap<>();
        for(int n : nums)
        {
            if(map.containsKey(n+k))
            {
                count += map.get(n+k);
            }
            if(map.containsKey(n-k))
            {
                count += map.get(n-k);
            }
            map.put(n, map.getOrDefault(n, 0)+1);
        }
        return count;
    }
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int[] nums = new int[n];
        for (int i = 0; i < n; i++) {
            nums[i] = sc.nextInt();
        }
        int k = sc.nextInt();
        int result = countKDifference(nums, k);
        System.out.println(result);
        sc.close();
    }
}

```

## Output:

<img width="431" height="299" alt="output3" src="https://github.com/user-attachments/assets/b3b80376-10f7-4710-9cda-6df0666c2889" />


## Result:
The program successfully implemented and the expected output is verified.
