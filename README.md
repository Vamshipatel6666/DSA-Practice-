# DSA-Practice-
#Recursion 09 - 05 -2026
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
