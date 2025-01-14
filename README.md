# Vaccine-Development-with-Monte-Carlo-Policy-Evaluation

## Introduction
In the high-stakes field of vaccine development, decision-making plays a critical role in determining the financial viability and success of a project. As the CEO of a biotech company, you must evaluate the potential returns from a new vaccine project and decide whether to invest additional resources at various stages to improve the likelihood of success.

This project applies Monte Carlo Policy Evaluation to analyze two distinct investment strategies:
Always Invest: Invest $100,000 in each state to improve transition probabilities.
Never Invest: Proceed without additional investments and rely on default probabilities.
The Monte Carlo method provides an empirical way to compute the value function for each state under these policies by simulating numerous random trajectories of the vaccine development process.

## Problem Overview
The project is modeled as a Markov Decision Process (MDP) with:

States:
Phase 0 (state 0): Initial state.
Phase 1 with promising results (state 1).
Phase 1 with disappointing results (state 2).
Success (state 3): End state with a $10M reward for selling the patent.
Failure (state 4): Absorbing state.

Actions:
Invest: Spend $100,000 to increase the probability of transitioning to a favorable state.
Do Not Invest: Proceed without additional investments.

State Transitions:
Transition probabilities dictate the movement between states. These probabilities depend on the investment strategy.

Rewards and Costs:
A reward of $10M is obtained upon reaching the success state (state 3).
A cost of $100,000 is incurred for each investment.
Failure (state 4) results in no further rewards.

Discount Factor:
The discount factor (0.996) ensures that future rewards are appropriately weighted in the valuation process.

## Methodologies
Monte Carlo Policy Evaluation:
The Monte Carlo method simulates numerous episodes of the vaccine development process under the given policies.
For each episode, the return is calculated as the cumulative discounted reward for the entire trajectory.
The value function V(s) is computed as the average return from all episodes that pass through state s.

## Policy Definitions:

Always Invest Policy: In every state, an investment of $100,000 is made to improve transition probabilities.

Never Invest Policy: No investment is made, and transitions follow default probabilities.

Discounted Rewards: Rewards obtained in future states are discounted using the factor 𝛾=0.996, reflecting the time value of money.

Simulation: The process is simulated for a sufficient number of episodes to ensure convergence of the value estimates.

## Objective
The objective of this project is to compute the value functions for each state under the two policies:
Always Invest Policy
Never Invest Policy
These value functions provide critical insights into the financial viability of the vaccine development project and the impact of investment strategies on expected returns. By using the Monte Carlo method, the project offers a data-driven approach to evaluate long-term rewards under uncertainty, enabling informed decision-making in biotech project management.
