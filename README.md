
# ε-Greedy Multi-Armed Bandit Simulation

This repository implements a multi-armed bandit simulation using the ε-greedy action-value method, a classic reinforcement learning problem.

## Features

- Simulates bandits with configurable numbers of arms.
- Implements an ε-greedy agent that balances exploration and exploitation.
- Tracks:
  - Average reward over time
  - Percentage of optimal actions selected
- Compares multiple ε values (0.1, 0.01, 0) and different numbers of arms (5, 10, 20).
- Generates plots of performance metrics, saved as `bandit_results.png`.

## Classes

### `NArmedBandit`
- Initializes `n` arms with true action values from `N(0,1)`.
- Provides rewards with Gaussian noise when arms are pulled.
- Identifies the optimal arm for evaluation.

### `EpsilonGreedyAgent`
- Selects actions using the ε-greedy strategy.
- Updates estimated action-values using incremental averages.

## Functions

- `run_simulation(n_arms, epsilons, n_tasks, n_steps)`: Runs multiple bandit tasks and computes metrics.
- `plot_results(avg_rewards, pct_optimal, epsilons, n_arms, ax1, ax2)`: Plots average rewards and % optimal actions over time.

