# Epsilon-Greedy Algorithm: Multi-Armed Bandit Problem

OVERVIEW 

This project implements the ε-greedy algorithm to solve the Multi-Armed Bandit (MAB) problem, which is a classic reinforcement learning scenario. The primary challenge in this problem is decision-making under uncertainty, where an agent must balance exploration (trying new options) and exploitation (choosing the best-known option) to maximize cumulative rewards over time.

In this implementation, the agent chooses from multiple arms, each with an unknown reward distribution, and adjusts its strategy based on past experiences. The ε-greedy strategy allows the agent to explore the environment with probability ε (randomly select an arm) and exploit its knowledge with probability 1 - ε (select the arm with the highest estimated reward).

KEY FEATURES

Fixed ε-greedy: The value of ε remains fixed throughout the entire process, influencing how much the agent explores versus exploiting.
Reward Estimation: The agent estimates the reward of each arm using a running average, which is updated after each pull.
Multiple Simulations: The algorithm runs multiple simulations to gather statistics and evaluate the performance across different scenarios.
Regret Calculation: The algorithm calculates the regret, which measures the difference between the optimal strategy (always choosing the best arm) and the chosen actions by the agent.

ALGORITHM WORKFLOW

Initialization:
The algorithm initializes the estimated rewards (Q) and the count of arm pulls (N) to zero.
The true reward probabilities for each arm are provided (though the agent does not know them).

Action Selection:
At each step, the agent either explores (with probability ε) or exploits (with probability 1 - ε) based on the estimated rewards of the arms.
If the agent explores, it randomly selects an arm. If it exploits, it selects the arm with the highest estimated reward.

Reward Update:
After pulling an arm, the agent receives a reward (either 0 or 1) and updates its estimated value for that arm using incremental mean updating.

Simulation:
Multiple simulations are run to observe how the algorithm performs over time. The average results across all simulations are computed to evaluate the algorithm's behavior.

Metrics:
The average cumulative reward, average estimated rewards, and regret are calculated to assess the performance.
The difference between the true reward probabilities and the agent’s estimated rewards is also computed.

RESULTS

The results include the average estimated rewards for each arm, the number of times each arm is pulled, the cumulative reward over all simulations, and the regret (which indicates how well the agent performs compared to the optimal strategy).



