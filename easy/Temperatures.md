```
import java.util.*;
import java.io.*;
import java.math.*;

/**
 * Auto-generated code below aims at helping you parse
 * the standard input according to the problem statement.
 **/
class Solution {

    public static void main(String args[]) {
        Scanner in = new Scanner(System.in);
        int n = in.nextInt(); // the number of temperatures to analyse

        int min = 0;


        for (int i = 0; i < n; i++) {
            int t = in.nextInt(); // a temperature expressed as an integer ranging from -273 to 5526
            
            if(Math.abs(t) < Math.abs(min) || i == 0){
                min = t;
            }
            else if(Math.abs(t) == Math.abs(min) && t > min){
                min = t;
            }
            else if(Math.abs(t) == Math.abs(min) && t < min){
                min = Math.abs(t);
            }
        }

        // Write an answer using System.out.println()
        // To debug: System.err.println("Debug messages...");

        System.out.println(min);
    }
}
```