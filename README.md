# Java-Project
import java.util.Scanner;

public class guessingGame
{
    public static void main(String args[])
    {
        try{
            Scanner sc = new Scanner(System.in);
            System.out.println("---Welcome to the Guessing Game---");
            System.out.println("Guess the number between 1 to 50");
            System.out.println("Instructions--");
            System.out.println("Your are provided with 5 trials and you have to guess the number.");
            System.out.println("If guessed correctly you WIN else you LOSE the game. GOOD LUCK");
            System.out.println("===========================================================");
            System.out.println("Let's start the game: ");

            int number = 1 + (int)(50*Math.random());

            int trials = 5;
            
            
                for(int i=1 ; i<=trials ; i++)
                {
                    System.out.print("Enter Number: ");
                    if(sc.hasNextInt())
                    {
                        System.out.print("Enter Number: ");
                        int guess = sc.nextInt();
                            
                        if(guess > 0 && guess <=50)
                        {
                            if(guess == number)
                            {
                                System.out.println("You guessed it!!");
                                System.out.println("Congratulations, You WON!!");
                                break;
                            }
                            else if(guess > number)
                            {
                                System.out.println("Guessed no. is greater than the ans.");
                                System.out.println("Try Again!");
                            }
                            else if(guess < number)
                            {
                                System.out.println("Guessed no. is less than the ans.");
                                System.out.println("Try Again!"); 
                            }
                        }
                        else
                        {
                            System.out.println("Write a valid number between 1-50");
                            
                        }
                        System.out.println("Trials left: " + (5-i));
                    }
                    else
                    {
                        System.out.println("Invalid format..not a number..Try again.");
                        break;
                    }
                    if((5-i) == 0)
                    {
                        System.out.println("Oops! Trials Over. Better LUCK next time...");
                    }
                    else
                    {
                        continue;
                    }
                }
        }
    
      catch(Exception e)
      {
          System.out.println(e);
      }  
            
    }
}
