# Deep Reinforcement Learning - Collaboration and Competition

## Project Overview
In this environment, two agents control rackets to bounce a ball over a net. If an agent hits the ball over the net, it receives a reward of +0.1. If an agent lets a ball hit the ground or hits the ball out of bounds, it receives a reward of -0.01. Thus, the goal of each agent is to keep the ball in play.

The observation space consists of 8 variables corresponding to the position and velocity of the ball and racket. Each agent receives its own, local observation. Also, the environment returns 3 consecutive stacked observations, so the total state space size is 24 (for each agent). Two continuous actions are available, corresponding to movement toward (or away from) the net, and jumping.

The environment is considered solved when the agents get an average score of +0.5 (over 100 consecutive episodes, after taking the maximum over both agents). Specifically,
  * After each episode, we add up the rewards that each agent received (without discounting), to get a score for each agent. This yields 2 (potentially different) scores. We then take the maximum of these 2 scores.
  * This yields a single score for each episode.

The environment is considered solved, when the average (over 100 episodes) of those scores is at least +0.5.

## Getting Started
The following are the dependencies for this project:
  
  * Python 3.6 (installed using MiniConda in my case).
  * OpenAI gym (https://github.com/openai/gym) with the classic control (https://github.com/openai/gym#classic-control) and box2d (https://github.com/openai/gym#box2d) environments installed.
  * The python packages listed at https://github.com/udacity/deep-reinforcement-learning/blob/master/python/requirements.txt (can be installed using pip).
  * The dependencies specified at https://github.com/ShangtongZhang/DeepRL/blob/master/requirements.txt. On my setup, I found that torchvision, opencv-python and tensorboardX were required to be installed over-and-above what was already present. But please install the entire requirements.txt in case you face missing package issues.
  * The project Unity environment. In my case, I used the Linux environment. A copy of this is present within the submission itself. In case your environment is different please remove the existing Tennis_Linux folder, copy the appropriate zip to the folder containing Tennis.ipynb and extract it there.
  
## Instructions
All the code for the project is inside the Tennis.ipynb notebook. Stepping through the notebook should be sufficient to train the agent from scratch and reproduce my results. The only thing which might need to be changed (depending on the reviewer's environment) is the file path with which the Unity environment is initialized.

Also, the weights of the final model are provided as winning_model.bin within the submission. This was saved using the mechanism provided by the ShangtongZhang DeepRL code (agent.save(file_name)). The weights should be restorable using the corresponding load API (agent.load(file_name)). 
