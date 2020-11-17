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
        int N = in.nextInt();


        ArrayList<Integer> power = new ArrayList();
        
        for (int i = 0; i < N; i++) {
            int pi = in.nextInt();
            power.add(pi);
        }
        Collections.sort(power);
        
        // Write an answer using System.out.println()
        // To debug: System.err.println("Debug messages...");

         int MenorDiferenca = 999999999;

        for(int i = 0; i < power.size()-1; i++){                     
        // Compare strenght pairs in sorted array

        int diferencaAtual = Math.abs(power.get(i)-power.get(i+1));        
        
        if(diferencaAtual < MenorDiferenca)
        {
            // Set the new smalles strenght differene
            MenorDiferenca = diferencaAtual;
        }            
    }
        System.out.println(MenorDiferenca);
    }
}
```