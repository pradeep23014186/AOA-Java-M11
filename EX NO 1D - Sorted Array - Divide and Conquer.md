
# EX 1D Sorted Array using Divide and Conquer Approach.
## DATE: 17/04/2026
## AIM:
To write a Java program to for given constraints.
Given two sorted arrays nums1 and nums2 of size m and n respectively, return the median of the two sorted arrays.

The overall run time complexity should be O(log (m+n)).

## Algorithm
1. Start the program and read the sizes and elements of the two sorted arrays.
2. Initialize two pointers to traverse both arrays and compare elements one by one.
3. Repeatedly select the smaller element from the two arrays and move the corresponding pointer forward.
4. Continue the process until the middle position of the combined sorted array is reached.
5. If the total number of elements is odd, print the middle element; otherwise, print the average of the two middle elements and stop the program.
 

## Program:
```
Program to implement Reverse a String
Developed by: Krishna Prasad S
Register Number: 212223230108
```
```
import java.util.Scanner;

public class Solution 
{
    private int p1 = 0, p2 = 0;

    // Get the smaller value between nums1[p1] and nums2[p2], and move the pointer forward
    private int getMin(int[] nums1, int[] nums2) 
    {
        if (p1 < nums1.length && p2 < nums2.length) 
        {
            return nums1[p1] < nums2[p2] ? nums1[p1++] : nums2[p2++];
        } 
        else if (p1 < nums1.length) 
        {
            return nums1[p1++];
        } 
        lse if (p2 < nums2.length) 
        {
            return nums2[p2++];
        }
        return -1; 
    }

    // Main logic to find median of two sorted arrays
    public double findMedianSortedArrays(int[] nums1, int[] nums2) 
    {
        int tot = nums1.length + nums2.length;
        int prev = 0, curr = 0;
        for(int i=0; i<=tot/2; i++)
        {
           prev = curr;
           curr = getMin(nums1, nums2);
        }
        if(tot%2 == 1)
        {
            return curr;
        }
        return (prev + curr)/2.0;
    }

    // Main method with user input
    public static void main(String[] args) 
    {
        Scanner sc = new Scanner(System.in);
        Solution sol = new Solution();

        // Input for nums1
        // System.out.print("Enter size of first sorted array: ");
        int m = sc.nextInt();
        int[] nums1 = new int[m];
        // System.out.println("Enter " + m + " sorted integers for first array:");
        for (int i = 0; i < m; i++) 
        {
            nums1[i] = sc.nextInt();
        }

        // Input for nums2
        // System.out.print("Enter size of second sorted array: ");
        int n = sc.nextInt();
        int[] nums2 = new int[n];
        //System.out.println("Enter " + n + " sorted integers for second array:");
        for (int i = 0; i < n; i++) {
            nums2[i] = sc.nextInt();
        }

        // Find and display the median
        double median = sol.findMedianSortedArrays(nums1, nums2);
        System.out.println("Median of the two sorted arrays = " + median);
        
        sc.close();
    }
}
```

## Output:

<img width="892" height="346" alt="output4" src="https://github.com/user-attachments/assets/17320811-6eac-465d-98c6-f1b81733e8f1" />


## Result:
The program successfully implemented and the expected output is verified.
