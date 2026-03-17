# Penalty Shootout Game

A browser-based penalty shootout game built with p5.js as a high school project.

---

## Overview

A two-player penalty shootout game where each team takes turns shooting penalties.
Players choose which side of the goal to shoot, while the goalkeeper randomly moves
between three positions. The team with the most goals after two rounds wins.

---

## How to Play

1. Press **Space** to advance through the intro screens
2. **Red team** shoots first — you have 60 seconds
3. Shoot by pressing the arrow keys:
   - `←` Left arrow — shoot left
   - `↑` Up arrow — shoot centre
   - `→` Right arrow — shoot right
4. A goal is scored if the goalkeeper is **not** in the same position as your shot
5. The goalkeeper changes position every 2 seconds
6. After 60 seconds, **Blue team** takes their turn
7. The team with the most goals wins!

---

## Controls

| Key | Action |
|-----|--------|
| `Space` | Advance to next screen |
| `← ↑ →` | Shoot left / centre / right |
| `B` | Force blue team victory screen |
| `R` | Force red team victory screen |

---

## Files

| File | Description |
|------|-------------|
| `sketch.js` | Main game logic |
| `img1.jpg` – `img7.jpg` | Game screen images |
| `img_goal.jpg` | Goal screen image |
| `img8_blaasejr.jpg` | Blue team victory screen |
| `img8_rodsejr.jpg` | Red team victory screen |
| `clap.mp3` | Victory sound effect |

---

## Requirements

- A browser with JavaScript enabled
- [p5.js](https://p5js.org/) and p5.sound library

---

## Known Issues

- Scoring can count multiple goals per shot due to re-rendering in `draw()` — score
  increments every frame the goal variables are set rather than once per keypress
- Timer continues running after the round ends if not handled carefully
- No draw/tie handling — if scores are equal, no winner screen is shown
