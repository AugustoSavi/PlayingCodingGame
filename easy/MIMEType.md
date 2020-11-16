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
        int N = in.nextInt(); // Number of elements which make up the association table.
        int Q = in.nextInt(); // Number Q of file names to be analyzed.

        Map<String,String> example = new HashMap<String,String>();

        for (int i = 0; i < N; i++) {
            String EXT = in.next(); // file extension
            String MT = in.next(); // MIME type.

            example.put(EXT.toLowerCase(), MT);
        }

        in.nextLine();

        for (int i = 0; i < Q; i++) {
            String FNAME = in.nextLine(); // One file name per line.
            
            int ponto = FNAME.lastIndexOf(".");

            String result = example.get(FNAME.substring(ponto + 1,FNAME.length()).toLowerCase());
            if(result == null|| ponto == -1){
                System.out.println("UNKNOWN");
            }
            else{
                System.out.println(result);
            }
        
        }
        //System.err.println("Debug messages...");


        // For each of the Q filenames, display on a line the corresponding MIME type. If there is no corresponding type, then display UNKNOWN.
        
    }
}
```