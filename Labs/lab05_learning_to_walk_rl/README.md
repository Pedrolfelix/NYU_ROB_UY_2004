# Lab 05 — Learning to Walk (Reinforcement Learning)

> **ROB-UY 2004: Robotic Manipulation & Locomotion** | NYU Tandon School of Engineering

Training a neural locomotion policy for the Stanford Pupper v3 using Reinforcement Learning — from a naive velocity-tracking reward all the way to deploying the trained policy on the physical robot.

---

## 🎯 Objective

Design and tune a reward function that trains Pupper to walk naturally and efficiently using PPO (Proximal Policy Optimization). The policy is first trained in simulation using MuJoCo + JAX, then deployed on the real robot — exploring the **sim-to-real gap** firsthand.

---

## 🧠 Concepts Covered

- **Reinforcement Learning for locomotion:** Reward shaping, PPO, policy training
- **Reward function design:** Velocity tracking, effort minimization, stability, smoothness, foot contact
- **Simulation:** MuJoCo + JAX (MJX) with thousands of parallel environments
- **Domain Randomization:** Training robustness via randomized mass, friction, perturbations, and terrain
- **Sim-to-Real Transfer:** Deploying a simulation-trained policy on physical hardware

---

## 🔁 Training Pipeline

```
Define reward function
        ↓
Train policy in MuJoCo + JAX (Google Colab A100)
        ↓
Track experiments with Weights & Biases (W&B)
        ↓
Visualize policy in simulation
        ↓
Deploy on physical Pupper v3 via PS3 controller
```

---

## 📋 Steps

### Step 1 — Velocity Tracking
Implemented a naive reward using only linear and angular velocity tracking to get Pupper moving in a commanded direction.

> 📹 [Watch simulation video](https://drive.google.com/file/d/1XJ2CpuxLfjVNoxyXkR4URoKDgIGOSc5e/view?usp=sharing)

---

### Step 2 — Effort Conservation
Added an effort minimization term to the reward function, penalizing excessive motor torques and encouraging energy-efficient locomotion.

> 📹 [Watch simulation video](https://drive.google.com/file/d/1g3LjEPqA14Zjjj_AQVuBoBmgf6B6U6Ae/view?usp=sharing)

---

### Step 3 — Full Reward Tuning
Tuned the complete reward function with stability, smoothness, foot contact, and height terms to produce a natural gait. Trained for 300M+ environment steps.

> 📹 [Watch simulation video](https://drive.google.com/file/d/1yPTMgqQQQrcsEsHB189bVn5aVnThcebp/view?usp=sharing)

---

### Step 4 — Deployment on Physical Robot
Deployed the trained policy on the real Pupper v3 using a PS3 controller. Compared the professor's default policy against our trained policy on the physical robot.

> 📹 **Professor's default policy:** [Watch video](https://drive.google.com/file/d/15rpvFwNysaC-50hpsVD0jp7ax3FhmPW8/view?usp=sharing)  
> 📹 **Our trained policy:** [Watch video](https://drive.google.com/file/d/1Tl648Y8R12prW5bXSwT24XGWYWDsiXUc/view?usp=sharing)

---

## 🛠️ Tech Stack

| Tool | Role |
|------|------|
| **MuJoCo + JAX (MJX)** | Physics simulation with GPU-accelerated parallel environments |
| **PPO** | Proximal Policy Optimization for policy training |
| **Google Colab (A100)** | Cloud GPU training environment |
| **Weights & Biases** | Experiment tracking and policy visualization |
| **Python** | Core implementation |
| **Stanford Pupper v3** | Physical robot for real-world deployment |

---

## 📂 Structure

```
lab05_learning_to_walk_rl/
├── step1/
│   └── step1.ipynb       ← velocity tracking policy
├── step2/
│   └── step2.ipynb       ← effort conservation policy
├── step3/
│   └── step3.ipynb       ← full reward tuning policy
└── README.md
```

---

## 👤 Author

**Pedro Felix** | Electrical Engineering — NYU Tandon School of Engineering  
[GitHub](https://github.com/Pedrolfelix)
