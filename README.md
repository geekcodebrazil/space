# Space Invaders

<p align="center"><img alt="space invaders screenshot" src="assets/images/screenshot_space_invaders.png"></p>

## Description

This project is a web-based implementation of the classic arcade game "Space Invaders." Players control a laser cannon to defend against waves of descending aliens, while also evading enemy fire and a periodically appearing spaceship. The game features a scoring system, multiple lives, and the ability to store and view high scores using a PHP backend and a database.

## Features

* **Classic Gameplay:** Faithful recreation of the original Space Invaders mechanics.
* **Player Control:** Move the player's ship left and right using arrow keys and fire with the spacebar.
* **Alien Formations:** Multiple rows of aliens of different types descend towards the player.
* **Alien Movement & Firing:** Aliens move horizontally, periodically dropping down, and randomly fire back at the player.
* **Enemy Spaceship:** A special spaceship periodically flies across the top of the screen, which can be shot for bonus points.
* **Scoring System:** Players earn points for destroying aliens and the enemy spaceship. The score is displayed during gameplay.
* **Lives System:** The player starts with a set number of lives and loses a life upon being hit or if aliens reach the bottom.
* **Game Over Conditions:** The game ends if the player loses all lives or if the aliens successfully invade (reach the player's level).
* **Win Condition:** The player wins by defeating all waves of aliens.
* **Sound Effects:** Includes sounds for player shooting, alien movement, explosions, and the enemy spaceship.
* **High Score System:**
    * After a game ends (win or lose), the player's score is submitted.
    * Scores are stored in a database via a PHP backend (`store_score.php`).
    * A separate page (`show_highscore.php`) displays the top 10 high scores retrieved from the database.
* **Game Menu:** A simple HTML menu (`space_invaders_menu.html`) allows navigation to play the game or view high scores.
* **Restart Option:** A "REINICIAR" (Restart) button is available on the game over screen.

## Technologies Used

* **HTML5:** Structure for the game, menu, and high score pages.
* **CSS:** Styling for the game elements (mostly inline within HTML).
* **JavaScript:** Core game logic, canvas rendering, controls, collision detection, and sound management.
* **PHP:** Backend processing for storing and retrieving high scores from a database.
* **SQL Database:** (Implied) Used by the PHP scripts to store player names and scores.

## How to Play

1.  **Navigate:** Start from the `space_invaders_menu.html` to either play the game or view high scores.
2.  **Movement:** Use the **Left Arrow Key** to move your ship left and the **Right Arrow Key** to move your ship right.
3.  **Shooting:** Press the **Spacebar** to fire your laser cannon.
4.  **Objective:**
    * Destroy all the aliens in each wave before they reach the bottom of the screen.
    * Avoid being hit by alien projectiles.
    * Try to hit the bonus spaceship that occasionally flies by.
5.  **Game End:** The game ends if you lose all your lives or an alien reaches your defense line.
6.  **Scoring:** Your score increases with each alien destroyed. Try to achieve the highest score possible!
7.  **High Scores:** After the game, your score can be saved. You can view the top scores on the "Highscore" page.

## Files Included

* `index.html` (or `space_invaders.html` as linked from menu): The main game page containing the canvas and JavaScript game logic.
* `space_invaders_menu.html`: The main menu page.
* `show_highscore.php`: PHP script to display the high scores from the database.
* `store_score.php`: PHP script to save the player's name and score to the database.
* `README.md`: This file.
* **assets/images/** (directory): Contains images like `star_background.jpg` and `screenshot_space_invaders.png`.
* **assets/sound/** (directory): Contains sound files like `ufo_lowpitch.wav`, `fastinvader1-4.wav`, `shoot.wav`, `explosion.wav`, `invaderkilled.wav`.

## Setup for High Score Functionality

To use the high score feature, you will need:

1.  A web server (like Apache or Nginx) with PHP support.
2.  A MySQL (or compatible) database.
3.  The PHP scripts (`show_highscore.php`, `store_score.php`) require database credentials to be configured within them (currently hardcoded with placeholder values like `id9791891_lulu98`).
4.  A database table named `spaceInvaders` with at least `name` and `score` columns must exist.

## Sources from original README.md

### Audio
Audio samples: https://www.classicgaming.cc/classics/space-invaders/sounds

### Images
Sky full of stars: https://wallpaperplay.com/walls/full/8/c/9/163758.jpg
Aliens: https://cdn2.vectorstock.com/i/1000x1000/54/21/space-invaders-8bit-aliens-icons-set-vector-1625421.jpg

## TODO (from original README.md)

* asteroids for safety
* (Potentially: Add defense station destruction animation - noted in `index.html` comments)
