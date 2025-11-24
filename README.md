# 🍎 Reversed Snake: You Are The Apple

> **Survival Horror in 8-bit.** The classic Nokia hit, inverted. You control the food, and the Snake is an AI determined to eat you.

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Language](https://img.shields.io/badge/language-JavaScript-yellow.svg)
![Size](https://img.shields.io/badge/size-2KB-green.svg)

## 🎮 Overview

**Reversed Snake** is a lightweight, single-file browser game built with **Vanilla JavaScript** and **HTML5 Canvas**. 

Instead of guiding the snake, you play as the **Apple**. The Snake is controlled by a pathfinding algorithm (A*) that ruthlessly hunts you down. As time passes, the snake grows longer, making the grid increasingly claustrophobic.

## ✨ Features

* **Inverted Gameplay Loop:** Break the habit of 30 years of gaming—run *away* from the snake!
* **AI Pathfinding:** The snake uses a custom implementation of the **A* (A-Star) Algorithm** to find the shortest path to the player.
* **Dynamic Difficulty:** The snake automatically grows every 5 seconds, reducing your safe space.
* **Visual Effects:** Includes a dynamic "panic" glitch effect when the snake gets too close (Manhattan distance ≤ 1).
* **Zero Dependencies:** Written in pure JS. No libraries, no frameworks, just one `.html` file.

## 🕹️ How to Play

1.  **Download** the `index.html` file (or clone this repo).
2.  **Open** the file in any modern web browser.
3.  **Controls:** Use your **Arrow Keys** (⬆️ ⬇️ ⬅️ ➡️) to move the Red Apple.
4.  **Objective:** Survive as long as possible. Do not let the Snake head touch you.

**Strategy Tip:** You are slightly faster than the snake (100ms move speed vs 140ms). Use your speed to bait the snake into knots, but don't get cornered!

## 🧠 Technical Details

For developers interested in the code, the logic is contained within a standard HTML structure.

### The AI (A* Search)
The snake doesn't move randomly. It utilizes a `PriorityQueue` to calculate the most efficient path to the player's coordinates:

```javascript
function findPath(start, goal, snake) {
  // Manhattan distance heuristic
  const heuristic = p => p.manhattan(goal);
  // ... implementation of A* loop
}
