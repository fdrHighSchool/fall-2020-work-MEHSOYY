# Random Number Guessing Game

import java.util.Scanner;
import java.util.Random;

public class Main {

	public static void main(String[] args) {

		Scanner scan = new Scanner(System.in);
		Random rand = new Random();

    Scanner input = new Scanner(System.in);

    System.out.print("Whats your name?");
    String name = input.next();

		System.out.println("Guess a number between 1 and 100," + name + ".");

		int num = rand.nextInt(100)+1;
		int guess = 0;
		int guesses = 0;

		while(guess != num) {

			guess = scan.nextInt();
			guesses++;

			if(guess < num) {
				System.out.println("Go Higher!");
			} else if (guess > num) {
				System.out.println("Go Lower!");
			}
		}

		System.out.println("Congratulations! You have guessed the number in " + guesses + " guesses!");
	}
}
