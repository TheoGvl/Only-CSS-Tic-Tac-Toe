# Pure CSS Tic-Tac-Toe

A fully functional, two-player game of Tic-Tac-Toe built completely without JavaScript. This project is a technical demonstration of advanced CSS State Management, DOM parsing, and sibling combinatorial logic.

## How It Works
Instead of using variables in JS to track board state, this project utilizes **18 hidden HTML checkboxes** (9 for Player X, and 9 for Player O). 

The CSS engine acts as the logical processor:
1. **Cell Locking:** When a user clicks the left or right side of a cell, a checkbox is `:checked`. CSS uses the `~` General Sibling selector to immediately `display: none;` the opponent's label for that specific cell, locking it in.
2. **Win Detection:** The stylesheet contains hardcoded algorithms for all 8 possible win states horizontal, vertical, diagonal. For example, if `#x1`, `#x2`, and `#x3` are all concurrently `:checked`, the CSS triggers `display: flex;` on the Victory Screen overlay, effectively ending the game.

## Technologies Used
* **HTML5:** Semantic architecture designed specifically for CSS traversal.
* **CSS3:** Advanced usage of `:checked`, `~`, `^=` attribute selectors, CSS Grid, and Keyframe Animations.
