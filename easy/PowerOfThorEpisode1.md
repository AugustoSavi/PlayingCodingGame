```
import java.util.*;
import java.io.*;
import java.math.*;

/**
 * Auto-generated code below aims at helping you parse
 * the standard input according to the problem statement.
 * ---
 * Hint: You can use the debug stream to print initialTX and initialTY, if Thor seems not follow your orders.
 **/
class Player {

    public static void main(String args[]) {
        Scanner in = new Scanner(System.in);
        int lightX = in.nextInt(); // the X position of the light of power
        int lightY = in.nextInt(); // the Y position of the light of power
        int initialTx = in.nextInt(); // Thor's starting X position
        int initialTy = in.nextInt(); // Thor's starting Y position

        int thorX = initialTx;
        int thorY = initialTy;

        // game loop
        while (true) {
            int remainingTurns = in.nextInt(); // The remaining amount of turns Thor can move. Do not remove this line.

            //Define as variaveis inicias 
            String directionX="";
            String directionY="";

            //Se a posição do X de thor for mais que a da luz movese para W
            if (thorX > lightX) {
                directionX="W";
                thorX = thorX - 1;
            } else if (thorX < lightX) {
                directionX = "E";
                thorX = thorX + 1;
            }
            
            if (thorY > lightY) {
                directionY = "N";
                thorY = thorY - 1;
            } else if (thorY < lightY) {
                directionY = "S";
                thorY = thorY + 1;
            }

            // A single line providing the move to be made: N NE E SE S SW W or NW
            System.out.println(directionY + directionX);
        }
    }
}
```