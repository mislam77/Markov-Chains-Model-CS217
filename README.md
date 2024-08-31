# 📈 Market Trend Prediction using Markov Chain

This project implements a **Markov Chain** model to predict stock market trends over a given number of weeks. The states considered are **Bull**, **Bear**, and **Stagnant**, and the transition between these states is probabilistic based on a given transition matrix.

## 📝 About the Project

In this project, we simulate the market trends using a Markov Chain model with three possible states:

1. **🐂 Bull Market** - A market condition where prices are rising.
2. **🐻 Bear Market** - A market condition where prices are falling.
3. **😐 Stagnant Market** - A market condition with little to no movement.

The model predicts the next state of the market based on the current state and the defined probabilities in the transition matrix.

### 🔄 Transition Matrix

The transition matrix defines the probability of moving from one state to another:

| Current State   | Bull (A) | Bear (B) | Stagnant (C) |
| --------------- | -------- | -------- | ------------- |
| **Bull (A)**    | 0.9      | 0.075    | 0.025         |
| **Bear (B)**    | 0.15     | 0.8      | 0.05          |
| **Stagnant (C)**| 0.25     | 0.25     | 0.5           |

### 📊 Simulation

The `market_trend` function simulates the market trend over a specified number of weeks, starting from a "Stagnant" state. It calculates the possible sequence of states and the probability of this sequence occurring.

### 🔍 Probability Calculation

The project also calculates the probability of starting in a "Stagnant" state and ending in a "Bear" state after 2 weeks over 10,000 iterations.

## 🚀 How to Run

1. **Clone the repository:**
   ```bash
   git clone https://github.com/yourusername/market-trend-markov-chain.git
   cd market-trend-markov-chain
   ```
2. **Install Dependencies:**

   Make sure you have **Python** and **NumPy** installed.

   Install NumPy if needed:

   ```bash
   pip install numpy
   ```
3. **Run the Simulation:**

   Execute the script to see the simulation results.

   ```bash
   python market_trend.py
   ```
4. **View the Results:**

   After running the script, check the console output to view the simulation results, including the sequence of states and the probability of ending in a "Bear" state.

## 📈 Example Output

When you run the simulation, you might see output similar to this:

```plaintext
Start state: Stagnant
Possible states: ['Stagnant', 'Bull', 'Bear']
End state after 2 weeks: Bear
Probability of the possible sequence of states: 0.01875

The probability of starting at state:'Stagnant' and ending at state:'Bear'= 27.45%
```
## 🛠️ Technologies Used

- **Python** 🐍
- **NumPy** for numerical operations
