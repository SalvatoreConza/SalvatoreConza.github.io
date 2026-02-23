# SalvatoreConza.github.io | Interactive Terminal Portfolio 🎮

Welcome to my personal portfolio! This is a unique, interactive web experience built to resemble a retro terminal interface. You can view the live site here: [salvatoreconza.github.io](https://salvatoreconza.github.io)

It's written entirely in vanilla HTML, CSS, and JavaScript, utilizing Tailwind CSS for the UI components. The portfolio features two distinct modes: a standard, professional mode and a "gamified" Pokémon-style battle mode.

## ✨ Features

### 1. Dual-Mode Interface
On initialization, the user is asked a simple question: **"DO YOU WANT TO PLAY?"**
* **If "no":** The terminal loads a standard, professional portfolio. The user can type commands like `about`, `projects`, `skills`, and `social` to learn more about me.
* **If "yes":** The terminal boots into the gamified Pokémon mode.

### 2. Gamified Portfolio Mode
In this mode, the standard portfolio commands (`about`, `projects`, `skills`, etc.) are linked to one of 6 Pokémon.
* **Team Selection:** The first 3 commands the user types "catch" the associated Pokémon, adding them to the player's team.
* **3v3 Battle:** Once the player's team of 3 is full, a 3v3 Pokémon battle automatically begins against the 3 remaining Pokémon serving as the "opponent" team.

### 3. Dynamic Pokémon Battle System
The battle is a fully functional turn-based system featuring:
* **Dynamic ASCII Art:** Pokémon sprites are fetched from the PokeAPI, drawn to an HTML `<canvas>`, and converted into colorful ASCII art in real-time. Each character in the art is wrapped in a `<span>` retaining its original pixel color.
* **Battle UI:** The terminal displays a special battle pane showing the player's Pokémon (back sprite) and opponent's Pokémon (front sprite).
* **HP Bars:** Colorful, text-based HP bars that update dynamically after every attack.
* **Combat Logic:** Users can type `moves` to list attacks or `1`-`4` to use a move. The enemy AI selects a random move on its turn.
* **Fainting & Switching:** When a Pokémon faints, the next in the party is automatically sent out until one team is entirely defeated.

## 🛠️ Core Technologies

* **HTML5:** Structures the terminal window.
* **Tailwind CSS:** Handles all major UI components, layout, and responsiveness.
* **Vanilla JavaScript (ES6+):** Powers all application logic, including:
  * State management (tracking `init`, `menu`, `game_menu`, and `battle` states).
  * Command parsing and processing.
  * Dynamic HTML generation for terminal output.
  * The complete battle system logic.
* **HTML `<canvas>` API:** Used for the `generateAscii` function. It reads pixel data (color and alpha) from an image to dynamically create the colored `<span>` elements for the ASCII art.

## 🚀 How to Use

1. Visit the live site or clone this repository and open `index.html` in any modern web browser.
2. Interact with the terminal by typing commands and hitting `Enter`.
3. Type `yes` at the start prompt to try the game mode!
   * Type `about`, `projects`, `contacts`, `papers`, `skills`, or `github` to select your team.
   * Once you have 3 Pokémon, the battle will begin.
   * In battle, type `moves` or `status` for info, or `1`-`4` to attack.
4. Type `reset` at any time to restart the entire experience and clear the terminal.
