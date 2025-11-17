# Ex.No:2(C) ACCESS SPECIFIERS

## QUESTION:
Write a Java program to create a class called Smartphone with private instance variables brand, model, and storageCapacity. Provide public getter and setter methods to access and modify these variables. Add a method called increaseStorage() that takes an integer value and increases the storageCapacity by that value.

## AIM:
To manage smartphone details using getters, setters, and a storage update method.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read brand, model, initial storage, and increment value from user input.
4. Assign these inputs to the Smartphone object using appropriate setter methods.
5. Call increaseStorage to add the given value to current storage capacity.
6. Use the display method to print brand, model, and updated storage capacity clearly.

## PROGRAM:
 ```
/*
Program to implement a Access Specifiers using Java
Developed by: Krithick Vivekananda 
RegisterNumber: 212223240075
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

class prog {
    private String brand;
    private String model;
    private int storageCapacity;

    
    public String getBrand() {
        return brand;
    }

    public String getModel() {
        return model;
    }

    public int getStorageCapacity() {
        return storageCapacity;
    }

    
    public void setBrand(String brand) {
        this.brand = brand;
    }

    public void setModel(String model) {
        this.model = model;
    }

    public void setStorageCapacity(int storageCapacity) {
        this.storageCapacity = storageCapacity;
    }

   
    public void increaseStorage(int value) {
        if (value > 0) {
            this.storageCapacity += value;
        }
    }

    
    public void display() {
        System.out.println("Brand: " + brand);
        System.out.println("Model: " + model);
        System.out.println("Updated Storage Capacity: " + storageCapacity + " GB");
        System.out.println("------------------------------");
    }
    
    public static void main(String[] args)
    {
        Scanner sc = new Scanner(System.in);
        prog s = new prog();
        String brand = sc.nextLine();
        String model = sc.nextLine();
        int storageCapacity = sc.nextInt();
        int value = sc.nextInt();
        s.setBrand(brand);
        s.setModel(model);
        s.setStorageCapacity(storageCapacity);
        s.increaseStorage(value);
        s.display();
        
    }
}
```

## OUTPUT:
| Test     | Input                                         | Expected                                                                 | Got                                                                      | Status |
|----------|-----------------------------------------------|---------------------------------------------------------------------------|---------------------------------------------------------------------------|--------|
| Samsung  | Samsung<br>Galaxy S21<br>128<br>64            | Brand: Samsung<br>Model: Galaxy S21<br>Updated Storage Capacity: 192 GB<br>------------------------------ | Brand: Samsung<br>Model: Galaxy S21<br>Updated Storage Capacity: 192 GB<br>------------------------------ | ✓ |
| Apple    | Apple<br>iPhone 14<br>256<br>128              | Brand: Apple<br>Model: iPhone 14<br>Updated Storage Capacity: 384 GB<br>------------------------------ | Brand: Apple<br>Model: iPhone 14<br>Updated Storage Capacity: 384 GB<br>------------------------------ | ✓ |
| OnePlus  | OnePlus<br>Nord CE 3<br>128<br>128            | Brand: OnePlus<br>Model: Nord CE 3<br>Updated Storage Capacity: 256 GB<br>------------------------------ | Brand: OnePlus<br>Model: Nord CE 3<br>Updated Storage Capacity: 256 GB<br>------------------------------ | ✓ |

**Passed all tests! ✓**


## RESULT:
Therefore, the program stores smartphone details, updates the storage value, and displays the final information using proper encapsulation.
