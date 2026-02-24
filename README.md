# 🐍 Classic Nokia Snake - Web Edition

**Official Tribute Page & Browser Game**  

This is a **retro browser-based recreation of the classic Nokia Snake game** (1997). The goal is simple: guide a snake around the screen to eat food, grow longer, and avoid collisions. This project replicates the original Nokia experience, complete with pixelated graphics, dot-matrix styling, and classic keypad controls.

**💡 Note:** This was developed as a **group mini-project** by **Sanika, Japji, Parth, and Subrato**.  
- **Parth** focused on **JavaScript/game logic**  
- **Subrato** focused on **HTML structure**  
- **Japji** and **Sanika** focused on **CSS and styling**

---

## 🎮 Game Overview

Snake is one of the most iconic mobile games in history. The player controls a moving snake on a grid, collecting food items to increase the snake's length. The challenge grows as the snake becomes longer, making collisions with itself more likely.  

**Key Gameplay Features in this Version:**

- **Grid-Based Movement:** The snake moves in discrete steps on a pixel grid, giving it a classic 8-bit feel.  
- **Wrapping Walls:** Passing off one edge of the screen makes the snake appear on the opposite side.  
- **Instant Input Response:** The game responds immediately to directional input.  
- **Increasing Difficulty:** As you collect more food, the game speed gradually increases.  
- **High Score Tracking:** The best score is saved in the browser using `localStorage`.  

---

## 🕹 How to Play

### Controls

- **Arrow Keys** → Move the snake in that direction  
- **Menu / Start Button** → Start or restart the game  
- **On-screen Buttons** → Touch controls for mobile devices  

### Rules

1. Navigate the snake to eat the food that appears randomly on the screen.  
2. Each food increases your **score by 10 points** and grows the snake.  
3. Avoid colliding with the snake's own body. Collision ends the game.  
4. The snake can pass through walls due to wrapping mechanics.  
5. Speed gradually increases as your score grows, increasing the challenge.  

---

## 🖌 Game Design

- **Pixelated Graphics:** Snake, food, and background grids replicate a retro Nokia LCD feel.  
- **Screen Glow Effect:** Simulates the classic greenish dot-matrix display using CSS.  
- **Overlay UI:** Displays start screen, game over screen, and score in pixel font.  
- **Info Cards:** Sections detailing the game’s developer, timeline, and gameplay features.  
- **Keypad Interface:** On-screen buttons simulate the classic Nokia keypad.  

---

## 🔢 How the Game Works (Logic Overview)

1. **Snake Representation:** The snake is stored as an array of `{x, y}` coordinates.  
2. **Movement:** Each game tick, the snake moves one step in the current direction.  
3. **Food Generation:** Food appears randomly on the grid. Eating food increases the snake length.  
4. **Collision Detection:** Checks if the snake head touches its own body to trigger game over.  
5. **Screen Wrapping:** The snake appears on the opposite side if it crosses the edge.  
6. **Speed Adjustment:** The interval between game ticks decreases as score increases.  
7. **High Score Tracking:** If the current score exceeds the stored high score, it updates `localStorage`.  

---

## 💾 Saving High Scores

High scores are automatically stored in the browser:

```javascript
localStorage.setItem('snake_hs', highScore);
