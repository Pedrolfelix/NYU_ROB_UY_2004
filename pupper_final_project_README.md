# 🐾 Final Project — 3-Legged Pupper Locomotion via Reinforcement Learning

> **ROB-UY 2004: Robotic Manipulation & Locomotion** | NYU Tandon School of Engineering

Training a Stanford Pupper v3 quadruped robot to walk with only **3 functional legs** using Reinforcement Learning — adapting its gait in simulation after a simulated leg failure.

---

## 🎯 Problem Statement

Quadruped robots are designed to walk on 4 legs. What happens when one leg fails?

This project addresses the challenge of **fault-tolerant locomotion**: training a RL policy that enables the Pupper to maintain stable forward motion after losing the use of one leg — without any pre-programmed fallback gait.

---

## 🧠 Approach

### Simulation Environment
The Stanford Pupper v3 model was simulated using **MuJoCo** and/or **PyBullet**, providing realistic rigid-body physics for legged locomotion training.

### Reinforcement Learning
A policy was trained using RL to discover a novel 3-legged gait from scratch. The reward function was shaped to encourage:
- **Forward velocity** — the robot should move in the desired direction
- **Stability** — minimize body roll and pitch to avoid falling
- **Energy efficiency** — penalize excessive joint torques
- **Foot contact patterns** — encourage appropriate 3-leg ground contact sequences

### Gait Adaptation
Rather than hard-coding a tripod gait, the RL agent learned to redistribute weight and timing across the 3 remaining legs, discovering emergent locomotion strategies.

---

## 🛠️ Tech Stack

| Tool | Role |
|------|------|
| **MuJoCo** | Primary physics simulation environment |
| **PyBullet** | Alternative physics engine for validation |
| **ROS** | Robot middleware and communication |
| **NumPy** | Numerical computations and state processing |
| **Python** | Core implementation language |

**Robot:** Stanford Pupper v3 — open-source quadruped developed at Stanford University

---

## 📊 Results

The trained RL policy successfully enabled the Pupper to achieve stable forward locomotion on 3 legs in simulation.

<!-- Add your simulation video here -->
> 📹 Simulation video: *[link to video]*  
> 📊 Project presentation: *[link to slides]*

---

## 🚀 How to Run

```bash
git clone https://github.com/Pedrolfelix/NYU_ROB_UY_2004.git
cd NYU_ROB_UY_2004/final_project

# Install dependencies
pip install -r requirements.txt

# Run the trained policy in simulation
python run_policy.py
```

> ⚠️ Requires MuJoCo license and Python 3.8+. See `requirements.txt` for full dependencies.

---

## 📚 References

- Stanford Pupper v3: [stanfordstudentrobotics.org/pupper](https://stanfordstudentrobotics.org/pupper)
- Schulman et al., *Proximal Policy Optimization Algorithms*, 2017
- Hwangbo et al., *Learning Agile and Dynamic Motor Skills for Legged Robots*, Science Robotics 2019
- Kumar et al., *RMA: Rapid Motor Adaptation for Legged Robots*, RSS 2021

---

## 👤 Author

**Pedro Felix** | Electrical Engineering — NYU Tandon School of Engineering  
[GitHub](https://github.com/Pedrolfelix)
