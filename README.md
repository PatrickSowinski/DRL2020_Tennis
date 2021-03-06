# DRL2020_Tennis

[//]: # (Image References)

[image1]: https://video.udacity-data.com/topher/2018/May/5af7955a_tennis/tennis.png "Tennis Env"
[image2]: https://user-images.githubusercontent.com/10624937/42386929-76f671f0-8106-11e8-9376-f17da2ae852e.png "Kernel"

![Trained Agents][image1]

This repository contains material related to Udacity's [Deep Reinforcement Learning Nanodegree](https://www.udacity.com/course/deep-reinforcement-learning-nanodegree--nd893) program.  

## Table of Contents

This repository contains the following files:

- Tennis_train.ipynb: The jupyter notebook used for training the agent that solves this environment. The notebook can also be used to visualize the trained agent.

- ddpg_agent.py: Source code for the Deep Deterministic Policy Gradient agent that solves the environment.

- model.py: Source code that defines the network architecture (layers, etc.) for the DDPG agent.

- checkpoint_*_solved.pth: Saved model weights (state dict) for the DDPG agent. (4 different files!)

- Tennis.app.zip: Compressed Unity environment that the agent runs in.

- python/: Folder used for installing dependencies

- Report.pdf: Report detailing how this project was completed.

## The Environment

The environment is implemented within Unity ML Agents. More info about these environments can be found [here](https://github.com/Unity-Technologies/ml-agents)

In this environment, two agents control rackets to bounce a ball over a net. If an agent hits the ball over the net, it receives a reward of +0.1. If an agent lets a ball hit the ground or hits the ball out of bounds, it receives a reward of -0.01. Thus, the goal of each agent is to keep the ball in play.

The observation space consists of 24 variables corresponding to the position and velocity of the ball and racket. Each agent receives its own, local observation. Two continuous actions are available, corresponding to movement toward (or away from) the net, and jumping.

The task is episodic, and in order to solve the environment, the agents must get an average score of +0.5 (over 100 consecutive episodes, after taking the maximum over both agents).

## Installation

To set up your python environment to run the code in this repository, follow the instructions below.

0. Do not use pyenv in combination with conda to manage your environment. If you want to use pyenv, you will have to set the environment to Python 3.6 there. Pyenv's global version setting will overwrite any changes you make in Anaconda.

1. Create (and activate) a new environment with Python 3.6.

- __Linux__ or __Mac__: 
```bash
conda create --name drlnd python=3.6
source activate drlnd
```
- __Windows__: 
```bash
conda create --name drlnd python=3.6 
activate drlnd
```

2. Follow the instructions in [this repository](https://github.com/openai/gym) to perform a minimal install of OpenAI gym. 
(Usually, you can ignore these extra steps:
- Next, install the **classic control** environment group by following the instructions [here](https://github.com/openai/gym#classic-control).
- Then, install the **box2d** environment group by following the instructions [here](https://github.com/openai/gym#box2d).
)

3. Clone the repository (if you haven't already!), and navigate to the `python/` folder.  Then, install several dependencies. (There is also a line in the training notebook to do this.)
```bash
git clone https://github.com/udacity/deep-reinforcement-learning.git
cd deep-reinforcement-learning/python
pip install .
```

4. Create an [IPython kernel](http://ipython.readthedocs.io/en/stable/install/kernel_install.html) for the `drlnd` environment.  
```bash
python -m ipykernel install --user --name drlnd --display-name "drlnd"
```

5. Before running code in a notebook, change the kernel to match the `drlnd` environment by using the drop-down `Kernel` menu. (May not need to do this, if you set an environment with pyenv.)

![Kernel][image2]

## Getting started

1. Unpack the Tennis.app.zip file.

2. Open the Tennis_train.ipynb notebook.

3. Run the cells in the notebook to start the unity environment and initialize the DDPG agent. You can train the agent, or you can skip to the end of the notebook to see a trained agent.

4. Close the environment from within the notebook after you're done.

