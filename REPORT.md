



### Unity Framework 

The code is written in PyTorch and Python 3.
This repository contains code built on top of the ml-agents from Unity [ Unity Agents ].

### Agent Training Code

This repository includes functional, well-documented, and organized code for training the agent.

Algorithm used for training: DQN with Neural Network for functional approxmation of action-value function.

#### Network architecture:

Input: vector (dimensions: 37)
Hidden Layer 1: Linear with 256 nodes + RELU
Hidden Layer 2: Linear with 128 nodes + RELU 
Output Layer: Linear with 4 nodes

##### Parameters

'gamma': 0.99,                 # discount factor for agent
'state_size': state_size,      # size of the state space
'action_size': action_size,    # size of the action space
'hidden_layers': [128, 64],    # hidden layer neurons
'brain_name' : brain_name,     # the brain name of the unity environment
'BUFFER_SIZE': int(1e5),       # replay buffer size
'BATCH_SIZE' : 64,             # minibatch size
'LR' : 5e-4,                   # learning rate
'TAU' : 1e-3,                  # for soft update of target parameters
'UPDATE_EVERY' : 4             # how often local and target network are updated

Administration:
'name': 'DQN+Parameter-Set-1', # Name of the parameter set
'environment': env,            # The environment object
'brain_name': brain_name,      # The brain name for the unity environment
'episodes': 600,               # number of episodes
'max_t': 5000,                 # maximum length of an episode
'state_size': state_size,      # size of the state space
'action_size': action_size,    # size of the action space
'hidden_layers': [128, 64],    # hidden layer neurons
'brain_name' : brain_name,     # the brain name of the unity environment
'BUFFER_SIZE': int(1e5),       # replay buffer size
'BATCH_SIZE' : 64,             # minibatch size

Optimization : Adam
e-greedy policy with Epsilon anealing Start: 1.
e-greedy policy with Epsilon anealing End: 0.01
Decay: 0.995
Discount factor: $\gamma$ 0.99
Soft-update ratio, $\tau$ 0.001
Replay buffer size 64

With the above hyperparameters, the average score of the last 100 consecutive episodes reached 13.0 after 330 episodes.


### Model Weights

The saved model weights of the successful agent are located in the file: xxxxx

### Learning Algorithm

The report clearly describes the learning algorithm, along with the chosen hyperparameters. It also describes the model architectures for any neural networks.

- Evaluate the state and action space.
- Establish baseline using a random action policy.
- Implement learning algorithm.
- Run experiments to measure agent performance.
- Select best performing agent and capture video of it navigating the environment.

### Agent Goal and Actions

The Agent code performs an episodic task and achieve a score which exceeds 13 after 100 consecutive episodes. The agent needs to select actions that help it to collect as many yellow bananas as possible and avoiding blue bananas.

The Agent code is capable of executing four possible discrete actions to help him solve the task:
0 — move forward.
1 — move backward.
2 — turn left.
3 — turn right.

### Interaction with the Environment 

The agent is rewarded with +1 for collecting a yellow banana, and a reward of -1 collecting a blue banana. 

### Evaluate State Space
37 dimensions which includes:
- agent’s velocity, 
- ray-based perception of objects around the agent’s forward direction. 
 
### Reward plot

The number of episodes needed to solve the environment: ##<br>
A plot of rewards per episode is included to show rewards received as the number of episodes goes over 100 : ##<br>

### Ideas for Future Work

- Concrete future ideas for improving the agent's performance could include to perform learning directly from pixels (e.g. images). The agent not be provided pre-processed information as it is nowe.g. ray-based representation of objects around it, but would have to extract relevant information from the images directly. 
- Apply the double DQN
- Apply the dueling DQN

## See also

[ Unity Agents ] https://github.com/Unity-Technologies/ml-agents
