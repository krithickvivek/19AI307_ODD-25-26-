# Ex.No:3(C) ABSTRACTION

## QUESTION:
Create an abstract class TaxPayer with method calculateTax(). Create subclasses SalariedPerson and BusinessPerson.
## AIM:
To compute tax for different taxpayer types using abstraction and subclasses.
## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read taxpayer type and income from user using Scanner input values.
4. Create the correct subclass object depending on whether the user selects salaried or business.
5. Call the overridden calculateTax method to compute tax based on income rules.
6. Print the calculated tax amount formatted to two decimal places for clarity.

## PROGRAM:
 ```
/*
Program to implement a Abstraction using Java
Developed by: Krithick Vivekananda 
RegisterNumber: 212223240075
*/
```

## SOURCE CODE:
```
import java.util.*;

abstract class TaxPayer {
    abstract double calculateTax();
}

class SalariedPerson extends TaxPayer {
    double income;
    SalariedPerson(double income) {
        this.income=income;
    }
    double calculateTax() {
        return income * 0.10; 
    }
}

class BusinessPerson extends TaxPayer {
    double income;
    BusinessPerson(double income) {
        this.income=income;
    }
    double calculateTax() {
        return income * 0.15; 
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int type = sc.nextInt();  
        double income = sc.nextDouble();
        
        TaxPayer tp;
        if (type == 1) {
            tp = new SalariedPerson(income);
        } else {
            tp = new BusinessPerson(income);
        }
        
        System.out.printf("%.2f", tp.calculateTax());
    }
}

```

## OUTPUT:
| Input            | Expected   | Got        | Status |
|------------------|------------|------------|--------|
| 1<br>50000       | 5000.00    | 5000.00    | ✓ |
| 2<br>100000      | 15000.00   | 15000.00   | ✓ |
| 1<br>72500       | 7250.00    | 7250.00    | ✓ |
| 2<br>40000       | 6000.00    | 6000.00    | ✓ |

**Passed all tests! ✓**



## RESULT:
Therefore, the program uses an abstract class with subclasses to calculate and display tax based on the taxpayer’s category and income.
