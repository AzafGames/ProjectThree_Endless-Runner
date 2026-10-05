# 🏃 Endless Runner — Unity Game

A Unity-based **endless runner game inspired by the core gameplay mechanics of popular endless-running games such as Subway Surfers**.

This project is being developed from scratch as a learning and game-development project to understand and implement player movement, lane switching, obstacles, collectibles, procedural/endless environments, scoring, health, UI systems, animations, and other essential gameplay mechanics.

> ⚠️ **Disclaimer:** This is an independent educational project inspired by the endless-runner genre. It is not affiliated with, endorsed by, or a copy of Subway Surfers or its developers. Original assets and implementations are used wherever possible.

---

## 🎮 Game Overview

The player controls a character running continuously through an endless environment.

The objective is to:

* 🏃 Keep running for as long as possible
* ↔️ Move between lanes
* ⬆️ Jump over obstacles
* ⬇️ Slide/duck under obstacles
* 🪙 Collect coins and other collectibles
* 🚧 Avoid obstacles
* ❤️ Manage player health or lives
* 📈 Achieve the highest possible score
* ⚡ Survive as the game progressively becomes more challenging

The game world is continuously generated or repositioned to create the illusion of an **infinite environment**.

---

# 🎯 Project Goals

The main goals of this project are to learn and implement:

* Unity game development fundamentals
* Character controller systems
* Endless runner mechanics
* Lane-based movement
* Jumping and sliding
* Collision detection
* Obstacle systems
* Collectible systems
* Score systems
* Health systems
* Increasing difficulty
* Endless environment generation
* Object pooling/repositioning
* UI and HUD development
* Animation systems
* Audio integration
* Game states
* Game-over and restart systems
* Performance optimization
* Clean and reusable C# code
* Git and GitHub project management

---

# 🕹️ Core Gameplay

## Player Movement

The player continuously moves forward while the player controls horizontal movement.

Planned controls include:

| Action     | Input               |
| ---------- | ------------------- |
| Move Left  | `A` / `←`           |
| Move Right | `D` / `→`           |
| Jump       | `W` / `↑` / `Space` |
| Slide      | `S` / `↓`           |

The control system may be expanded or modified during development.

---

# 🛤️ Lane System

The game uses a lane-based movement system.

The player can move between:

```text
LEFT LANE    CENTER LANE    RIGHT LANE
    |             |             |
    ↓             ↓             ↓
   [ ]           [ ]           [ ]
```

The player must quickly change lanes to avoid incoming obstacles and collect valuable items.

---

# 🚧 Obstacle System

Different obstacles will be placed throughout the environment.

Possible obstacles include:

* 🚧 Road barriers
* 🚆 Vehicles
* 🧱 Blocks
* 🚨 Moving obstacles
* 🛑 Stationary obstacles
* Other environmental hazards

Collision with an obstacle can result in:

* Health reduction
* Temporary stun
* Speed reduction
* Game over

depending on the implemented game rules.

---

# 🪙 Collectible System

Collectibles will be placed throughout the endless environment.

Planned collectible types:

* 🪙 Coins
* ⭐ Score items
* ⚡ Power-ups
* ❤️ Health items
* 🛡️ Special abilities

Collected items will update the corresponding gameplay systems and UI.

---

# 📊 Scoring System

The player's score will increase based on gameplay performance.

Possible score factors include:

* Distance traveled
* Coins collected
* Special items collected
* Obstacles avoided
* Missions completed
* Survival time

Example:

```text
Distance Score
      +
Coin Score
      +
Bonus Score
      ↓
 TOTAL SCORE
```

---

# ❤️ Health System

The player will have a health/life system.

Example:

```text
❤️ ❤️ ❤️
```

When the player collides with certain obstacles, health may decrease.

When health reaches zero:

```text
GAME OVER
```

The exact health rules may change during development.

---

# 🌍 Endless Environment

One of the primary systems of the project is the endless environment.

Instead of creating an enormous level, environment sections can be continuously reused.

Example:

```text
[Environment 1]
        ↓
[Environment 2]
        ↓
[Environment 3]
        ↓
[Environment 4]
        ↓
[Environment 1 reused]
        ↓
[Environment 2 reused]
        ↓
...
```

This approach helps create an effectively infinite level while reducing unnecessary memory usage.

---

# 🔄 Environment Repositioning

Environment pieces can be repositioned when they move behind the player.

Instead of continuously creating and destroying objects:

```text
Move → Detect End → Reposition → Reuse
```

This can improve performance and reduce unnecessary object creation.

---

# 🚗 Dynamic Obstacles

Obstacles will be spawned or repositioned at appropriate locations in the endless environment.

The system will control:

* Spawn position
* Lane selection
* Spawn timing
* Obstacle type
* Movement
* Destruction/reuse
* Difficulty scaling

---

# 📈 Difficulty System

The game will gradually become more challenging as the player survives longer.

Possible difficulty changes:

* Increased player/environment speed
* More frequent obstacles
* More complex obstacle patterns
* Reduced reaction time
* Increased obstacle variety
* More challenging collectible placement

Example:

```text
TIME
 ↓
Difficulty ↑
 ↓
Speed ↑
 ↓
Obstacle Frequency ↑
 ↓
Challenge ↑
```

---

# 🎨 Visual Environment

The environment may contain:

* Roads/tracks
* Buildings
* Trees
* Vehicles
* Signs
* Barriers
* Lamps
* Environmental props
* Background scenery
* Skybox
* Lighting effects
* Particles

The visual style will evolve throughout development.

---

# 🧍 Player Character

The player character will include:

* Idle/starting animation
* Running animation
* Jump animation
* Falling animation
* Sliding animation
* Hit/damage animation
* Game-over animation

The character controller will be implemented using C# scripts and Unity components.

---

# 🎥 Camera System

The camera will follow the player and maintain an appropriate gameplay perspective.

Planned camera features:

* Player following
* Smooth movement
* Camera positioning
* Camera rotation
* Dynamic camera effects
* Optional shake effects

---

# 🖥️ UI / HUD

The game will contain an in-game HUD displaying important gameplay information.

Planned UI elements:

```text
--------------------------------
 SCORE: 000000

 🪙 000

 ❤️ ❤️ ❤️
--------------------------------
```

Possible UI screens:

### Main Menu

* Play
* Settings
* Quit

### Gameplay HUD

* Score
* Coins
* Health
* Distance
* Power-ups

### Pause Menu

* Resume
* Restart
* Main Menu

### Game Over

* Final Score
* Best Score
* Restart
* Main Menu

---

# 🎮 Game States

The project will use different game states to organize gameplay.

Possible states:

```text
Main Menu
    ↓
Playing
    ↓
Paused
    ↓
Game Over
    ↓
Restart / Main Menu
```

This will help separate gameplay logic from UI and other systems.

---

# 🔊 Audio

Planned audio systems include:

### Sound Effects

* Player movement
* Jump
* Slide
* Coin collection
* Obstacle collision
* Power-up activation
* Button interaction
* Game over

### Background Music

* Main menu music
* Gameplay music
* Game-over music

---

# ⚡ Power-Ups

Future versions may include special power-ups such as:

* 🧲 Coin Magnet
* 🛡️ Shield
* ⚡ Speed Boost
* ✖️ Score Multiplier
* ❤️ Health Boost

Each power-up will have its own gameplay effect and duration.

---

# 🧠 AI / Enemy Systems

Future development may include AI-controlled characters or enemies.

Possible systems:

* Enemy movement
* Enemy spawning
* Enemy detection
* Enemy interaction
* Chase behavior
* Collision behavior

---

# 🗂️ Project Structure

The project will follow a structured Unity folder organization.

```text
Assets/
│
├── Art/
│   ├── Characters/
│   ├── Environment/
│   ├── Materials/
│   ├── Textures/
│   └── UI/
│
├── Audio/
│   ├── Music/
│   └── SFX/
│
├── Animations/
│
├── Prefabs/
│   ├── Player/
│   ├── Obstacles/
│   ├── Collectibles/
│   └── Environment/
│
├── Scenes/
│   ├── MainMenu/
│   └── Gameplay/
│
├── Scripts/
│   ├── Player/
│   ├── Environment/
│   ├── Obstacles/
│   ├── Collectibles/
│   ├── UI/
│   ├── Game/
│   └── Managers/
│
├── Materials/
│
└── Settings/
```

The exact structure may evolve as the project grows.

---

# 🧩 Main Systems

The project is planned around several independent gameplay systems.

| System              | Purpose                             |
| ------------------- | ----------------------------------- |
| Player Controller   | Handles player movement             |
| Lane System         | Controls left/center/right movement |
| Jump System         | Handles jumping                     |
| Slide System        | Handles sliding                     |
| Obstacle System     | Controls hazards                    |
| Collectible System  | Handles coins/items                 |
| Score Manager       | Calculates score                    |
| Health System       | Manages player health               |
| Environment Manager | Controls endless environment        |
| Spawn System        | Handles obstacle/item placement     |
| Game Manager        | Controls game states                |
| UI Manager          | Controls menus and HUD              |
| Audio Manager       | Controls sound and music            |
| Difficulty Manager  | Increases game difficulty           |

---

# 🛠️ Technologies Used

* **Unity**
* **C#**
* **Unity Physics**
* **Unity Animator**
* **Unity UI**
* **Unity Input System**
* **Git**
* **GitHub**

Additional Unity packages may be added as development progresses.

---

# 💻 Development Approach

The project is being developed incrementally.

The development process follows:

```text
Idea
 ↓
Project Setup
 ↓
Player Controller
 ↓
Movement
 ↓
Environment
 ↓
Obstacles
 ↓
Collectibles
 ↓
Scoring
 ↓
Health
 ↓
UI
 ↓
Game States
 ↓
Difficulty
 ↓
Audio
 ↓
Optimization
 ↓
Polishing
 ↓
Release
```

Each major feature will be developed, tested, and committed separately.

---

# 📌 Development Roadmap

## Phase 1 — Project Setup

* [x] Create Unity project
* [x] Configure project settings
* [x] Create folder structure
* [x] Set up Git repository
* [x] Connect project with GitHub

## Phase 2 — Player

* [ ] Import player character
* [ ] Create player controller
* [ ] Implement forward movement
* [ ] Implement lane switching
* [ ] Implement jumping
* [ ] Implement sliding
* [ ] Add player animations

## Phase 3 — Environment

* [ ] Create road/track
* [ ] Create environment sections
* [ ] Add trees and props
* [ ] Add background environment
* [ ] Implement endless environment
* [ ] Implement environment repositioning

## Phase 4 — Obstacles

* [ ] Create obstacle prefabs
* [ ] Implement obstacle spawning
* [ ] Implement lane-based obstacle placement
* [ ] Implement collision detection
* [ ] Add obstacle variations

## Phase 5 — Collectibles

* [ ] Create coin system
* [ ] Add collectible prefabs
* [ ] Implement collection detection
* [ ] Add collectible effects
* [ ] Connect collectibles to scoring

## Phase 6 — Gameplay Systems

* [ ] Implement score system
* [ ] Implement health system
* [ ] Implement distance tracking
* [ ] Implement game-over system
* [ ] Implement restart system
* [ ] Implement difficulty scaling

## Phase 7 — UI

* [ ] Create main menu
* [ ] Create gameplay HUD
* [ ] Add score display
* [ ] Add coin counter
* [ ] Add health display
* [ ] Create pause menu
* [ ] Create game-over screen

## Phase 8 — Audio & Effects

* [ ] Add background music
* [ ] Add sound effects
* [ ] Add particle effects
* [ ] Add environment effects
* [ ] Add camera effects

## Phase 9 — Optimization

* [ ] Profile CPU performance
* [ ] Profile GPU performance
* [ ] Optimize environment
* [ ] Optimize spawning
* [ ] Implement object pooling where appropriate
* [ ] Optimize physics
* [ ] Optimize rendering

## Phase 10 — Release

* [ ] Final gameplay testing
* [ ] Bug fixing
* [ ] Performance testing
* [ ] Build game
* [ ] Create release build
* [ ] Create GitHub release
* [ ] Document final version

---

# 🧪 Testing

Testing will be performed throughout development.

Areas being tested:

* Player movement
* Lane switching
* Jumping
* Sliding
* Collision detection
* Obstacle spawning
* Collectible detection
* Score calculation
* Health reduction
* Game-over conditions
* Environment looping
* UI functionality
* Performance
* Build stability

---

# 🚀 Future Improvements

Possible future features include:

* 🏆 High-score leaderboard
* 🎯 Missions and challenges
* 🎁 Daily rewards
* 🧍 Multiple characters
* 👕 Character customization
* 🛹 Different movement abilities
* ⚡ More power-ups
* 🌎 Multiple environments
* 🌙 Day/night cycle
* 🌧️ Weather system
* 🤖 Enemy characters
* 📱 Mobile controls
* 🎮 Controller support
* 🔊 Advanced audio system
* ✨ Advanced VFX
* 📊 Analytics
* ☁️ Cloud save system

---

# 📸 Screenshots & Gameplay

Screenshots and gameplay videos will be added as development progresses.

### Gameplay

> Coming soon...

### Screenshots

> Coming soon...

---

# 📦 Releases

Development builds and milestone releases will be published through GitHub Releases.

### Current Version

**v0.1.0 — Development**

Status: 🚧 In Development

---

# 📝 Development Log

Development progress will be documented through Git commits and GitHub releases.

Each major milestone may include:

* New gameplay systems
* New assets
* New mechanics
* Bug fixes
* Performance improvements
* UI improvements
* Gameplay balancing

---

# 🔐 License

This project is intended primarily for **educational and portfolio purposes**.

All third-party assets, libraries, trademarks, and intellectual property remain the property of their respective owners.

This project is not affiliated with or endorsed by the creators of Subway Surfers.

---

# 👨‍💻 Developer

**Azaf Games**

Game Development • Unity • C# • 3D Game Development

---

# ⭐ Project Status

🚧 **Active Development**

This project is being developed from scratch as part of my journey to learn and improve my skills in:

* Unity
* C#
* Game Programming
* 3D Game Development
* Gameplay Systems
* Game Optimization
* Git & GitHub

More features, improvements, and development updates will be added as the project progresses.

---

## 🎮 Made with Unity & C#

**Build → Test → Improve → Repeat 🔁**
