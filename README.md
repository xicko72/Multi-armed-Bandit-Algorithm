# ε-Greedy Multi-Armed Bandit Simulation

This repository simulates the ε-greedy action-value method for multi-armed bandits. It compares exploration rates across repeated tasks and plots average reward and the percentage of times the agent selects the best arm.

## Run it

Install `numpy`, `matplotlib` and Jupyter, then open `Multi_Armed_Bandit (1).ipynb` and run its first cell. The default experiment uses 2,000 tasks and 2,000 steps for each arm count, so it can take a while. For a quick check, reduce `N_TASKS` and `N_STEPS` near the bottom of the cell. The notebook saves `bandit_results.png` locally when it finishes; this generated image is not stored in the repository.

## Features

- Simulates bandits with configurable numbers of arms.
- Implements an ε-greedy agent that balances exploration and exploitation.
- Tracks average reward over time and the percentage of optimal actions selected.
- Compares ε values of 0.1, 0.01 and 0 across 5, 10 and 20 arms.
- Generates performance plots.

## Implementation

`NArmedBandit` samples true action values from N(0,1), adds Gaussian reward noise and identifies the optimal arm. `EpsilonGreedyAgent` selects actions and updates estimated values using incremental averages. `run_simulation` repeats tasks and aggregates metrics; `plot_results` visualises them.
