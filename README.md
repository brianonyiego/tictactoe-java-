# Tic-Tac-Toe Game (Java GUI)

## Overview
This is a simple Tic-Tac-Toe game built using Java Swing for GUI components. The game allows two players ('X' and 'O') to take turns playing on a 3x3 grid. The first player to align three symbols in a row, column, or diagonal wins the game. If all grid spaces are filled without any player winning, the game ends in a draw.

## Features
- GUI built using Java's Swing library.
- Two-player mode with alternating turns.
- Displays current player's turn.
- Automatically detects win conditions or draws.
- Game status displayed at the top of the window.

## Getting Started
1. Install the **Eclipse IDE** or any Java IDE of your choice.
2. Create a new Java project and package named `tictactoe`.
3. Create a new class file `tictac.java` and paste the code.
4. Run the program to start the Tic-Tac-Toe game.

## Prerequisites
- Java 8 or above installed.
- Eclipse IDE (or any preferred Java IDE).

## How the Game Works
1. A 3x3 grid is displayed on the screen using buttons.
2. A text label at the top displays which player's turn it is.
3. Players click on the buttons to place their symbol ('X' or 'O') on the grid.
4. The game automatically checks for winning conditions (three identical symbols in a row, column, or diagonal).
5. If a player wins, the game disables the grid and displays the winner.
6. If the grid is filled without a winner, the game ends in a draw.

## Code Structure
- **tictac.java**: Main class containing the GUI setup, game logic, and event handling.
  - **JPanel, JButton, JLabel**: Components used for building the user interface.
  - **actionPerformed()**: Method to handle user input (button clicks) and update the game state.
  - **check()**: Function to verify if a player has won after each move.
  - **firstTurn()**: Randomly selects the first player.
  - **xWins(), oWins()**: Methods to handle game-over scenarios when a player wins.

## Running the Game
- Simply run the `tictac` class in your IDE. The Tic-Tac-Toe window will appear, and you can begin playing by clicking the buttons.

## Future Improvements
- Add support for AI to play against the computer.
- Include reset functionality to start a new game without restarting the program.
- Track player scores over multiple rounds.

## License
This project is for educational purposes only.
