# the-gambling-game
import java.util.*;
public class MainApplication{
	public static void main(String[] args){
	Casino c=new Casino();
	c.OrganizeNewGame();
	}
}
class Casino{
	Player p1=new Player();
	Game g1=new Game();
	String userAnswer;
	Scanner sc=new Scanner(System.in);
	public void OrganizeNewGame(){
	System.out.println("Welcome to our Casino: Would you like to play?(y/n)");
	userAnswer= sc.nextLine();
	if(userAnswer.equals("y")){
	System.out.println("let's get started");
	g1.PlayGame();
	}
	else{
	System.out.println("Goodbye");
	}
	}
}
class Game{
	Random rand=new Random();
	private int ComputerGuess=-1;
	public void PlayGame(){
	System.out.println("Guess a number from 1 to 100");
	System.out.println("And I will guess a game");
	System.out.println("If your guess is within 20 of my guess: then you will win. Else I will win");
	ComputerGuess=ComputerGuess();
	System.out.println("Computer Guess is" + ComputerGuess);

	}
	public int ComputerGuess(){
	int programGuess=rand.nextInt(100);
	return programGuess;
	}

}
class Player{
	Scanner sc=new Scanner(System.in);
	private int userGuess;
	public int guessNumber(){
	System.out.println("enter your guess number from 1 to 100");
	userGuess=sc.nextInt();
	return userGuess;
	}
}
