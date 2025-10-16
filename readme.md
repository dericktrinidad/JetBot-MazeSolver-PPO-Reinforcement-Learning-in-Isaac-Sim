# JetBot MazeSolver with Isaac Sim

JetBot MazeSolver is a reinforcement learning project that trains a JetBot robot to autonomously navigate and solve mazes inside NVIDIA Isaac Sim.
It uses a Proximal Policy Optimization (PPO) model to learn optimal movement strategies through trial and error.

### Overview

![Top Down  Maze View][./demos/mazeview.png]
This project explores how an agent can learn spatial awareness, wall avoidance, and goal-oriented navigation using simulated sensory inputs. The robot starts without any prior knowledge of the maze and gradually learns how to reach the goal faster and more efficiently.

### Video Demos

##### First Person
![1p Robot View][./demos/firstpersonview_compressed.gif]

##### Third Person
![3p Robot View](./demos/thirdpersonview_compressed.gif)

### Features

- PPO Reinforcement Model
Learns from reward feedback to reach the goal while minimizing collisions.

- GPS-Based Position Awareness
The robot receives continuous distance readings from its current position to the goal.

- 360° Lidar Sensor Input
Provides obstacle detection and spatial awareness to avoid walls and dead ends.


### Rules

1. The robot must reach the center of the maze to complete the objective.

2. The robot cannot touch any walls. A collision instantly resets it to the starting position.

3. Each training episode has a limited time budget. If the robot fails to reach the goal before time runs out, it resets and receives a penalty.

### Progress

This is an early-stage project, started just yesterday.
Current progress focuses on environment setup, reinforcement learning loops, and early model exploration.
Upcoming updates will include:

Improved reward shaping

Stay tuned for visuals showcasing the JetBot learning to conquer complex mazes.

### Requirements

- NVIDIA Isaac Sim v5.0.0

- Python 3.10+

- PyTorch for PPO implementation

- Gymnasium or custom environment interface

- Omniverse Kit utilities for simulation access