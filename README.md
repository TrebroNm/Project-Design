# Project-Design
package UserInterface;

import java.util.Scanner;

public class TUI{
	
	private static Scanner scan;
	
	public static void main(String[] args) {
		new TUI();
		}
	
	public TUI(){
		scan = new Scanner(System.in);
		start();
	}
	
	public void start() {
		System.out.println("Welcome!");
		System.out.println("(1) Borrower menu \n (2) LP Menu \n (3) Loan Menu \n (0) Quit");
		boolean finished = false;
		while(!finished) {
			String command = print();
			finished = processCommand(command);
		}
	}
	
	public String print() {
		String inputLine;
		System.out.println(">");
		inputLine = scan.nextLine();
		return inputLine;
		
	}
	
	public boolean processCommand(String command) {
		boolean wantsToQuit = false;
		switch(command) {
		case "1":
			System.out.println("Borrower menu");
			break;
		case "2":
			System.out.println("LP Menu");
			break;
		case "3":
			System.out.println("Loan Menu");
			break;
		case "0":
			System.out.println("Quit");
			wantsToQuit = true;
			break;
		default:
			System.out.println("Invalid command");
			break;	
		}
		return wantsToQuit;
	}	
}

