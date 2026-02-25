1️⃣ import java.util.Scanner;

Imports the Scanner class to take user input.

2️⃣ public class TicTacToe {

Defines the class named TicTacToe.

3️⃣ static char[][] board = {...};

Creates a 3×3 character array to represent the game board.

4️⃣ static char currentPlayer = 'X';

Stores the current player symbol. Game starts with player X.

5️⃣ public static void main(String[] args)

Main method – execution starts from here.

6️⃣ Scanner sc = new Scanner(System.in);

Creates Scanner object to read input from keyboard.

7️⃣ boolean gameOver = false;

Boolean variable to control game loop.

8️⃣ while (!gameOver)

Loop runs until the game is over.

9️⃣ printBoard();

Displays the current board.

🔟 System.out.println("Player " + currentPlayer + ...)

Asks current player to enter row and column.

1️⃣1️⃣ int row = sc.nextInt();

Reads row number from user.

1️⃣2️⃣ int col = sc.nextInt();

Reads column number from user.

1️⃣3️⃣ if (board[row][col] == ' ')

Checks if selected cell is empty.

1️⃣4️⃣ board[row][col] = currentPlayer;

Places current player's symbol on board.

1️⃣5️⃣ if (checkWin())

Checks if current player has won.

1️⃣6️⃣ printBoard();

Prints final board after win.

1️⃣7️⃣ System.out.println("Player " + currentPlayer + " wins!");

Displays winning message.

1️⃣8️⃣ gameOver = true;

Stops the game loop.

1️⃣9️⃣ else if (isBoardFull())

Checks if board is full (draw condition).

2️⃣0️⃣ System.out.println("It's a draw!");

Displays draw message.

2️⃣1️⃣ currentPlayer = (currentPlayer == 'X') ? 'O' : 'X';

Switches player using ternary operator.

2️⃣2️⃣ else { System.out.println("Cell already taken!"); }

If cell is not empty, shows error message.

2️⃣3️⃣ sc.close();

Closes Scanner object.

🔹 printBoard() Method
Prints horizontal line.
Uses nested loops:

Outer loop → rows

Inner loop → columns

Prints board elements in grid format.
🔹 checkWin() Method
Checks:

✔ All rows
✔ All columns
✔ Main diagonal
✔ Other diagonal

Returns true if player wins.

🔹 isBoardFull() Method
Checks all cells:

If any empty → return false

If no empty → return true
