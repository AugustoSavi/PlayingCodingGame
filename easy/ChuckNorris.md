Esse eu demorei para entender o desafio e acabei procurando pelos forum algo que me ajudasse, acabei encontrando a resposta
mas para não só ganhar os ponto. 

Quis entender o codigo e comentei o mesmo para gerar conhecimento

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

        //Transformou  a mensagem em um array de char
        char[] MESSAGE = in.nextLine().toCharArray();

        // Write an answer using System.out.println()
        // To debug: System.err.println("Debug messages...");

        //classe do java.lang, todos os dados inseridos são considerados objetos
        StringBuilder binary = new StringBuilder();

		for(char c : MESSAGE) {
			String res = Integer.toBinaryString(c);
			
			//for non-letters
			while(res.length() < 7) res = '0' + res;
			
			binary.append(res);
		}
		
		//convert to unary and print to console
		int i = 0;
		char currentChar;
		while(i < binary.length()) {
			if(binary.charAt(i) == '0') {
				System.out.print("00 ");
				currentChar = '0';
			}
			else {
				System.out.print("0 ");
				currentChar = '1';
			}
            
			while(binary.charAt(i) == currentChar) {
				System.out.print("0");
				i++;
				if(i >= binary.length()) break;
			}
			if(i < binary.length()) System.out.print(" ");
    }
    }
}
```