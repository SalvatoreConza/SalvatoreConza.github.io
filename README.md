# SalvatoreConza.github.io

# Interactive Terminal Portfolio (with Pokémon Battle!)

This is a unique, interactive personal portfolio built to resemble a terminal interface. It's written entirely in vanilla HTML, CSS, and JavaScript, using Tailwind CSS for the UI components.

The portfolio has two modes: a standard, professional mode and a "gamified" Pokémon-style battle mode.

## Features

### 1. Dual-Mode Interface

On initialization, the user is asked a simple question: "DO YOU WANT TO PLAY?".

* **If "no"**: The terminal loads a standard, professional portfolio. The user can type commands like `about`, `projects`, `skills`, and `social` to learn more about me.
* **If "yes"**: The terminal loads the "gamified" version.

### 2. Gamified Portfolio Mode

In this mode, the portfolio commands (`about`, `projects`, `skills`, etc.) are linked to one of 6 Pokémon.

* **Team Selection:** The first 3 commands the user types "catch" the associated Pokémon, adding them to the player's team.
* **3v3 Battle:** Once the player's team of 3 is full, a 3v3 Pokémon battle automatically begins against the 3 remaining Pokémon as the "opponent" team.

### 3. Dynamic Pokémon Battle System

The battle is a fully turn-based system with:

* **Dynamic ASCII Art:** Pokémon sprites are fetched from the PokeAPI, drawn to an HTML `<canvas>`, and converted into colorful ASCII art in real-time. Each character in the art is wrapped in a `<span>` with its original pixel color.
* **Battle UI:** The terminal displays a special "battle" pane showing the player's (back sprite) and opponent's (front sprite) Pokémon.
* **HP Bars:** Colorful, text-based HP bars update after every attack.
* **Combat Logic:** Users can type `moves` to list attacks or `1`-`4` to use a move. The enemy AI selects a random move on its turn.
* **Fainting & Switching:** When a Pokémon faints, the next in the party is automatically sent out until one team is defeated.

### 4. Core Technologies

* **HTML5:** Structures the terminal window.
* **Tailwind CSS:** Used for all major UI components, layout, and responsiveness.
* **Vanilla JavaScript (ES6+):** Powers all logic, including:
    * State management (tracking `init`, `menu`, `game_menu`, `battle` states).
    * Command parsing and processing.
    * Dynamic HTML generation for terminal output.
    * The complete battle system logic.
* **HTML `<canvas>` API:** Used for the `generateAscii` function. It reads pixel data (color and alpha) from an image to dynamically create the colored `<span>` elements for the art.

## How to Use

1.  Open the `portfolio.html` file in any modern web browser.
2.  Interact with the terminal by typing commands.
3.  Type `yes` at the start to try the game mode!
    * Type `about`, `projects`, `contacts`, `papers`, `skills`, or `github` to select your team.
    * Once you have 3, the battle will begin.
    * In battle, type `moves` or `status` for info, or `1`-`4` to attack.
    * Type `reset` at any time to restart the entire experience.

---
