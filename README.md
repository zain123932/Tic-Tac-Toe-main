# Tic Tac Toe

A neon-styled, two-player Tic Tac Toe game built with plain HTML, CSS, and vanilla JavaScript. No frameworks, no dependencies: just open `index.html` and play.


**Live Demo:**

---

## Features

- **Two-player local game**: players take turns as **O** and **X** (O goes first)
- **Win detection** across all 8 winning lines (rows, columns, diagonals)
- **Draw detection** when the board fills with no winner
- **Winner / draw announcement** screen with a Restart button
- **Reset button** to start a fresh game at any time
- **Neon dark theme**: cyan glow for O, pink glow for X
- **Responsive layout** with dedicated styles for mobile and tablet screens
- Filled boxes are disabled, so a move can't be overwritten

---

## Tech Stack

| Technology | Purpose |
| --- | --- |
| HTML5 | Page structure and game board |
| CSS3 | Layout (Flexbox), theming with CSS variables, responsive media queries |
| JavaScript (ES6) | Game logic, turn handling, win/draw detection |

---

## Project Structure

```
tic-tac-toe/
├── index.html    # Page structure: board, reset button, result message
├── style.css     # Styling, theme colors, responsive rules
├── script.js     # Game logic
└── README.md
```

---

## Getting Started

### Run locally

1. Clone the repository:
   ```bash
   git clone https://github.com/zain123932/Tic-Tac-Toe-main.git
   ```
2. Open the project folder:
   ```bash
   cd Tic-Tac-Toe-main
   ```
3. Open `index.html` in any modern browser (or use the VS Code **Live Server** extension).

No installation or build step is required.

---

## How to Play

1. Player **O** starts. Click any empty box to place your mark.
2. Players alternate turns between **O** and **X**.
3. The first player to get **three marks in a row** (horizontal, vertical, or diagonal) wins.
4. If all nine boxes are filled with no winner, the game is a **draw**.
5. Press **Restart** on the result screen, or **Reset** at any time, to play again.

---

## How It Works

- The board is nine `<button class="box">` elements, read in order as indexes `0` to `8`.
- All eight winning combinations are stored in a `winningPattern` array of index triples.
- After every move, `checkWinner()` compares the three boxes in each pattern. If they match and are not empty, the winner is shown; otherwise, once nine moves are made, a draw is declared.
- `resetGame()` clears the board, re-enables all boxes, resets the turn to O and the move counter to 0, and hides the result message.
- Theme colors live in CSS variables (`:root`), so the look is easy to customize:

```css
:root {
  --bg-color: #0B132B;
  --board-bg: #1C2541;
  --x-color: #F72585;
  --o-color: #4CC9F0;
}
```

---

## Responsive Design

| Screen size | Behavior |
| --- | --- |
| Mobile (`≤ 450px`) | Smaller boxes and tighter spacing |
| Tablet (`700px – 1000px`) | Larger board and boxes |
| Desktop | Default layout |

---

## Future Improvements

- [ ] Single-player mode with a computer opponent
- [ ] Score tracking across rounds
- [ ] Highlight the winning line
- [ ] Display whose turn it is
- [ ] Sound effects and animations
- [ ] Choose which symbol starts

---

## Author

**Zain**
Software Engineering student, University of Poonch Rawalakot

- GitHub: [@zain123932](https://github.com/zain123932/)

---
