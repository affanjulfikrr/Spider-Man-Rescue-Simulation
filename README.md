# 🕷️ Spider-Man Rescue Simulation

A 2D Computer Graphics simulation developed using **C++, OpenGL, and GLUT**, where Spider-Man rescues a falling citizen from a building.

The project demonstrates fundamental **Computer Graphics algorithms, 2D transformations, animation, physics, collision detection, and interactive controls** in a city environment.

---

## 🎯 Project Overview

The **Spider-Man Rescue Simulation** represents a dynamic city scene where a citizen falls from a building and Spider-Man attempts to rescue them.

The simulation includes:

* 🕷️ Spider-Man
* 👤 Falling citizen
* 🏢 Buildings
* 🌳 Trees
* 🚗 Vehicles
* 🛣️ Roads and footpaths
* ☁️ Clouds
* 🐦 Birds
* 💡 Street lamps
* ☀️ Day mode
* 🌙 Night mode
* 🎮 Interactive controls

The main game flow is:

```text
WAITING
   ↓
JUMPING
   ↓
RESCUE
   ↓
CARRY
   ↓
TALK
   ↓
WALK
   ↓
SUCCESS
```

If Spider-Man fails to reach the citizen:

```text
WAITING → JUMPING → FAILURE
```

---

## 🛠️ Technologies Used

* **C++**
* **OpenGL**
* **GLUT / FreeGLUT**
* **Computer Graphics**
* **2D Animation**
* **Collision Detection**

---

## 📐 Computer Graphics Algorithms

The project implements several fundamental graphics algorithms.

### 1. DDA Line Algorithm

**Function:** `ddaLine()`

Used for:

* Road markings
* Window lines
* Building details

Basic idea:

```text
x = x + xIncrement
y = y + yIncrement
```

---

### 2. Bresenham Line Algorithm

**Function:** `bresenhamLine()`

Used for:

* Spider-Man body parts
* Character arms
* Building edges

It uses mainly integer calculations and is efficient for drawing lines.

---

### 3. Midpoint Circle Algorithm

**Function:** `midpointCircle()`

Used for:

* Sun
* Moon
* Tree leaves
* Car wheels
* Human head

---

### 4. Bezier Curve

**Function:** `bezierCurve()`

Used for:

* Spider-Man's web

The Bezier curve creates a smooth curved line for the web.

---

### 5. Cohen-Sutherland Line Clipping

**Function:** `cohenSutherlandClip()`

Used for:

* Line clipping

It ensures that only the visible portion of a line is displayed.

---

## 🔄 2D Transformations

### Translation

**Function:** `translatePoint()`

Used for moving:

* Cars
* Clouds
* Birds
* Pedestrians

Formula:

```text
x' = x + dx
y' = y + dy
```

### Rotation

**Function:** `rotatePoint()`

Used for:

* Spider-Man swinging

Formula:

```text
x' = x cosθ - y sinθ
y' = x sinθ + y cosθ
```

### Scaling

**Function:** `scalePoint()`

Used for:

* Road reflection

The project uses negative Y scaling to create a reflection effect.

---

## ⚙️ Physics & Simulation

### Gravity

The citizen's falling movement is simulated using gravity.

```text
GRAVITY = 260.0
```

The falling velocity is updated continuously to create the falling effect.

### Collision Detection

**Function:** `collisionSpiderVictim()`

The simulation checks the distance between Spider-Man and the citizen.

If the distance becomes smaller than the defined threshold, the rescue is triggered.

```text
Distance < 26
       ↓
    RESCUE
```

---

## 🎬 Animation

The project contains several animated elements:

* 🚗 Moving cars
* ☁️ Moving clouds
* 🐦 Moving birds
* 🚶 Moving pedestrians
* 🕷️ Spider-Man swinging
* 👤 Falling citizen
* ☀️ Day/Night transition

The main update functions include:

```text
updateVictimFall()
updateSpiderSwing()
updateGame()
animateCars()
```

---

## 🌆 Scene Elements

The simulation creates a complete city environment containing:

* Buildings
* Roads
* Footpaths
* Trees
* Vehicles
* Street lamps
* Clouds
* Birds
* Spider-Man
* Citizen

Buildings create the city environment and provide the starting/ending positions required for the rescue scenario.

---

## 🌞 Day & 🌙 Night Mode

The simulation supports two lighting modes.

### Day Mode

* Bright sky
* Sun
* Normal city environment

### Night Mode

* Dark sky
* Moon
* Street lamps

---

## 🎮 Controls

| Key         | Action                |
| ----------- | --------------------- |
| `S`         | Save / Rescue Citizen |
| `D`         | Day Mode              |
| `N`         | Night Mode            |
| `P`         | Pause                 |
| `G`         | Show/Hide Grid        |
| `H`         | Show Help             |
| `R`         | Restart Game          |
| `Q` / `ESC` | Exit                  |

---

## 🖥️ Display & Game Loop

The main display function is:

```text
display()
```

Objects are drawn in the following order:

```text
Sky
 ↓
Buildings
 ↓
Trees
 ↓
Road
 ↓
Vehicles
 ↓
Street Lamps
 ↓
Citizen
 ↓
Spider-Man
 ↓
HUD
```

The timer updates the scene approximately every **30 ms** and refreshes the display.

---

## 📁 Project Structure

```text
Spider-Man-Rescue-Simulation/
│
├── README.md
│
├── src/
│   └── SpiderManRescue.cpp
│
├── screenshots/
│   ├── daytime.png
│   ├── nighttime.png
│   └── rescue.png
│
├── documentation/
│   └── Project-Report.pdf
│
└── LICENSE
```

> File and folder names can be changed according to the actual project structure.

---

## 🚀 How to Run

### Requirements

Install:

* C++
* OpenGL
* GLUT / FreeGLUT
* A compatible C++ IDE/compiler

### Steps

1. Clone the repository.

```bash
git clone https://github.com/your-username/Spider-Man-Rescue-Simulation.git
```

2. Open the project in your C++ IDE.

3. Make sure OpenGL and GLUT/FreeGLUT are properly configured.

4. Compile the source code.

5. Run the program.

---

## 📸 Screenshots

Add screenshots of the simulation here.

### Day Mode

![Day Mode](screenshots/daytime.png)

### Night Mode

![Night Mode](screenshots/nighttime.png)

### Rescue Scene

![Rescue Scene](screenshots/rescue.png)

---

## 👥 Team Members

* **Affan Julfiker**
* **Nusrat Jahan Choity**
* **Munjarin Khan**
* **Fawjia Jerin Kheya**

---

## 📚 Learning Outcomes

Through this project, we practiced:

* Fundamental Computer Graphics algorithms
* OpenGL and GLUT programming
* 2D transformations
* Animation techniques
* Collision detection
* Basic physics simulation
* Interactive keyboard controls
* Object-oriented/programming concepts
* Designing a complete 2D graphical environment

---

## 📄 License

This project is licensed under the **MIT License**.

See the [`LICENSE`](LICENSE) file for details.

---

## ⭐ Acknowledgement

This project was developed as an academic **Computer Graphics** project to demonstrate fundamental graphics algorithms and interactive 2D animation using OpenGL and GLUT.
