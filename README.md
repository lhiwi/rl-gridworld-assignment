```md
# Reinforcement Learning – Gridworld Assignment

This repository contains the solution for an individual reinforcement learning assignment focused on understanding and implementing **planning** and **learning** algorithms in a small gridworld environment.

The assignment is implemented entirely in **Jupyter notebooks** and covers two core reinforcement learning methods applied to the same environment for comparison and understanding.

---

## Assignment Overview

The goal of this assignment is to model a **5×5 Gridworld** as a reinforcement learning problem and solve it using:

1. **Value Iteration** – a planning algorithm for fully observable Markov Decision Processes (MDPs)
2. **Q-Learning** – a model-free reinforcement learning algorithm based on trial-and-error interaction

Both exercises use the same environment to highlight the conceptual and practical differences between planning with a known model and learning from experience.

---

## Environment Description

- Grid size: **5 × 5**
- State space: each cell in the grid
- Action space: **Up, Down, Left, Right**
- Transition dynamics: deterministic, with boundary constraints
- Reward structure:
  - **+10** for reaching the goal state
  - **–1** for every other step
- Goal state: bottom-right cell **(4, 4)**
- Terminal state: the goal state ends the episode
- Discount factor:
  - Value Iteration: **γ = 0.9**
  - Q-Learning: **γ = 0.9**
- Learning rate (Q-Learning): **α = 0.5**

---

## Implemented Exercises

### 1. Value Iteration (MDP Planning)

The value iteration notebook formulates the gridworld as a fully observable MDP and iteratively applies the Bellman optimality update until convergence.  
After convergence, the optimal value function and the corresponding optimal policy are extracted and displayed in grid form.

**Notebook:**  
- `Value_Iteration.ipynb`

---

### 2. Q-Learning (Model-Free Reinforcement Learning)

The Q-learning notebook implements a tabular Q-learning agent that learns optimal action values through repeated interaction with the environment.  
The agent uses an epsilon-greedy policy for exploration and updates the Q-table using the standard temporal-difference update rule.

After training for a fixed number of episodes, the learned Q-values and the greedy policy induced by the Q-table are printed.

**Notebook:**  
- `Q_Learning.ipynb`

---

## Repository Structure

```

rl-gridworld-assignment/
├── notebooks/
│   ├── Value_Iteration.ipynb
│   └── Q_Learning.ipynb
├── requirements.txt
└── README.md

```


