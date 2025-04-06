# 🔥 The Walk of Fire

**The Walk of Fire** is a Game Boy Advance (GBA) game developed in C for CS 2110 at Georgia Tech.  
This adventure drops you into hell where you must guide your soul through waves of fire to reach salvation.

---

## 🎮 Gameplay

You just died. For your soul’s chance at heaven, you must survive the fire, avoid being hit in the heart, and make it to the right side of the screen.  

### Features:
- 🔥 **Dynamic Fireballs:** Fall and rise in randomized patterns.
- 🧘‍♂️ **Karma System:** Dodge fireballs to earn karma.
- 🧱 **State Machine:** Title screen, gameplay, win/lose screens, and "Impossible Mode".
- ⏱️ **Score Tracker:** Shows how many fireballs you’ve dodged.
- 🎨 **Custom Sprites:** Built with [nin10kit](https://github.com/TricksterGuy/nin10kit/raw/master/readme.pdf)
- 😈 **Impossible Mode:** Unlocked after winning once.

---

## 🕹️ Controls

| Button        | Action                                |
|---------------|----------------------------------------|
| Arrow Keys    | Move your soul                        |
| `Enter`       | Start game                            |
| `Backspace`   | Restart from title screen             |
| `←` (on Win)  | Enter Impossible Mode                 |

---

## 🚀 How to Build & Run

### 📦 Requirements

- [Docker Desktop](https://www.docker.com/products/docker-desktop)
- CS 2110 Docker Image: `gtcs2110/cs2110docker-c:stable-gba`
- The mGBA emulator (runs automatically inside the container)

---

### 🧪 Step-by-Step Instructions

#### 1. Clone the Repo & Enter the Directory

```bash
git clone https://github.com/vishruthanand08/walk-of-fire-gba.git
cd walk-of-fire-gba
```

#### 2. Start the Docker Container

```bash
./cs2110docker-c.sh start
```

> This mounts your project into the Docker container and pulls the correct image.

#### 3. Inside the Docker Container, Run:

```bash
cd host
make mgba
```

> This compiles the `.gba` ROM and automatically launches it in the mGBA emulator.

---

### 🛑 To Stop the Docker Container

```bash
./cs2110docker-c.sh stop
```

---

## 📁 Project Structure

| File / Folder         | Purpose                                 |
|------------------------|------------------------------------------|
| `main.c`              | Game state machine and gameplay logic    |
| `gba.c` / `gba.h`     | DMA, pixel, and screen drawing functions |
| `images/`             | Sprite/image assets from nin10kit        |
| `client.c`            | Docker socket bridge for emulator        |
| `cs2110docker-c.sh`   | Script to manage Docker container        |
| `Makefile`            | Build logic, GDB support, emulator calls |

---

## 📸 Screenshots

*Coming soon!* Add images like `images/fires.png`, `images/heaven.png`, or even a GIF of gameplay.

---

## 👤 Author

**Vishruth Anand**  
CS 2110 - Georgia Tech  
*The Walk of Fire*

---

## 📜 License

This project is for educational use only — developed as part of the CS 2110 coursework.
