# TwinkleToes 🎮

A 2D platformer game developed in **Unity** using **C#**, created as a Game Development course project at **HITEC University, Taxila**.

TwinkleToes focuses on precision platforming, where the player navigates through multiple levels, avoids traps and hazards, and reaches the finish point to progress through the game.

---

## 📌 Project Overview

**TwinkleToes** was developed to gain practical experience with the fundamental concepts of 2D game development using Unity.

The project demonstrates:

* 2D player movement
* Rigidbody-based physics
* Collision detection
* Player death and life handling
* Hazard detection
* Level progression
* Scene management
* Main Menu and End Screen
* UI button interactions
* C# scripting
* 2D pixel-art game design

---

## 🎮 Gameplay

The player controls a 2D character and must carefully traverse each level while avoiding traps and other hazards.

### Game Flow

```text
Main Menu
    ↓
Level 1
    ↓
Level 2
    ↓
   ...
    ↓
Final Level
    ↓
End Screen
```

If the player encounters a hazard:

```text
Hazard Collision
      ↓
Player Dies
      ↓
Death Animation + Sound
      ↓
Current Level Reloads
```

After completing the final level, the player can either:

* Restart the game from Level 1
* Return to the Main Menu

---

## ⚙️ Core Game Mechanics

### 1. Player Movement and Physics

The player controller uses Unity's:

* `Rigidbody2D`
* `BoxCollider2D`

The system supports:

* Horizontal movement
* Jumping
* Gravity
* Physics-based movement
* Collision handling

---

### 2. Player Life System

The `PlayerLife.cs` script manages the player's death state.

When the player touches a hazard:

1. The collision is detected.
2. Player movement is disabled.
3. Death animation is triggered.
4. Death sound is played.
5. The current scene is restarted.

---

### 3. Hazards and Collision Detection

Unity's **Tag System** is used to distinguish hazards from normal terrain.

| Object  | Tag      |
| ------- | -------- |
| Player  | `Player` |
| Hazards | `Trap`   |

This allows the game to respond specifically when the player comes into contact with a dangerous object.

---

### 4. Level Progression

Each level contains a designated **Finish Point**.

When the player reaches it:

```text
Player reaches Finish Point
          ↓
OnTriggerEnter2D()
          ↓
Victory Sound
          ↓
Next Scene Loaded
```

Level transitions are handled using Unity's `SceneManager`.

---

## 🧩 C# Scripts

The game functionality is divided into separate scripts according to responsibility.

### `PlayerLife.cs`

Responsible for the player's life cycle.

**Functions include:**

* Detecting hazard collisions
* Triggering the death animation
* Playing death sound effects
* Disabling player movement
* Reloading the current scene

---

### `FinishPoint.cs`

Responsible for level completion.

**Functions include:**

* Detecting the player using `OnTriggerEnter2D()`
* Playing victory sound effects
* Loading the next level
* Managing level progression

---

### `EndMenu.cs`

Controls the final game screen.

**Functions include:**

* Restarting the game from Level 1
* Returning to the Main Menu
* Connecting UI buttons with scene-management functions

---

## 🛠️ Technologies & Tools

| Component            | Technology         |
| -------------------- | ------------------ |
| Game Engine          | Unity              |
| Programming Language | C#                 |
| IDE                  | Visual Studio      |
| Physics              | Unity Rigidbody2D  |
| Collision            | Unity Collider2D   |
| Scene Management     | Unity SceneManager |
| Asset Pack           | Pixel Adventure 1  |
| Target Platform      | Windows PC         |

---

## 🎨 Assets

The project extensively uses the **Pixel Adventure 1** asset pack for the game's retro pixel-art presentation.

Assets include:

* Character sprites
* Environment tiles
* Character animations
* Decorative objects
* UI elements

These assets provide a consistent pixel-art visual style throughout the game.

---

## 🖥️ Game Screens

The game contains:

### Main Menu

The starting interface where the player can begin the game.

### Playable Levels

Multiple platforming levels with different layouts, obstacles, and hazards.

### End Screen

Displayed after successfully completing the final level.

Players can:

* Restart from Level 1
* Return to the Main Menu

---

## 🧠 Challenges & Solutions

### Scene Management

**Challenge:**
Managing transitions between the Main Menu, multiple gameplay levels, and the End Screen.

**Solution:**
Scene names were used with Unity's `SceneManager`, for example:

```csharp
SceneManager.LoadScene("Level 1");
```

Using explicit scene names helped make scene routing easier to maintain.

---

### Collision Detection

**Challenge:**
Distinguishing dangerous hazards from ordinary platforms and terrain.

**Solution:**
Unity's Tag System was used to identify objects:

```text
Player → "Player"
Hazards → "Trap"
```

This allowed the game to respond specifically to hazard collisions.

---

## 📚 Learning Outcomes

Through this project, I gained practical experience with:

* Unity 2D game development
* C# scripting
* Rigidbody2D physics
* Collider-based interactions
* Trigger events
* Unity Tags
* Scene management
* UI button integration
* Game-state handling
* Animation and sound integration
* Structuring gameplay logic across multiple scripts

---

## 🚀 Future Improvements

Potential future enhancements include:

* More playable levels
* Additional enemy types
* Collectible items
* Health/checkpoint systems
* Level timer
* Score system
* Improved animations
* Additional player abilities
* Background music and expanded sound design
* Save/progress system
* Multiple difficulty levels

---

## 👨‍💻 Developer

**Muhammad Huzaifa**
BS Computer Science — HITEC University, Taxila
Section 6C

**Course:** Game Development
**Instructor:** Irfan Haider

---

## 📄 Project Information

**Project:** TwinkleToes
**Type:** 2D Platformer Game
**Engine:** Unity
**Language:** C#
**Platform:** Windows PC
