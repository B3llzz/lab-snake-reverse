# **🍎 Reversed Snake: The Swarm**

**Survival Horror in 8-bit.** The classic Nokia hit, inverted. You control the food, and the Snake is an AI determined to eat you.

## **🎮 Play Now**

👉 [**Click here to play the live game**](https://imbios.github.io/lab-snake-reverse/)

## **✨ Overview**

**Reversed Snake** is a lightweight, single-file browser game built with **Vanilla JavaScript** and **HTML5 Canvas**.

Instead of guiding the snake, you play as the **Apple**. The Snake is controlled by a pathfinding algorithm (A\*) that ruthlessly hunts you down. As time passes, the snake grows longer, making the grid increasingly claustrophobic.

**Level 10** features a "Swarm Mode" where you must dodge 10 snakes simultaneously.

## **🕹️ How to Play**

1. **Desktop:** Use your **Arrow Keys** (⬆️ ⬇️ ⬅️ ➡️) to move the Red Apple.  
2. **Mobile:** Use the **on-screen joystick** to navigate.  
3. **Objective:** Survive as long as possible. Do not let any Snake head touch you.

## **🧠 Technical Details**

### **The AI (A\* Search)**

The snake utilizes a PriorityQueue to calculate the most efficient path to the player's coordinates. To maintain 60FPS with 10 snakes, the game uses a **Collision Grid Cache** (O(1) lookup) instead of checking every snake body segment individually.

```js
function findPath(start, goal, snake) {  
  // Manhattan distance heuristic  
  const heuristic \= p \=\> p.manhattan(goal);  
  // ... implementation of A\* loop  
}
```

### **📱 Features**

* **Responsive:** Works on iPhone, Android, and Desktop.  
* **Zero Dependencies:** Written in pure JS. No libraries, no frameworks, just one .html file.  
* **High Scores:** Saves your best times for each level to localStorage.

## **🚀 Installation**

No build steps required.

```sh
# Clone the repository  
git clone https://github.com/ImBIOS/lab-snake-reverse.git

# Navigate to directory  
cd lab-snake-reverse

# Open in browser  
open index.html
```

## **📄 License**

This project is open source and available under the [MIT License](./LICENSE).
