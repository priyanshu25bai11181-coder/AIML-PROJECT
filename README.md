# Tic‑Tac‑Toe with AI

A command‑line Tic‑Tac‑Toe game where you play against an unbeatable AI opponent.  
The AI uses the **Minimax algorithm with Alpha‑Beta pruning** to guarantee optimal moves, making it fast and impossible to defeat.

## Features

- Clean console interface with a numbered board (1–9) for easy move entry.
- Human plays as **X** (first), AI plays as **O**.
- AI never loses – your best outcome is a draw.
- Fast move calculation thanks to alpha‑beta pruning (no noticeable delay).

## How to Run

1. Make sure you have **Python 3** installed.
2. Download or copy `tictactoe.py`.
3. Run the script:

   ```bash
   python tictactoe.py
Follow the on‑screen prompts. Enter a number (1–9) corresponding to the cell you want to mark.

Dependencies
None – uses only the Python standard library.

Algorithm
The AI decides its move by exploring the game tree with Minimax. Alpha‑beta pruning eliminates branches that cannot influence the final decision, dramatically speeding up the search. The evaluation function gives:

+1 if the AI (O) wins,

-1 if the human (X) wins,

0 for a draw.

Because the board is small (3×3), the AI always makes a perfect move in a fraction of a second.

Example
text
  1 | 2 | 3
 -----------
  4 | 5 | 6
 -----------
  7 | 8 | 9

Your turn (X). Enter a number (1-9): 5

  1 | 2 | 3
 -----------
  4 | X | 6
 -----------
  7 | 8 | 9

AI (O) chooses 1 ...
...
License
Feel free to use and modify this code for learning purposes.

text

---

## 2. problem_statement.md

```markdown
# Problem Statement: AI for Tic‑Tac‑Toe

## Goal

Implement an **unbeatable Tic‑Tac‑Toe AI** that plays optimally against a human player.  
The AI must decide its moves quickly and guarantee at least a draw.

## Constraints

- Board: 3×3 grid.
- Human: plays first as **X**.
- AI: plays as **O**.
- The AI must be fast enough to respond instantly (no noticeable delay).

## Approach

The solution uses the **Minimax algorithm** with **Alpha‑Beta pruning**:

- **Minimax** recursively evaluates all possible moves, assuming both players play optimally.  
  The AI (maximizer) aims for +1 (win), the human (minimizer) aims for –1 (win).  
  A draw yields 0.

- **Alpha‑Beta pruning** cuts off branches that are already worse than the best found so far, reducing the number of nodes explored.

Because the game tree is small (9! possible sequences), the AI can evaluate all possibilities even without pruning, but alpha‑beta makes the code extensible and demonstrates efficient decision‑making.

## Implementation Details

- The board is represented as a list of 9 strings (`" "`, `"X"`, `"O"`).
- The `minimax` function returns a score for a given board state.
- The AI picks the move with the highest score.
- Input validation ensures the human selects only empty cells.

## Outcome

The AI is unbeatable – a human player can either lose or draw, depending on their moves.  
The game runs in a terminal, providing a simple and interactive experience.
