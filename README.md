# Unblock_Me

## 1. Introduction

The **Unblock Me Game** is a puzzle-based grid game developed using the **Python programming language and the Tkinter GUI library**.
The objective of the game is to move different blocks inside a **6 × 6 grid** in such a way that the **red block reaches the exit path**. The player must slide the blocks without overlapping them and within the grid boundaries.

---

## 2. Technology Used

* **Python** – Main programming language used for implementing the logic of the game.
* **Tkinter** – Used to create the graphical user interface (GUI).
* **Canvas Widget** – Used to draw the grid and blocks on the screen.

---

## 3. Game Structure

The game consists of several components:

### 1. Start Page

When the program starts, a **welcome screen** appears with a **Classic Mode button**.
This screen allows the user to start the game.

### 2. Difficulty Selection

The player can choose the difficulty level:

* Beginner
* Medium
* Hard

Each difficulty level contains multiple puzzle levels.

### 3. Level Selection

After selecting difficulty, the player chooses a **specific level** to play.

### 4. Game Board

The game board is a **6 × 6 grid** created using the Tkinter Canvas.
Each cell has a fixed size (100 × 100 pixels).

Blocks are placed inside the grid with predefined positions.

---

## 4. Block Representation

Each block in the game is represented using a **Block class**.

The block stores:

* **Start position** (row, column)
* **End position** (row, column)
* **Orientation** (horizontal or vertical)

Blocks can move only in their allowed direction:

* Horizontal blocks → move **left or right**
* Vertical blocks → move **up or down**

The **red block** is the main block that must reach the exit.

---

## 5. Game Controls

The player interacts with the game using:

**Mouse Click**

* Select a block on the board.

**Keyboard Arrow Keys**

* Move the selected block.

  * Up Arrow
  * Down Arrow
  * Left Arrow
  * Right Arrow

The program checks whether the block can move before updating its position.

---

## 6. Collision and Boundary Checking

Before moving a block, the game verifies:

1. The block should **not go outside the grid**.
2. The block should **not overlap with another block**.

This is handled using functions such as:

* `can_move()`
* `is_overlapping()`

These functions ensure valid movement of blocks.

---

## 7. Winning Condition

The game is solved when the **red block reaches the exit position** on the right side of the grid.

Condition used in the code:

```
red_block.end[1] == 5
```

When the player solves the puzzle:

* A **"You Win!" message** is displayed.
* Options appear to **go to the next level or return to home**.

---

## 8. Level Generation

Different puzzles are created using predefined **block configurations**.
Each level specifies:

* Block name
* Starting position
* Ending position
* Orientation

These configurations are stored in the `generate_blocks()` function.

---

## 9. Conclusion

The **Unblock Me Game** demonstrates concepts such as:

* Object-Oriented Programming (OOP)
* GUI development using Tkinter
* Event handling
* Grid-based game logic

It provides an interactive puzzle experience where players must use **logical thinking and strategy** to solve each level.


