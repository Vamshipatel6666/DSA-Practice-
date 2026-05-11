# DSA-Practice-
#Recursion 09 - 05 -2026
#Factorial of N
#Iterative Solution - O(n) Time and O(1) Space
import java.util.*;

public class Main {
    public static void main(String[] args) {
      int n = 5;
      int ans = 0;
      
      for(int i=0;i<=n;i++){
        if(i == 0){
          ans = 1;
        }
        else{
          ans = ans * i;
        }
      }
      System.out.println(ans);
    }
}



#Recursive Solution - O(n) Time and O(n) Space

import java.util.*;

public class Main {
    public static void main(String[] args) {
      int n = 5;
      int ans = fact(n);     
      System.out.println(ans);
    }
    static int fact(int n){
      if(n == 0){
        return 1;
      }
      return n * fact(n-1);
    }
}

#Recursion 10 - 05 -2026
#Sum of Natural Numbers (n=3)

import java.util.*;

public class Main {
    public static void main(String[] args) {
      int n = 3;
      int ans = sum(n);
      System.out.println(ans);
      
    }
    static int sum(int n){
      if(n == 1){
        return 1;
      }
      return n + sum(n-1);
    }
}

#fibanocci series 
general approach
import java.util.*;

public class Main {
    public static void main(String[] args) {
      int n = 3;
      int ans = fib(n);
      System.out.println(ans);
      
    }
    static int fib(int n){
      if(n <= 1){
        return 0;
      }
      else{
        return fib(n-1) + fib(n-2);
      }
    }
}

#basic recursion coding problems (hands-on)  11 may 2026
# Print Numbers from 1 to N

import java.util.*;

public class Main {
  
   static void printnum(int n){
      if(n == 0){
        return;
      }
      printnum(n - 1);
      System.out.print(n +" ");
   }
    public static void main(String[] args) {
      int n = 5;
      printnum(n);
      
      
    }
}
# Print Numbers from N to 1
import java.util.*;

public class Main {
  
   static void printnum(int n){
      if(n == 0){
        return;
      }
      System.out.print(n +" ");
      printnum(n - 1);
   }
    public static void main(String[] args) {
      int n = 5;
      printnum(n);
    }
}

/* <img width="1472" height="1640" alt="image" src="https://github.com/user-attachments/assets/c6475152-d930-477d-b6a1-de58a659760d" />

Great question! Let me break this down visually — the key to understanding this code is the **call stack** and what happens when the recursion "unwinds."

The code calls `printnum(5)`, which keeps calling itself with `n-1` until it hits 0 (the base case), then prints on the way back up. That's why it prints `1 2 3 4 5` — **not** `5 4 3 2 1`.Here's the full breakdown, step by step:

**Phase 1 — Going down (recursive calls)**

`main()` calls `printnum(5)`. Each call immediately hits the line `printnum(n-1)` — so it dives deeper before doing anything else. Nothing gets printed yet. The call stack builds up like this:

`printnum(5)` → `printnum(4)` → `printnum(3)` → `printnum(2)` → `printnum(1)` → `printnum(0)`

**Phase 2 — Base case triggers**

When `n == 0`, the `if` condition is true and the function just does `return` — no print, no more calls. The recursion stops here.

**Phase 3 — Coming back up (the unwind)**

This is the key insight. The `System.out.print(n)` line sits **after** the recursive call. So it was always waiting. Now, as each function finishes and returns control to the one that called it, the print finally runs:

- `printnum(0)` returns → `printnum(1)` resumes → prints `1`
- `printnum(1)` returns → `printnum(2)` resumes → prints `2`
- … and so on up to `printnum(5)` printing `5`

**The critical trick:** if you moved `System.out.print(n)` to be *before* `printnum(n-1)`, it would print `5 4 3 2 1` instead. The order of the print relative to the recursive call is everything. */




