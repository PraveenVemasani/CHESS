## Project Name
**CHESS Game**

## Description

This repository contains a chess game application written in Python. The program supports features like making valid moves, detecting check/checkmate/stalemate, and finding the best moves using algorithms such as MinMax and Alpha-Beta pruning. The repository is organized into three main Python scripts and an `images` folder for graphical assets.

---
![image](https://github.com/user-attachments/assets/88794c71-dbe0-49e3-b049-223bf6f81aa5)

## Folder Structure

```
/ChessProgram
├── images
│   ├── pieces
│   │   ├── wK.png   # White King
│   │   ├── wQ.png   # White Queen
│   │   ├── wR.png   # White Rook
│   │   ├── wB.png   # White Bishop
│   │   ├── wN.png   # White Knight
│   │   ├── wp.png   # White Pawn
│   │   ├── bK.png   # Black King
│   │   ├── bQ.png   # Black Queen
│   │   ├── bR.png   # Black Rook
│   │   ├── bB.png   # Black Bishop
│   │   ├── bN.png   # Black Knight
│   │   ├── bp.png   # Black Pawn
│   └── board.png     # (Optional) Chessboard background
├── ChessMain.py       # Main program for running the chess game
├── ChessEngine.py     # Handles game logic and rules
├── SmartMoveFinder.py # Algorithms for move calculation
└── ADDME.md           # Documentation file
```

---

## File Descriptions

### 1. `ChessMain.py`

This script serves as the entry point for the chess game. It handles the GUI using `pygame` and manages user interactions. Key features include:

- Rendering the chessboard and pieces.
- Detecting and responding to user input.
- Communicating with `ChessEngine.py` for move validation and game state updates.
- Optionally utilizing `SmartMoveFinder.py` for AI-driven moves.

### 2. `ChessEngine.py`

This script implements the core game logic and rules, including:

- Managing the chessboard state.
- Validating legal moves.
- Detecting check, checkmate, and stalemate.
- Undoing moves for backtracking.

### 3. `SmartMoveFinder.py`

This script contains algorithms for determining optimal moves:

- **Random Move Finder**: Picks a random valid move.
- **MinMax Algorithm**: Evaluates moves to a specified depth.
- **NegaMax Algorithm**: Simplifies MinMax by incorporating the turn multiplier.
- **NegaMax with Alpha-Beta Pruning**: Optimized NegaMax algorithm with pruning for improved efficiency.

---

## Installation

### Prerequisites

- Python 3.6 or higher
- `pygame` library

### Steps

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd ChessProgram
   ```
2. Install dependencies:
   ```bash
   pip install pygame
   ```
3. Run the program:
   ```bash
   python ChessMain.py
   ```

---

## Usage

### Playing the Game

- Start the program to launch the GUI.
- Click on pieces to select and move them.
- The game will enforce valid moves and display the current state.

### AI Functionality

- The AI can be activated to play against the user by uncommenting relevant lines in `ChessMain.py`.
- The strength of the AI depends on the selected algorithm and depth (adjustable in `SmartMoveFinder.py`).

---

## Images

### Chess Piece Images

Ensure the `images/pieces` folder contains the following files:

- `wK.png`, `wQ.png`, `wR.png`, `wB.png`, `wN.png`, `wp.png` (White pieces)
- `bK.png`, `bQ.png`, `bR.png`, `bB.png`, `bN.png`, `bp.png` (Black pieces)

### Optional Chessboard Image

Place a `board.png` in the `images` folder for a custom board design.

---

## Future Enhancements

- Add support for additional AI difficulty levels.
- Implement a timer for timed games.
- Support for saving and loading games.
- Enhance the GUI with animations and improved graphics.
