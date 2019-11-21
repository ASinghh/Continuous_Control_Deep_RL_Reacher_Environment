# Continuous_Control_Deep_RL_Reacher_Environment
## Introduction
The project is the second one of the three projects required for graduating [Udacity's Deep Reinforcement Learning Nano Degree](https://www.udacity.com/course/deep-reinforcement-learning-nanodegree--nd893). The project is to train the agent/agents using the Deep Deterministic Policy Gradient(DDPG) to solve the Unity ML Reacher environment. The base code for implementation is borrowed from [Udacity's implementation of DDPG](https://github.com/udacity/deep-reinforcement-learning/blob/master/ddpg-bipedal/DDPG.ipynb), which I have modified and finetuned to solve the environment under consideration. 


## Project details
### Environment 
The environment under consideration is on of the many [Unity ML-Agents Toolkit's](https://github.com/Unity-Technologies/ml-agents) game environments. These environments enable games and simulations to serve as environments for training intelligent agents. The environment is called the Reacher Environment. In this environment, a double-jointed arm can move to target locations.The goal of the agent is to maintain its position at the target location for as many time steps as possible. Two separate versions of the Unity environment are considered for the project,<br/>
    * Environment with a single agent.<br/>
    * Environment with 20 identical agents, each with its own copy of the environment.<br/>
 A graphic rendering of the environment looks like the following GIF. <br/> <br/> <br/> ![Reacher](gifs/reacher.gif)

#### State Space
The state space has 37 dimensions and contains the agent's velocity, along with ray-based perception of objects around the agent's forward direction. Given this information, the agent has to learn how to best select actions.

#### Action Space
Four discrete actions are available, corresponding to:
```   
       0 - move forward.
       1 - move backward.
       2 - turn left.
       3 - turn right.
```
#### Rewards
A reward of +1 is provided for collecting a yellow banana, and a reward of -1 is provided for collecting a blue banana.

### Completion Criteria
Based on the instructions provided in the study material, in order to consider the environment solved, the agent must get an average score of +13 over 100 consecutive episodes.

### Getting Started
1. Download the environment from one of the links below.  You need only select the environment that matches your operating system:
    - Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Linux.zip)
    - Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana.app.zip)
    - Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86.zip)
    - Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86_64.zip)

    (_For Windows users_) Check out [this link](https://support.microsoft.com/en-us/help/827218/how-to-determine-whether-a-computer-is-running-a-32-bit-version-or-64) if you need help with determining if your computer is running a 32-bit version or 64-bit version of the Windows operating system.

    (_For AWS_) If you'd like to train the agent on AWS (and have not [enabled a virtual screen](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Training-on-Amazon-Web-Service.md)), then please use [this link](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Linux_NoVis.zip) to obtain the environment.

2. Place the file in the DRLND GitHub repository, in the `p1_navigation/` folder, and unzip (or decompress) the file.

### Instructions
The file `dqn_agent.py` contains classes for creating DQN agents, Double DQN agents, Dueling DQN agents and Dueling Double DQN agents. It also contains a calss for creating Replay Buffers. The file `model.py` contains the Neural Network classes for creating Q Networks and Dueling Q Networks. These Network classes are used to define the four Agent classes in the file `dqn_agent.py`. To understand the implementation of training iterations, read through the `Navigation.ipynb` notebook.

### Report
The file `Report.pdf` contains information regarding the Learning Algorithms used for defining the agents, Plot of Rewards and Ideas for Future Work.

