```md
# RL Gridworld Assignment (Value Iteration + Q-Learning)

This repository contains notebook-based implementations of two reinforcement learning algorithms in a **5x5 Gridworld**:

1) **Value Iteration** (MDP planning, fully observable)  
2) **Q-Learning** (model-free RL)

Both environments use:
- Actions: **Up, Down, Left, Right**
- Reward: **+10** for reaching the goal, **-1** for every other step
- Goal state: **(4, 4)** (bottom-right)
- Terminal: goal state ends the episode

---

## Repository Structure

```

.
├── notebooks/
│   ├── Value_Iteration.ipynb
│   └── Q_Learning.ipynb
├── src/                  # (optional) python scripts if included
├── requirements.txt
└── README.md

````

> Main deliverables are the `.ipynb` notebooks in `notebooks/`.

---

## Requirements

- Python 3.9+ (3.10/3.11 recommended)
- Git
- VS Code (recommended) with:
  - Python extension
  - Jupyter extension

---

## Setup (VS Code + Virtual Environment)

### 1) Clone the repository
```bash
git clone https://github.com/lhiwi/rl-gridworld-assignment.git
cd rl-gridworld-assignment
code .
````

### 2) Create and activate a virtual environment

**Windows PowerShell**

```bash
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

If activation is blocked:

```bash
Set-ExecutionPolicy -Scope CurrentUser RemoteSigned
.\.venv\Scripts\Activate.ps1
```

**macOS/Linux**

```bash
python3 -m venv .venv
source .venv/bin/activate
```

### 3) Install dependencies

```bash
python -m pip install --upgrade pip
pip install -r requirements.txt
```

If `requirements.txt` is missing, install manually:

```bash
pip install numpy ipykernel
```

### 4) Register the venv as a Jupyter kernel (recommended)

```bash
python -m ipykernel install --user --name rl-gridworld-venv --display-name "Python (rl-gridworld-venv)"
```

### 5) Select the kernel in VS Code

Open a notebook → top-right **Kernel** → choose:
**Python (rl-gridworld-venv)**

---

## Running the Notebooks

Open and run cells in order:

* `notebooks/Value_Iteration.ipynb`

  * Computes **optimal value function** (V^*)
  * Prints **optimal policy** (\pi^*) after convergence

* `notebooks/Q_Learning.ipynb`

  * Trains Q-learning for a **fixed number of episodes**
  * Prints the learned **Q-table** and greedy policy

---

## Algorithm Settings (As Required)

### Value Iteration

* Discount factor: **γ = 0.9**
* Convergence threshold: small tolerance (e.g., `1e-6`)
* Deterministic transitions with wall-bounce (stay in place if action goes off-grid)

### Q-Learning

* Learning rate: **α = 0.5**
* Discount factor: **γ = 0.9**
* Q-table initialized to **zeros**
* Epsilon-greedy exploration used for action selection (typical RL training setup)


---


```
```
