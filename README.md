# TicTactics

## Video Demo: 

## Description:
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

## Code Explanation

### JavaScript

The JavaScript file (`app.js`) contains the logic and functionality of the Tic-Tac-Toe game. Below is a detailed explanation of each section of the code:

---

### 1. **Initializations**
The code starts by initializing essential variables, DOM elements, and game state:
- **Tiles and Scores**: References the board tiles and scoreboard elements.
- **Player and Opponent**: Tracks the current player's and opponent's characters ('X' and 'O').
- **Game State Variables**: Includes `tileNum`, `corners`, `winningTiles`, and others to keep track of available tiles, winning combinations, and whether someone has won.

---

### 2. **Game Initialization**
The `initialize` function resets the game variables:
- **Player Moves**: Clears the moves of both players.
- **Winning Tiles**: Prepares an array of possible winning combinations.
- **Flags**: Sets the `haveWon` flag to `false`.

---

### 3. **Start Game**
The `startGame` function:
1. Calls `initialize` to reset the game state.
2. Updates the scoreboard with `updateScoreboard`.
3. Generates the first random move if in single-player mode.
4. Adds click event listeners to each tile to handle the game logic.

---

### 4. **Handle Game Logic**
The `handleGame` function determines the current game mode (single or multiplayer) and processes the player's move:
- **Single Player Mode**: The bot (opponent) responds after the player makes a move.
- **Multiplayer Mode**: Alternates turns between two players.

---

### 5. **Single Player Logic**
The `handleSingleGame` function handles:
1. **Player Moves**: Updates the board with the player's move.
2. **Opponent Response**: Calls `opponentResponse` to calculate the bot's next move using strategies such as blocking the player or taking corners.

---

### 6. **Multiplayer Logic**
The `handleMultiplayerGame` function alternates between the two players based on the turn count:
1. Updates the board with the current player's or opponent's move.
2. Checks for win conditions or draws.
3. Highlights the winning tiles and updates the scoreboard if someone wins.

---

### 7. **Opponent Strategies**
The `stratPlay` function implements the bot's playing strategies in single-player mode:
- **Attack**: Wins if it detects two tiles in a row and one empty tile.
- **Defend**: Blocks the player if they are about to win.
- **Random Moves**: Plays a random move when no immediate strategy is applicable.

---

### 8. **Tile Management**
Helper functions:
- `getTileNum`: Converts a tile's class name to its numerical equivalent.
- `remove` and `removeCorner`: Updates the list of available tiles after a move.

---

### 9. **Reset and Restart**
The `startOver` and `resetBtn` event listeners reset the game state:
- Clears the board.
- Resets game variables.
- Starts a new game.

---

### 10. **Character Selection and Game Mode**
The code includes event listeners for buttons:
- **Character Selection**: Allows the player to choose 'X' or 'O'.
- **Mode Selection**: Switches between single-player and multiplayer modes.

---

### 11. **Visual Effects**
The code applies animations to highlight winning tiles using CSS styles when a player wins.

---

### Summary of Functions
| **Function**           | **Purpose**                                                                 |
|-------------------------|-----------------------------------------------------------------------------|
| `initialize`           | Resets the game state and variables.                                        |
| `startGame`            | Initializes the game and adds event listeners to tiles.                    |
| `handleGame`           | Processes player moves based on the selected game mode.                    |
| `handleSingleGame`     | Handles player moves and calls opponent's response in single-player mode.  |
| `handleMultiplayerGame`| Alternates turns between two players and checks for win conditions.        |
| `stratPlay`            | Implements the opponent's strategies for attacking and defending.          |
| `clear`                | Clears the board and resets game-related messages.                        |
