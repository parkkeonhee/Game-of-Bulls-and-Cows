This project is from http://grid.cs.gsu.edu/~csc2010/f13/assignments/h8/

This Java program focuses on encapsulation of object-oriented programming.

These are the instructions to the Java assignment.

Write a Java program for the game of BULLS and COWS, called Bulls.java. The objective of this game is to make the user (player) guess a 4-digit number which is randomly generated in the program. The 4-digit number should not have repeating digits and will be in the range 1000 to 9999. The player will be given a maximum of 10 tries to guess. The player WINS if he/she guesses the number within 10 tries; otherwise the player LOSES the game. After each guess, the computer will provide to the player a sense of how close their guess was to the target number in terms of how many digits they guessed right and whether these were in the correct positions within the target, defined as follows:
Consider numbers in the range 1000 and 9999 which do not have repeating digits. Given two such numbers, we define the number of BULLS and COWS for the pair of numbers as follows:

BULLS = number of digits that appear in the same positions in the two numbers. 
COWS = number of digits that appear in both the numbers, but at different positions.

For example, if the two numbers were 2367 and 1327, we have 2 BULLS (for the exact matches for digits 3 and 7) and 1 COW (for the remaining common digit 2 which is in different positions in the two numbers). If the numbers were 9852 and 8926, we have 0 BULLS and 3 COWS and if the numbers were 1234 and 4321, we have 0 BULLS and 4 COWS. It is quite clear that if the two numbers are the same, we have 4 BULLS and 0 COWS.

The main program should first display a Welcome Message explaining the rules of the games. Then, it should generate a 4-digit random number between 1000 and 9999 with no repeating digits. After that, it should repeatedly ask the user for his/her guess and report the BULLS and COWS for the guess compared with the random number. The game stops when either the player has made a correct guess or when the player had made 10 guesses.

You should make use of the class methods to solve this problem. Class methods are helper methods to the main() method and are useful to break the solution into smaller parts. They are also useful to encapsulate code that repeats several places in the main method. In addition to the main() method, you will write the following class methods and make calls to them in appropriate places in the code.

// This method prints the welcome message
private static void printWelcomeMessage()

// This method produces a valid 4-digit number and returns it
// as a String object. The following statement can be used to
// generate a number between 1000 and 9999:
// num = 1000 + ( (int) (Math.random() * 10000) % 9000);
private static String produceRandomTarget()

// This method receives a 4-digit number, num, as a String parameter and
// returns true if num has repeating digits and false otherwise..
private static boolean hasRepeatingDigits(String num)

// This method received a String, num, as parameter and 
// returns true if num contains a non-digit and false otherwise.
private static boolean containsNonDigits(String num)

// This method receives two String parameters, num1 and num2, which
// contain the two 4-digit numbers and returns the number of "BULLS".
private static int computeBulls(String num1, String num2)

// This method receives two String parameters, num1 and num2, which
// contain the two 4-digit numbers and returns the number of "COWS".
private static int computeCows(String num1, String num2)

Two sample runs are shown below:


A winning sample run:

Welcome to the game of BULLS and COWS.
The objective in this game is for you to guess a 4-digit number
The computer responds with how close your guess is to the target
BULLS = # common digits with exact matches and
COWS  = # common digits in wrong position.

Enter guess number 1: aw
Your guess should contain 4 symbols (digits)
Enter guess number 1: 123
Your guess should contain 4 symbols (digits)
Enter guess number 1: 1a34
Your guess should not contain non-digits
Enter guess number 1: 1233
Your guess should not contain repeating digits
Enter guess number 1: 1234
Bulls = 0  Cows = 3
Enter guess number 2: 2413
Bulls = 3  Cows = 0
Enter guess number 3: 2418
Bulls = 3  Cows = 0
Enter guess number 4: 2419
Bulls = 4  Cows = 0
Congratulations; You Won!!

A non-winning sample run:
Welcome to the game of BULLS and COWS.
The objective in this game is for you to guess a 4-digit number
The computer responds with how close your guess is to the target
BULLS = # common digits with exact matches and
COWS  = # common digits in wrong position.

Enter guess number 1: qwer
Your guess should not contain non-digits
Enter guess number 1: 1234
Bulls = 0  Cows = 1
Enter guess number 2: 1235
Bulls = 0  Cows = 2
Enter guess number 3: 1236
Bulls = 0  Cows = 1
Enter guess number 4: 8723
Bulls = 0  Cows = 0
Enter guess number 5: 8078
Your guess should not contain repeating digits
Enter guess number 5: 8076
Bulls = 1  Cows = 0
Enter guess number 6: 2315
Bulls = 1  Cows = 1
Enter guess number 7: 8765
Bulls = 0  Cows = 1
Enter guess number 8: 7654
Bulls = 0  Cows = 1
Enter guess number 9: 6543
Bulls = 0  Cows = 1
Enter guess number 10: 9087
Bulls = 1  Cows = 1
Sorry; You ran out of guesses!!
The correct number was: 5019
