# Ex.No:1(D) ARRAYS

## QUESTION:
Write a Java Program to count Even and Odd Numbers in an Array.

## AIM:
To count how many even and odd numbers are present in an array.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read the array size and input all elements from the user.
4. Initialize counters for even numbers and odd numbers to zero.
5. Traverse each element, check divisibility by two, and update respective counter.
6. Print the total even count and odd count after completing the loop.

## PROGRAM:
 ```
/*
Program to implement a Array concept using Java
Developed by: Krithick Vivekananda 
RegisterNumber: 212223240075
*/
```

## SOURCE CODE:
```
import java.util.*;
public class demo
{
    public static void main(String[] args)
    {
        Scanner sc = new Scanner(System.in);
        int n=sc.nextInt();
        int arr[] = new int[n];
        for (int i=0; i<n; i++)
        {
            arr[i]=sc.nextInt();
        }
        int even=0, odd=0;
        for(int i=0; i<n; i++)
        {
            if(arr[i] % 2==0) even+=1;
            else odd+=1;
        }
        System.out.println("Number of even elements: "+even);
        System.out.println("Number of odd elements: "+odd);
    }
}
```
## OUTPUT:
| Input | Expected                                                   | Got                                                        | Status |
|-------|-------------------------------------------------------------|-------------------------------------------------------------|--------|
| 5<br>1<br>2<br>3<br>4<br>5 | Number of even elements: 2<br>Number of odd elements: 3 | Number of even elements: 2<br>Number of odd elements: 3 | ✓ |
| 6<br>0<br>1<br>2<br>3<br>4<br>5 | Number of even elements: 3<br>Number of odd elements: 3 | Number of even elements: 3<br>Number of odd elements: 3 | ✓ |
| 3<br>1<br>3<br>7 | Number of even elements: 0<br>Number of odd elements: 3 | Number of even elements: 0<br>Number of odd elements: 3 | ✓ |

**Passed all tests! ✓**


## RESULT:
Therefore, the program reads the array values, checks each element, and accurately prints how many numbers are even and how many are odd.
