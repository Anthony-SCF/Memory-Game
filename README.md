# JavaScript Memory Game — Bug Hunt

A debugging and code-correction project based on a JavaScript **Memory Card Matching Game**. Six bugs were identified, documented, and fixed — each tied to a specific JavaScript event concept from the course textbook. The corrected game is fully functional and playable in the browser.

---

## Features

- **4×4 card grid:** 16 cards (8 emoji pairs) shuffled randomly each game
- **Flip mechanics:** Cards reveal their emoji on click and flip back if unmatched
- **Match detection:** Matched pairs are locked in place with a distinct color
- **Score tracking:** Score increments with each successful match
- **Win condition:** Alerts the player and disables the board when all pairs are found
- **Event delegation:** A single container listener manages all card clicks efficiently

---

## Bug Fixes Summary

| # | Bug | Fix Applied |
|---|-----|-------------|
| 1 | `window.onload` overwritten by second assignment | Replaced with `addEventListener("load", ...)` |
| 2 | Multiple identical listeners added to each card | Replaced with single delegated listener on container |
| 3 | Container click fired on every click (event bubbling) | Added `event.target` check to filter non-card clicks |
| 4 | Flipped/matched cards could be re-clicked | Added `classList.contains()` guard conditions |
| 5 | No logic to handle non-matching card pairs | Added `else` block with `setTimeout` to flip cards back |
| 6 | Win-check function defined but never called | Added `checkWin()` call after each successful match |

---

## Project Structure

```
JS-Memory-Game-Bug-Hunt/
├── MemoryGame.html               # Fully debugged and playable memory game
├── North_Project2_BugHunt.pdf    # Written bug report with textbook references
└── README.md
```

---

## Technologies Used

- **HTML5** – Game container and card structure
- **CSS3** – Grid layout, card states (default, flipped, matched), visual styling
- **JavaScript (ES6)** – Event listeners, DOM manipulation, game logic, `setTimeout`

---

## Concepts Covered

- `addEventListener()` vs `window.onload` assignment
- Event delegation for efficient click handling
- Event bubbling and `event.target` filtering
- Conditional guards using `classList.contains()`
- `setTimeout()` for delayed DOM updates
- Function invocation and scope

---

## Textbook References

- Section 2-1c: Calling a Function (p. 41)
- Section 2-2a: Using Event Handlers (p. 42)
- Section 2-2c: Event Listeners (p. 43)
- Section 2-2e: Applying a Function to an Event (p. 44)
- Section 2-4b: Local and Global Scope (p. 50)
- Section 2-6d: Conditional Operators (p. 54)

---

## Author

**Anthony North**  
State College of Florida  
Course: Web Development / JavaScript  
Project: 2 — Bug Hunt
