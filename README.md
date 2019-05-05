# DRLND-Project-Navigation

Draft submission to Udacity of project code towards the completion of the nano degree "Deep Reinforcement Learning" (DRL). Project #1 called "Navigation" trains an agent to navigate (and collect bananas!) in a large, square world.

### Introduction

For this project, you will train an agent to navigate (and collect bananas!) in a large, square world.  

A reward of +1 is provided for collecting a yellow banana, and a reward of -1 is provided for collecting a blue banana.  Thus, the goal of your agent is to collect as many yellow bananas as possible while avoiding blue bananas.  

The state space has 37 dimensions and contains the agent's velocity, along with ray-based perception of objects around agent's forward direction.  Given this information, the agent has to learn how to best select actions.  Four discrete actions are available, corresponding to:
- **`0`** - move forward.
- **`1`** - move backward.
- **`2`** - turn left.
- **`3`** - turn right.

The task is episodic, and in order to solve the environment, your agent must get an average score of +13 over 100 consecutive episodes.

### Repository structure

The code is structured as follows:

Navigation.ipynb: Notebook which trains the DRL Agent. 
agent.py: Python code for the a DQN agent class.
model.py: Python code for the a neural network used to approximate the action value function (A-V).
checkpoint.pth: Binary code containing the trained neural network weights.

### Dependencies

-- python 3.6
-- numpy: install with ‘pip install numpy’.
-- PyTorch: Installed using conda
-- ml-agents: Limited OpenAI Gym environment provided by Udacity

### Project Environment 

Describe the details (i.e., the state and action spaces, and when the environment is considered solved).

### Getting Started

Instructions for installing dependencies or downloading needed files.

1. Download the environment from one of the links below.  You need only select the environment that matches your operating system:
    - Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Linux.zip)
    - Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana.app.zip)
    - Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86.zip)
    - Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86_64.zip)
    


    (_For AWS_) If you'd like to train the agent on AWS (and have not [enabled a virtual screen](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Training-on-Amazon-Web-Service.md)), then please use [this link](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Linux_NoVis.zip) to obtain the environment.

2. Place the file in the DRLND GitHub repository, in the `p1_navigation/` folder, and unzip (or decompress) the file. 

### Instructions

A description of howto run the code in the repository, to train the agent. 

Follow the instructions in `Navigation.ipynb` to get started with training your own agent!  
The repository contains a jupyter notebook, which needs to be run within a conda environment [ conda ] . Once you have your notebook running with a web browser (e.g. Chrome) you can begin training the deep reinforcement agent, by execute cells in Navigation.ipynb notebook. 

### Output

After training, the notebook will show the average score per hundred episodes will be displayed.

### See Also

[ Windows version ] Check out [this link](https://support.microsoft.com/en-us/help/827218/how-to-determine-whether-a-computer-is-running-a-32-bit-version-or-64) if you need help with determining if your computer is running a 32-bit version or 64-bit version of the Windows operating system.
