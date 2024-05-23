Addis Ababa Institute of Technology  
School of Information Technology and Engineering  
Department of Artificial Intelligence  

# Reinforcement Learning

## Exercise I: Introduction to Reinforcement Learning

### Topics
- Value Iteration
- Policy Iteration
- Q-Learning
- Epsilon-Greedy Policy
- UCB Algorithm

### Problem Definition

#### Grid World Problem Definition

**Environment:**
The environment is a grid world represented by a 2D grid of size 𝑛×𝑚 (where n and m are the number of rows and columns in the grid).  
Each cell in the grid can be in one of three states: empty, obstacle, or goal.

**Agent:**
- The agent starts at a designated starting point in the grid, which is an empty cell.
- The agent's goal is to navigate to the goal cell in the grid.

**Actions:**
- The agent can take one of four actions at each step: move up, down, left, or right.
- The agent cannot move outside the grid or into cells containing obstacles.

**Rewards:**
- +10 for reaching the goal cell.
- -1 for each step taken (to encourage efficiency).
- -10 penalty for entering a cell containing an obstacle.

**Transition Dynamics:**
- The agent's actions deterministically move the agent in the specified direction, as long as the move is within the grid and not blocked by an obstacle.

**Objective:**
- The agent's objective is to find the shortest path from the starting point to the goal while minimizing the total cost (or maximizing the total reward).

**Starting Point and Goal:**
- Starting point: Cell (0, 0)
- Goal point: Cell (n-1, m-1)

**Obstacles:**
- A list of cell coordinates that contain obstacles.

**Initial Conditions:**
- The agent starts at the starting point with no prior knowledge of the environment.
- The agent's initial policy and state values can be set to default values (e.g., zero).

#### Single-State Multi-Armed Bandit Problem Definition

**Environment:**
- The environment is a single-state, multi-armed bandit problem with a single state.
- There are multiple arms (actions) available for the agent to choose from, typically denoted as K arms (e.g., 𝐾=10 arms).

**Agent:**
- The agent's goal is to maximize the total reward it accumulates over a fixed number of time steps by selecting the best arms to pull.
- The agent must balance exploration (trying new arms to find better rewards) and exploitation (choosing arms with known high rewards).

**Actions:**
- The agent can take one of 𝐾 actions at each time step, where each action corresponds to pulling one of the K arms.

**Rewards:**
- Each arm has a reward distribution that determines the reward received when the arm is pulled.
- The rewards are stochastic (random) and follow a specific distribution (e.g., normal distribution, Bernoulli distribution).
- The mean reward and variance of each arm's distribution may be unknown to the agent initially.

**Objective:**
- The agent's objective is to maximize the total cumulative reward it receives over a fixed number of time steps 𝑁.
- The agent must learn which arms provide the highest expected rewards while also exploring less-known arms.

**Initial Conditions:**
- The agent starts with no prior knowledge of the arms' reward distributions.
- The agent can keep track of the estimated mean reward for each arm based on its past observations.

**Evaluation:**
- At the end of the experiment, evaluate the agent's performance based on the total cumulative reward it received over 𝑁 time steps.
- Compare the agent's strategy with the optimal strategy (if known) and observe how closely the agent approached the optimal cumulative reward.

### Environment

[Gym of OpenAI](https://gymnasium.farama.org)  
Use FrozenLake-v1 of OpenAI Gym as a Gridworld environment

### Algorithm Implementation

#### Value Iteration:
- Apply value iteration-based reinforcement learning to both the grid world and single-state multi-armed bandit problems.

#### Policy Iteration:
- Use policy iteration-based reinforcement learning to solve both the grid world and single-state multi-armed bandit problems.

#### Q-Learning:
- Develop the Q-learning algorithm to determine the optimal action-value function in both the grid world and single-state multi-armed bandit problems.

#### Epsilon-Greedy Policy:
- Implement an epsilon-greedy policy to balance exploration and exploitation in the grid world and single-state multi-armed bandit environments.

#### UCB Algorithm:
- Apply the Upper Confidence Bound (UCB) algorithm to balance exploration and exploitation in the grid world and single-state multi-armed bandit problems.



ID: UGR/4709/12
