# Pac-Man Game (Java Swing)

## Project Overview

The Pac-Man Game is a arcade-style maze game recreated in **Java** using the **Swing/AWT** GUI framework. The player controls Pac-Man through a maze, collecting dots for points while avoiding four AI-controlled ghosts.

This project demonstrates core **Object-Oriented Programming (OOP)** concepts — encapsulation, reusable classes, and event-driven design — combined with real-time game logic such as collision detection, movement handling, and a game loop driven by Java's `Timer` class.

---

## Objectives

* Recreate the Pac-Man gameplay experience using Java.
* Apply object-oriented design principles to game development.
* Implement real-time collision detection and movement mechanics.
* Simulate basic ghost AI behavior using randomized movement.
* Demonstrate event-driven programming using keyboard input handling.

---

## Features

* Real-time Pac-Man movement using arrow key controls.
* Collision detection between Pac-Man, walls, ghosts, and food.
* Randomized ghost movement for unpredictable gameplay.
* Score tracking — 10 points awarded per dot collected.
* Lives system — 3 lives, with position reset on ghost collision.
* Game Over detection and restart functionality.
* Automatic maze reload once all dots are collected.

---

## Technologies Used

| Technology     | Purpose                              |
| -------------- | ------------------------------------- |
| Java           | Core game logic and application       |
| Swing / AWT    | GUI rendering and window management   |
| `javax.swing.Timer` | Game loop and frame updates      |
| `KeyListener`  | Keyboard input handling               |

---

## System Architecture

The system consists of:

* A `Block` class representing Pac-Man, ghosts, walls, and food items.
* A tile-map based maze layout (`String[]` grid) defining walls, paths, and starting positions.
* A game loop (`Timer`) that continuously updates positions and repaints the board.
* Collision-detection logic that governs movement, scoring, and life loss.

### Workflow

1. The maze is loaded from a tile map into wall, food, and ghost objects.
2. The player presses arrow keys to set Pac-Man's direction.
3. The game loop updates Pac-Man's and each ghost's position every frame.
4. Collisions are checked against walls, food, and ghosts.
5. Score and lives are updated based on collisions.
6. The game ends when lives reach zero, and can be restarted with a key press.

---

## Screenshots

### Start of Game
![Start of game](screenshots/gameplay-start.png)

### Gameplay in Progress
![Gameplay in progress](screenshots/gameplay-running.png)

### Game Over
![Game over screen](screenshots/gameover.png)

---

## Repository Structure

```text
Pacman-Java-Game/
│
├── README.md
├── App.java
├── PacMan.java
└──  Project_Report.pdf
```

> **Note:** The game also requires a set of image assets at runtime (`wall.png`, `blueGhost.png`, `orangeGhost.png`, `pinkGhost.png`, `redGhost.png`, `pacmanUp.png`, `pacmanDown.png`, `pacmanLeft.png`, `pacmanRight.png`), which should be placed alongside `PacMan.java` before running the project.

---

## How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/<your-username>/<your-repo-name>.git
   cd <your-repo-name>
   ```
2. Make sure the required image assets are placed alongside `PacMan.java`.
3. Compile the project:
   ```bash
   javac App.java PacMan.java
   ```
4. Run the game:
   ```bash
   java App
   ```
5. Use the **arrow keys** to move Pac-Man around the maze.

---

## Controls

| Key | Action |
|-----|--------|
| ⬆️ Up Arrow | Move up |
| ⬇️ Down Arrow | Move down |
| ⬅️ Left Arrow | Move left |
| ➡️ Right Arrow | Move right |
| Any key (after Game Over) | Restart the game |

---

## Future Enhancements

* Smarter, pathfinding-based ghost AI (e.g., BFS/A* chasing behavior).
* Power pellets that let Pac-Man temporarily eat ghosts.
* Multiple levels with increasing difficulty.
* Sound effects and background music.
* High-score leaderboard with persistent storage.
* Pause/resume functionality.

---

## Documentation

Detailed project documentation is available in:

* [`Project_Report.pdf`](Project_Report.pdf)

The report includes:

* Project overview and key features
* Game setup and maze rendering logic
* Player controls and collision detection
* Ghost movement logic
* Restart functionality
* Sample output/screenshots

---

## License

This project is developed for educational and academic purposes.
