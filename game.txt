import java.util.*;
import java.util.Scanner;

public class Game1 {
    public static void main(String[] args) {
        int attempt=3,i=0,j=0,s=0,rounds=3;//number of attempts is 3
        System.out.println("This is the game where computer generates the value you have to guess the generated value\n ");
               
       int answer,guess;
       final int Max=100;
       Scanner keyboard=new Scanner(System.in);
       Random r=new Random();
       answer=r.nextInt(Max) + 1;  // generates the random number between 1 to 100
       while(i!=attempt)
         {
       System.out.println("Enter your number between 1 to 100");
       guess=keyboard.nextInt();
       if(answer==guess)
       { 
           s=s+1;
       }
       if(answer>guess) 
       {
           System.out.println("your guessed value is lesser than the generated value\n");
       }
       if(answer<guess)
       {
           System.out.println("your guessed value is greater than the generated value\n");
       }
       i++;
       j++;
       if(j==3)
       {
           System.out.println("sorry your attempt is completed\n");
           System.out.println("the random number is:\n"+ answer);
           System.out.println("your final score is\n"+s);
       }
        }
         
    }
    
}