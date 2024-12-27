# TicTactics

## Overview
This project is a web-based implementation of the classic Tic-Tac-Toe game. It allows users to play against another player or against a computer (single-player mode). The game keeps track of scores for both players and the number of draws.

## Features
- **Single Player Mode**: Play against the computer.
- **Multiplayer Mode**: Play against another player.
- **Scoreboard**: Tracks the number of wins for each player and the number of draws.
- **Reset Game**: Allows players to reset the game at any time.
- **Responsive Design**: The game is designed to work well on different screen sizes.

## Technologies Used
- HTML
- CSS
- JavaScript

## How to Play
1. **Select Mode**: Choose between Single Player and Multiplayer modes.
2. **Pick Character**: Select whether you want to play as 'X' or 'O'.
3. **Make Moves**: Click on the tiles to make your move. The game will automatically switch turns between players.
4. **Win or Draw**: The game will detect if a player has won or if the game ends in a draw. The scoreboard will be updated accordingly.
5. **Reset Game**: Click the "Reset Game" button to start a new game.

## Game Rules
- The game board consists of 9 tiles arranged in a 3x3 grid.
- Players take turns to place their mark ('X' or 'O') on an empty tile.
- The first player to get three of their marks in a row (horizontally, vertically, or diagonally) wins the game.
- If all tiles are filled and no player has three marks in a row, the game ends in a draw.

## Files
- `index.html`: The main HTML file that contains the structure of the game.
- `style.css`: The CSS file that styles the game.
- `app.js`: The JavaScript file that contains the game logic and functionality.

## Code Explanation
### HTML
The HTML file sets up the structure of the game, including the game board, mode selection, character selection, scoreboard, and reset button.

### CSS
The CSS file styles the game elements, including the game board, tiles, buttons, and scoreboard.

### JavaScript
The JavaScript file contains the game logic and functionality:
- **Initialization**: Sets up the initial state of the game.
- **Event Listeners**: Handles user interactions such as clicking on tiles, selecting mode, and picking characters.
- **Game Logic**: Manages the game state, checks for win conditions, and updates the scoreboard.
- **Reset Functionality**: Resets the game state and clears the board.

### Detailed Code Explanation
#### Initialization
The `initialize` function sets up the initial state of the game by resetting player and opponent tiles, available corners, and winning tile combinations. It also sets the `haveWon` flag to `false`.

#### Event Listeners
Event listeners are added to the player character buttons and game mode buttons to allow players to switch between 'X' and 'O' and toggle between single-player and multiplayer modes. These event listeners call the `initialize`, `clear`, and `startGame` functions to reset and start the game with the selected settings.

#### Game Logic
The `handleGame` function determines the current game mode and calls either `handleSingleGame` or `handleMultiplayerGame` based on the mode. These functions update the game board, check for winning conditions, and handle the opponent's response in single-player mode.

#### Reset Functionality
The `resetBtn` event listener calls the `initialize`, `clear`, and `startGame` functions to reset the game state and clear the board when the reset button is clicked.

## How to Run the Project
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/tic-tac-toe.git