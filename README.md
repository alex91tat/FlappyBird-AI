<div>

# 🐦 Flappy Bird AI 

### An intelligent Flappy Bird clone featuring a **NEAT-inspired neural network** that learns to play the game through evolutionary algorithms.

*Built with Python & Pygame*

---

## 🎯 About the Project

This project is a **Flappy Bird** game clone built with **Pygame** that features two game modes:

1. **Manual Mode** — The classic Flappy Bird experience where the player controls the bird.
2. **AI Mode** — A population of birds controlled by neural networks that **learn to play** the game through **neuroevolution** (NEAT — NeuroEvolution of Augmenting Topologies).

The AI starts with no knowledge of the game and, over successive generations, evolves neural networks that become increasingly skilled at navigating through pipes. The project demonstrates key AI concepts such as **neural networks**, **genetic algorithms**, **speciation**, and **natural selection**.

---

## ✨ Features

| Feature | Description |
|---|---|
| 🎮 **Manual Play Mode** | Classic Flappy Bird gameplay with keyboard/mouse controls |
| 🤖 **AI Mode** | Watch a population of 50 birds evolve and learn to play |
| 🧠 **Neural Network** | Each bird has its own brain (feedforward neural network) |
| 🧬 **Neuroevolution** | Genetic algorithms with mutation, crossover, and speciation |
| 🏆 **Scoring System** | Real-time score tracking with persistent high score |
| 🏅 **Medal System** | Bronze, Silver, Gold, and Platinum medals based on score |
| ⏸️ **Pause/Resume** | Pause the game at any time with a button or keyboard shortcut |
| 📊 **AI HUD** | Live display of generation count, alive birds, and best score |

---

## 🧠 How the AI Works

The AI is built on a **NEAT-inspired** neuroevolution framework. Here's how it works at a high level:

### Neural Network Architecture

- **3 Input Nodes**: Distance to top pipe, horizontal distance to next pipe, distance to bottom pipe
- **1 Bias Node**: Constant value of 1
- **1 Output Node**: Sigmoid-activated decision (> 0.7 → flap)

### Evolutionary Process


1. **Population Initialization** — 50 birds with random neural network weights
2. **Evaluation** — Each bird plays the game; fitness = lifespan + (pipes_passed × 50)
3. **Speciation** — Birds are grouped into species based on weight similarity
4. **Selection** — Stale and extinct species are culled
5. **Reproduction** — Champions are cloned; offspring are created with mutations
6. **Mutation** — 80% chance of weight perturbation per connection (10% chance of full reset)

---

## 📁 Project Structure

```
flappy-bird-ai-segmentationfaults-2/
│
├── main.py                    # Entry point — initializes Pygame and runs the game loop
├── bird.py                    # Bird class — physics, collision, AI vision & decision-making
├── pipe.py                    # Pipe class — obstacle sprites (top and bottom)
├── ground.py                  # Ground class — scrolling ground sprite
├── score.py                   # High score persistence (load/save to file)
├── utils.py                   # Constants, image loading, scaling, game state definitions
├── ui.py                      # UI components — buttons, title, score display, copyright
├── highscore.txt              # Persistent high score storage
│
├── game_modules/              # Game logic and screen management
│   ├── game_config.py         # Global game configuration (state, scores, AI settings)
│   ├── game_controller.py     # Core game loop — handles both manual and AI modes
│   └── screens.py             # Menu, Get Ready, and Game Over screen renderers
│
├── ai/                        # Neuroevolution AI module
│   ├── __init__.py            # Module initializer
│   ├── brain.py               # Neural network (feedforward, mutation, cloning)
│   ├── node.py                # Network node with sigmoid activation
│   ├── connection.py          # Weighted connection between nodes with mutation
│   ├── population.py          # Population management — natural selection, speciation
│   └── species.py             # Species grouping — similarity, fitness, offspring
│
└── sprites/                   # Game assets (PNG/JPG)
    ├── *bird*.png             # Bird animation frames (red, blue, yellow)
    ├── pipe-green*.png        # Pipe sprites (top and bottom)
    ├── background-*.png       # Background images (day and night)
    ├── base.png               # Ground texture
    ├── *.png (0-9)            # Digit sprites for score display
    ├── *_medal.png            # Medal images (bronze, silver, gold, platinum)
    ├── gameover.png           # Game over banner
    ├── message.png            # Get ready message
    ├── start.png              # Start screen image
    └── btn*.png / *.jpg       # UI button sprites (pause, restart, menu, AI mode)
```

---

## 🚀 Getting Started

### Prerequisites

- **Python 3.7+**
- **Pygame** — Game development library for Python

### Running the Game

```bash
python main.py
```

---

## 🎮 Game Controls

### Menu Screen

| Action | Control |
|---|---|
| Start Game (Manual) | Click **START** button or press `Space` |
| Start Game (AI Mode) | Click **AI** button |
| View High Score | Click **SCORE** button |

### During Gameplay (Manual Mode)

| Action | Control |
|---|---|
| Flap | `Space`, or `Left Click` |
| Pause / Resume | `P`, `Escape`, or click the pause button |

### Game Over Screen

| Action | Control |
|---|---|
| Restart | Press `R` or click **Restart** button |
| Return to Menu | Press `M` or click **Menu** button |

### AI Mode

In AI mode, the game runs autonomously. A **HUD** at the bottom-left displays:
- **Generation number** — Current evolutionary generation
- **Alive count** — Number of birds still alive out of 50
- The **best score** across all generations is displayed at the top center

---

## 👥 Team

| Name | GitHub 
|---|---|
| *Alex Tat* | [@alex91tat](https://github.com/alex91tat) |
| *Ariana Turc* | [@arianaturc](https://github.com/arianaturc) |
| *Paul Dobra* | [@pold8](https://github.com/pold8) |



---

<div align="center">


</div>


