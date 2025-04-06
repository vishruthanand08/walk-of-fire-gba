# The Walk of Fire 🔥

The Walk of Fire is a Game Boy Advance (GBA) game developed in C for CS 2110 at Georgia Tech.  
Inspired by World's Hardest Game, this GBA adventure drops you into hell, where you must guide your soul through waves of fire to reach salvation.

## Gameplay 🎮

You just died. For your soul’s chance at heaven, you must survive the fire, avoid being hit in the heart, and make it to the right side of the screen.

### Features

- 🔥 Dynamic Fireballs: Fall and rise in randomized patterns.
- 🧘‍♂️ Karma System: Dodge fireballs to earn karma.
- 🧱 State Machine: Title screen, gameplay, win/lose screens, and "Impossible Mode".
- ⏱️ Score Tracker: Displays how many fireballs you’ve dodged.
- 🎨 Custom Sprites: Created using [nin10kit](https://github.com/TricksterGuy/nin10kit/raw/master/readme.pdf).
- 😈 Impossible Mode: Unlocked after completing normal mode.


## Controls 🕹️

- Arrow Keys — Move your soul
- Enter — Start the game
- Backspace — Restart from the title screen
- Left Arrow (←) — Activate Impossible Mode after winning

## Requirements

- [Docker Desktop](https://www.docker.com/products/docker-desktop)
- CS 2110 Docker image: `gtcs2110/cs2110docker-c:stable-gba`
- mGBA emulator (runs automatically inside the Docker container)

## Setup Instructions

1. Clone the Repository

   ```bash
   git clone https://github.com/vishruthanand08/walk-of-fire-gba.git
   cd walk-of-fire-gba
   ```

2. Start the Docker Container

   ```bash
   ./cs2110docker-c.sh start
   ```

   This pulls the image and mounts your project inside the container.

3. Run the Game in mGBA

   ```bash
   cd host
   make mgba
   ```

   This compiles the `.gba` ROM and launches the emulator.

4. Stop the Docker Container (when done)

   ```bash
   ./cs2110docker-c.sh stop
   ```

---

## File Structure 📁

| File/Folder         | Description                                      |
|---------------------|--------------------------------------------------|
| `main.c`            | Game logic, state machine                        |
| `gba.c` / `gba.h`   | Drawing utilities, screen & pixel control        |
| `images/`           | Sprite assets (created with nin10kit)            |
| `client.c`          | Sends ROM to emulator through Docker             |
| `cs2110docker-c.sh` | Script for managing Docker container             |
| `Makefile`          | Build process, GBA toolchain commands            |

---

## Author 👤

Vishruth Anand

## License 📜

This project was built as part of CS 2110 and is for educational use only.

