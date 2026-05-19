# Lab 03 — Inverse Kinematics & Gait Implementation

> **ROB-UY 2004: Robotic Manipulation & Locomotion** | NYU Tandon School of Engineering

Implementation of inverse kinematics for the Stanford Pupper v3, computing the joint angles required to place each foot along a desired trajectory — and using it to drive a trot gait.

---

## 🎯 Objective

Given a desired **end-effector (foot) position** in 3D space, compute the joint angles needed to reach it using inverse kinematics. Apply this to generate a **trot gait**, where diagonal leg pairs move in sync to produce forward locomotion.

---

## 🧠 Concepts Covered

- **Inverse Kinematics:** Computing joint angles from a desired end-effector position
- **Jacobian / Geometric IK:** Solving the IK problem for a 3-DOF leg
- **Gait Generation:** Defining foot trajectories (swing + stance phases) for a trot gait
- **Trot Gait Pattern:** Diagonal leg pairs (FR+RL, FL+RR) moving in alternation

---

## 📐 Trot Gait Foot Trajectory

Each foot follows a cyclic path consisting of two phases:

- **Stance phase** (bottom, flat): foot on the ground, pushing the body forward
- **Swing phase** (top, triangular arc): foot lifted and swung forward to the next contact point

![Front-Right Foot Trot Gait Path](./trot_gait_path.jpeg)

*Front-Right foot trajectory in the X-Z plane. The triangular arc represents the swing phase and the flat bottom line represents the stance phase.*

---

## 🛠️ Tech Stack

![Python](https://img.shields.io/badge/Python-3.10+-blue?logo=python&logoColor=white)
![PyBullet](https://img.shields.io/badge/PyBullet-physics_sim-green)
![NumPy](https://img.shields.io/badge/NumPy-scientific-013243?logo=numpy)

---

## 📊 Results

### IK Validation
The plot below shows the computed end-effector X position (red dots) against the target trajectory (black line) — the near-perfect overlap confirms the accuracy of the IK implementation.

![IK Validation](./Ik_validation.jpeg)

### Simulation Videos
> 📹 **Demo video 1:** [Watch on Google Drive](https://drive.google.com/file/d/10TvyIyVuYEDk-ssEGEDlKnWEEpm_3CjO/view?usp=sharing)  
> 📹 **Demo video 2:** [Watch on Google Drive](https://drive.google.com/file/d/1GLI7ir4bdcU1CxHBNcFE_d04xc6VjxKf/view?usp=sharing)

---

## 👤 Author

**Pedro Felix** | Electrical Engineering — NYU Tandon School of Engineering  
[GitHub](https://github.com/Pedrolfelix)
