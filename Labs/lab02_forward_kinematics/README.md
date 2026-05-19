# Lab 02 — Forward Kinematics

> **ROB-UY 2004: Robotic Manipulation & Locomotion** | NYU Tandon School of Engineering

Implementation of forward kinematics for the Stanford Pupper v3, computing the end-effector position from joint angles and detecting self-collisions in real time.

---

## 🎯 Objective

Given the joint angles of the robot, compute the position of each leg's **end-effector** (foot) relative to the robot's center using forward kinematics — and trigger an audio alert whenever a foot collides with another part of the robot's body.

---

## 🧠 Concepts Covered

- **Forward Kinematics:** Computing end-effector position from joint angles using transformation matrices
- **Homogeneous Transformation Matrices:** Chaining rotations and translations from the base frame to the tip of each leg
- **Self-Collision Detection:** Checking end-effector positions against the robot's body geometry in real time
- **Event-Based Response:** Triggering a sound alert when a collision is detected

---

## 📐 Kinematic Chain

```
Robot Center (Base Frame)
    └── Hip Joint
            └── Upper Leg (Thigh)
                    └── Lower Leg (Shin)
                            └── End-Effector (Foot) ← computed position
```

The forward kinematics chain is computed for each of the 4 legs independently, transforming from the base frame to the foot position using the Denavit-Hartenberg convention.

---

## 🛠️ Tech Stack

![Python](https://img.shields.io/badge/Python-3.10+-blue?logo=python&logoColor=white)
![PyBullet](https://img.shields.io/badge/PyBullet-physics_sim-green)
![NumPy](https://img.shields.io/badge/NumPy-scientific-013243?logo=numpy)

---

## 📊 Results

> 📹 **Demo video:** [Watch on Google Drive](https://drive.google.com/file/d/1Lu79_IPDkYy8w41SV68C6TTp6graWsC6/view?usp=sharing)

---

## 👤 Author

**Pedro Felix** | Electrical Engineering — NYU Tandon School of Engineering  
[GitHub](https://github.com/Pedrolfelix)
