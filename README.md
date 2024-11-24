
---

# Tic-Tac-Toe: Player vs Computer with Minimax and Alpha-Beta Pruning

## Overview
This is a Python implementation of the classic Tic-Tac-Toe game, where a player competes against a computer opponent. The computer uses the Minimax algorithm with Alpha-Beta pruning to determine the optimal moves. The player can choose whether they want to play first or second.

## Features
- **Two-player game**: Play against the computer in a 3x3 grid board.
- **Minimax Algorithm**: The computer uses this algorithm to simulate all possible moves and choose the best one.
- **Alpha-Beta Pruning**: Optimizes the Minimax algorithm by pruning branches in the game tree that do not need to be evaluated, improving performance.
- **Dynamic Gameplay**: The player can choose whether they want to go first or second.

## How the Game Works
- The game is played on a 3x3 grid.
- Players take turns to place their respective symbols (`X` for the player and `O` for the computer).
- The goal is to get three of your symbols in a row, either horizontally, vertically, or diagonally.
- If the board is full and no player has won, the game ends in a draw.

## Minimax Algorithm with Alpha-Beta Pruning
The **Minimax Algorithm** is a decision rule for minimizing the possible loss for a worst-case scenario. When dealing with gains, it is referred to as "maximizing". The **Alpha-Beta Pruning** optimizes the Minimax algorithm by cutting off branches that cannot affect the final decision, improving its performance.

### Minimax Steps:
1. **Define the game state**: This consists of the current configuration of the board.
2. **Evaluate the game state**: Assign scores based on the result:
   - +10 if the computer wins.
   - -10 if the player wins.
   - 0 if it’s a draw.
3. **Generate all possible moves**: Simulate each possible move for the player and the computer.
4. **Evaluate each move**: Recursively evaluate each move, simulating future moves.
5. **Choose the best move**: Select the move that maximizes the computer's score or minimizes the player’s score.
6. **Make the move**: Apply the chosen move to the game board.
7. **Repeat**: Continue until the game ends.

### Alpha-Beta Pruning:
- Alpha represents the best value that the maximizer can guarantee so far.
- Beta represents the best value that the minimizer can guarantee so far.
- If at any point the algorithm detects that a branch cannot improve the current best value, it prunes that branch and moves to the next one.

## Installation

This game only requires Python 3 to run. There are no additional libraries or dependencies required.

1. Clone or download the repository to your local machine.
2. Navigate to the folder containing the script in the terminal.
3. Run the script with Python:
   ```bash
   python tic_tac_toe.py
   ```

## Game Instructions

1. The player will be prompted to choose whether they want to play first (enter 1) or second (enter 2).
2. The game board will display after each move, and the player will be asked to enter a number between 1 and 9 corresponding to the grid's positions.
3. The computer will make its move automatically using the Minimax algorithm with Alpha-Beta pruning.
4. The game continues until there’s a winner or a draw.

### Example Board Layout

```
| X | O | X |
---------------
| O | X | O |
---------------
| O | X |   |
===============
```

## Code Structure

The main functions and their roles are as follows:

- **Gameboard(board)**: Displays the current state of the board.
- **Clearboard(board)**: Resets the board to its initial empty state.
- **winningPlayer(board, player)**: Checks if a given player has won.
- **gameWon(board)**: Returns whether the game is over (a player has won).
- **printResult(board)**: Displays the result of the game (win or draw).
- **blanks(board)**: Returns a list of all empty spaces on the board.
- **boardFull(board)**: Checks if the board is full.
- **setMove(board, x, y, player)**: Places the player's move on the board.
- **playerMove(board)**: Allows the human player to make a move.
- **getScore(board)**: Evaluates the board and returns a score (+10, -10, or 0).
- **abminimax(board, depth, alpha, beta, player)**: The Minimax algorithm with Alpha-Beta pruning to evaluate the best move.
- **o_moves(board)**: Computer's move when it plays as 'O'.
- **x_moves(board)**: Computer's move when it plays as 'X'.
- **makeMove(board, player, mode)**: Executes the move for either the player or the computer.
- **PlayervsComputer()**: Runs the game between the player and the computer.

## Example Gameplay
```
========================================================================================
TIC-TAC-TOE using MINIMAX with ALPHA-BETA Pruning
========================================================================================
Enter to play 1st or 2nd: 1
|   |   |   |
---------------
|   |   |   |
---------------
|   |   |   |
===============
Enter a number between 1-9: 1
| X |   |   |
---------------
|   |   |   |
---------------
|   |   |   |
===============
Computer's turn...
| X | O |   |
---------------
|   |   |   |
---------------
|   |   |   |
===============
...
```

## License

This project is open-source and available for modification and distribution under the MIT License.

---
