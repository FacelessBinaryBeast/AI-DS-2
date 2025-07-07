# Monty Hall Problem — Bayesian Network Implementation

## 🧩 Problem Statement

The **Monty Hall Problem** is a classic probability puzzle based on a game show scenario. Here's how it works:

1. A contestant is presented with **three closed doors**. Behind one is a **car** (the prize), behind the other two are **goats**.
2. The contestant picks one door.
3. The host (Monty Hall), who **knows what’s behind each door**, opens **one of the other two doors** revealing a goat.
4. The contestant is then given a choice: **stick with their original pick** or **switch to the remaining unopened door**.

**The paradox:** Intuitively, it seems like there's a 50-50 chance between switching or staying, but mathematically, switching **increases your chance of winning to 2/3**, while staying keeps it at 1/3.

---

## 🧠 Solution Approach: Bayesian Network

We modeled the Monty Hall problem using a **Bayesian Network** — a probabilistic graphical model that represents variables and their conditional dependencies.

### Key Components:
- **Bayesian Network Tool**: `pgmpy`
- **Graph Visualization**: `networkx` and `pylab`

### Nodes in the Network:
1. **Prize** – The door behind which the car is placed.
2. **Choice** – The door initially chosen by the player.
3. **Host** – The door revealed by the host (always a goat and not the chosen one).

### Flow of the Model:
1. Define the probability distributions:
   - Each door has equal probability of hiding the prize.
   - Player’s initial choice is random.
   - Host's choice depends on the player's pick and prize door.
2. Use `pgmpy` to model this as a Bayesian Network.
3. Infer the best decision (stay or switch) based on conditional probabilities.

---

## 🔍 What We Found

- When the contestant switches doors after the host reveals a goat, their **probability of winning the car increases to ~66.7%**.
- If the contestant stays with their original choice, their chance remains **only ~33.3%**.
- This reinforces the **counter-intuitive** result of the Monty Hall problem.

---

## 🖼️ Visual Output

A **Directed Acyclic Graph (DAG)** was generated to visualize the Bayesian model structure, showing dependencies between the player's choice, the prize, and the host's action.

---

## 🛠️ Tools Used

- Python 3
- `pgmpy` – for probabilistic modeling
- `networkx` and `matplotlib/pylab` – for graph visualization
- Jupyter Notebook – for interactive development

---

## ✅ Conclusion

This project successfully demonstrates how a Bayesian Network can be used to **simulate and understand the Monty Hall problem**. It not only confirms the optimal strategy (always switch!) but also gives a clear, visual explanation of the underlying probabilities.

---

## 📁 File

- `Amit_22104025_Exp1.ipynb`: Jupyter notebook containing the implementation, explanation, and visualization.
