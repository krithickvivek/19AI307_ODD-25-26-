# Ex.No:5(D) THREAD PRIORITY

## QUESTION:
Write a java program for determine the priority and name of the current thread.

## AIM:
To display the priority and name of a thread using Thread class.
## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read the thread name from user input using Scanner in the main method.
4. Create a Thread object by passing a Runnable instance and the user-given name.
5. Print the thread’s current priority and name using getPriority() and getName().
6. Start the thread to display complete Thread information via Thread.currentThread().

## PROGRAM:
 ```
/*
Program to implement a Thread Priority Concept using Java
Developed by: Krithick Vivekananda 
RegisterNumber: 212223240075
*/
```

## SOURCE CODE:

```
import java.util.*;

public class A implements Runnable {
    public void run() {
        System.out.println(Thread.currentThread());
    }

    public static void main(String[] args) {
        A a = new A();
        Scanner sc = new Scanner(System.in);
        String thname = sc.nextLine();
        Thread t = new Thread(a, thname);

        System.out.println("Priority of Thread: " + t.getPriority());
        System.out.println("Name of Thread: " + t.getName());
        t.start();
    }
}

```





## OUTPUT:

| Input      | Expected                                                                 | Got                                                                      | Status |
|------------|---------------------------------------------------------------------------|---------------------------------------------------------------------------|--------|
| NewThread  | Priority of Thread: 5<br>Name of Thread: NewThread<br>Thread[NewThread,5,main] | Priority of Thread: 5<br>Name of Thread: NewThread<br>Thread[NewThread,5,main] | ✓ |

**Passed all tests! ✓**


## RESULT:
Therefore, the program reads a thread name, prints its priority and name, and displays full thread details when executed.
