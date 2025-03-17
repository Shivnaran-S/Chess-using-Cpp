# Chess Game Implementation in C++

## Overview

This project is a comprehensive implementation of a Chess game in C++. It includes all the standard rules of Chess, such as piece movements, check, checkmate, and pawn promotion. The game is designed to be played between two players, with one controlling the White pieces and the other controlling the Black pieces. The implementation is modular, with separate header files for different functionalities, making the codebase clean, maintainable, and easy to understand.

## Features

1. **Piece Movement**: 
   - All standard Chess pieces (Pawn, Rook, Knight, Bishop, Queen, King) are implemented with their correct movement rules.
   - Special moves like pawn promotion and en passant are supported.

2. **Check and Checkmate**:
   - The game detects when a king is in check and highlights the possible moves to get out of check.
   - Checkmate is detected, and the game ends when a player's king is checkmated.

3. **Dynamic Move Generation**:
   - The possible moves for each piece are dynamically generated based on the current state of the board.
   - The game ensures that moves do not leave the king in a vulnerable position.

4. **User Interaction**:
   - The game is played via the console, with players entering their moves in a user-friendly format.
   - The board is displayed after each move, showing the current state of the game.

5. **Modular Codebase**:
   - The code is divided into multiple header files, each handling a specific aspect of the game (e.g., `check.h`, `checkmate.h`, `possible_moves.h`, etc.).
   - This modular approach makes the code easy to extend and maintain.

## Code Structure

### Main File: `Chess1.cpp`
- **Initialization**: The chessboard is initialized with all pieces in their standard positions.
- **Game Loop**: The game runs in a loop, alternating between players until a checkmate or stalemate occurs.
- **Move Validation**: Each move is validated to ensure it is legal and does not leave the king in check.
- **Display**: The current state of the board is displayed after each move.

### Header Files

1. **`check.h`**:
   - Contains the logic to check if the king is under attack by any opponent piece.
   - Returns the number of attackers on the king and their positions.

2. **`checkmate.h`**:
   - Determines if the current player is in checkmate.
   - Updates a 2D array with possible moves to stop the check on the king.

3. **`future_check.h`**:
   - Ensures that a move does not leave the king in a vulnerable position.
   - Removes invalid moves from the list of possible moves.

4. **`king_move_check.h`**:
   - Checks if a specific move is safe for the king.
   - Returns the number of opponents targeting the king's new position.

5. **`possible_moves.h`**:
   - Generates all possible moves for a given piece based on the current board state.
   - Excludes moves that would capture the opponent's king.

6. **`possible_moves_k.h`**:
   - Similar to `possible_moves.h`, but includes moves that could capture the opponent's king.
   - Used for checking if the king is under attack.

## How to Run the Game

1. **Compilation**:
   - Ensure you have a C++ compiler installed (e.g., `g++`).
   - Compile the `Chess1.cpp` file along with the necessary header files:
     ```bash
     g++ Chess1.cpp -o chess
     ```

2. **Execution**:
   - Run the compiled executable:
     ```bash
     ./chess
     ```

3. **Gameplay**:
   - Follow the on-screen instructions to enter moves.
   - The game will prompt you to enter the piece you wish to move and the target position.
   - The board will be displayed after each move, showing the current state of the game.

## Key Highlights

- **Efficient Move Generation**: The game dynamically generates possible moves for each piece, ensuring that all rules of Chess are followed.
- **Checkmate Detection**: The game accurately detects checkmate, ensuring a smooth and rule-compliant gameplay experience.
- **Modular Design**: The code is divided into multiple header files, each handling a specific aspect of the game, making it easy to extend and maintain.
- **User-Friendly Interface**: The game is played via the console, with clear instructions and a well-formatted board display.

## Future Enhancements

- **GUI Implementation**: A graphical user interface (GUI) could be added to make the game more visually appealing.
- **AI Opponent**: An AI opponent could be implemented to allow single-player gameplay.
- **Multiplayer Support**: Online multiplayer support could be added to allow players to compete over the internet.

## Conclusion

This Chess implementation is a robust and well-structured project that demonstrates a deep understanding of both the game of Chess and C++ programming. The modular design, efficient move generation, and accurate checkmate detection make this project a standout example of object-oriented programming and game development. It is a testament to the developer's ability to create complex, rule-based systems with clean and maintainable code.
