# Manmohit

   
package Card;

import java.util.Random;
import java.util.Scanner;

/**
 * This class models a simple card guessing game
 * 
 * 
 */
public class cardgame {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
           Scanner input = new Scanner(System.in);

        // Create an array to hold 7 cards
           int[] hand = new int[7];

        // We'll use Random to generate random numbers
        Random random = new Random();

        for( int i=0; i<hand.length;i++)
		{
			hand[i]=(int)(Math.random()*13);
		}

        // print them out for debugging purposes
        System.out.println("Here are the cards in the hand");
        for(int data: hand)
		{
			System.out.println(data);
		}

        // Now ask the user for a card
        
        System.out.println("Pick a suit for your card");
       
        int suit = input.nextInt();

        System.out.println("Enter a value (1 to 13)");
        int value = input.nextInt();

//        Card userGuess = new Card(value, Card.SUITS[suit - 1]);

        boolean match = false;
       for (int card : hand) {
            if (card == suit);
                {
                match = true;
               break;
            }
        }
    
        String response = match ? "Right guess": "No match";
        
        System.out.println(response);
        
    }
    
}
