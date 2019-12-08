## Continous-control
Udacity's Deep Reinforcement Learning Nanodegree Project Continuous Control: Training an agent with a double-jointed 
arm to reach a goal position.

## Problem Statement
The challenge is to train an agent with a double-jointed arm to move to target locations. A reward of +0.1 is provided 
for each step that the agent's hand is in the goal location. Thus, the goal of your agent is to maintain its position 
at the target location for as many time steps as possible.

The observation space consists of 33 variables corresponding to position, rotation, velocity, and angular velocities 
of the arm. Each action is a vector with four numbers, corresponding to torque applicable to two joints. Every entry in 
the action vector should be a number between -1 and 1.

## Dependencies:
Python Environment can be set up based on the following instructions:

Create (and activate) a new environment with Python 3.6.
conda create --name drlnd python=3.6
source activate drlnd

Download the Unity Environment Download the environment that matches your operation system, then place the file in the 
continuous-control-rl/ folder and unizip the file.

Version 1: 1 Agent:

Version 2: 20 Agents:

## Details of Repository:

ddpg_agent.py: Agent and ReplayBuffer classes with all required functions
model.py: Actor and Critc Network classes
Continous_Control.ipynb: As an alternative to the run.py script this Jupyter Notebook has a step-by-step structure. 
Here the learning algorithm is described in detail
checkpoint_actor.pth: Contains the weights of a successful Actor Network
checkpoint_critic.pth: Contains the weights of a successful Critic Network

## Solved the Second Version
The barrier for solving the second version of the environment is slightly different, to take into account the presence of many 
agents. In particular, the agents must get an average score of +30 (over 100 consecutive episodes, and over all agents). 

After each episode, we add up the rewards that each agent received (without discounting), to get a score for each agent. 
This yields 20 (potentially different) scores. We then take the average of these 20 scores.
This yields an average score for each episode (where the average is over all 20 agents).
The environment is considered solved, when the average (over 100 episodes) of those average scores is at least +30.
