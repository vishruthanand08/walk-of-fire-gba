# 🔥 The Walk of Fire

**The Walk of Fire** is a Game Boy Advance (GBA) game developed in C for CS 2110 at Georgia Tech.  
Inspired by games like *World's Hardest Game*, this adventure drops you into hell where you must guide your soul through waves of fire to reach salvation.

---

## 🎮 Gameplay

You just died. For your soul’s chance at heaven, you must survive the fire, avoid being hit in the heart, and make it to the right side of the screen.  

Features:
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

- [Docker](https://www.docker.com/products/docker-desktop)
- CS 2110 Docker Image (`gtcs2110/cs2110docker-c:stable-gba`)
- mGBA emulator (included in CS 2110 Docker setup)

---

### 🧪 Step-by-Step Instructions

#### 1. Clone the Repo & Enter the Directory

```bash
git clone https://github.com/vishruthanand08/walk-of-fire-gba.git
cd walk-of-fire-gba

#### 2. Start Docker container
'''bash
./cs2110docker-c.sh start

#### 3. Run game 
'''bash
cd host
make mgba
