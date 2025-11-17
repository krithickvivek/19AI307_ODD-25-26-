# Ex.No:3(F) WRAPPER CLASS

## QUESTION:
Write a Java program to check if a number is prime using wrapper classes. 
## AIM:
To check whether a number is prime using Java wrapper class Integer.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read a number from the user and store it inside an Integer object.
4. If the number is less than or equal to one, mark it as not prime.
5. Loop from two to half of the number and check divisibility for factors.
6. Print whether the number is prime or not based on the flag value.


## PROGRAM:
 ```
/*
Program to implement a Wrapper Class using Java
Developed by: Krithick Vivekananda 
RegisterNumber: 212223240075
*/
```

## SOURCE CODE:
```
import java.util.*;
public class PrimeCheck {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Integer number = sc.nextInt();
        boolean isPrime = true;

        if (number <= 1) {
            isPrime = false;
        } else {
            for (int i = 2; i <= number / 2; i++) {
                if (number % i == 0) {
                    isPrime = false;
                    break;
                }
            }
        }

        if (isPrime)
            System.out.println(number + " is a prime number.");
        else
            System.out.println(number + " is not a prime number.");
    }
}

```

## OUTPUT:
| Input | Expected                         | Got                              | Status |
|-------|-----------------------------------|-----------------------------------|--------|
| 29    | 29 is a prime number.            | 29 is a prime number.            | ✓ |
| 153   | 153 is not a prime number.       | 153 is not a prime number.       | ✓ |
| 7     | 7 is a prime number.             | 7 is a prime number.             | ✓ |

**Passed all tests! ✓**

## RESULT:
Therefore, the program uses an Integer wrapper, checks for factors, and prints whether the given number is prime or not.
