# Udacity's Deep Reinforcement Learning Nanodegree: Continuous control project

This repository contains my solution to the second project in [Udacity's DRL nanodegree](https://www.udacity.com/course/deep-reinforcement-learning-nanodegree--nd893).

## The task

<img src=media/trained-agent.gif width=60%>

Meet the Reacher! An agent that was trained with [Deep Deterministic Policy Gradients (DDPG)](https://arxiv.org/pdf/1509.02971.pdf) to collect yellow bananas and avoid blue bananas. The environment is a modified version of [Unity ML-Agents' Reacher environment](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Learning-Environment-Examples.md#reacher).

A reward of `+0.1` is provided for each time step that the agent's hand is inside the goal (the greenish balloon that rotates around the agent's hand). The agent will learn to choose the approppriate actions at each time step which will lead to the maximum cumulative reward.

### State and action spaces, goal

- **The state space** is `33` dimensional and contains position, rotation, velocity, and angular velocities of the arm, as well as information on the goal's position and speed.

- **The action space** is `4` dimensional, the torques applicable to the arm's two joints. Every entry in the action vector is a number between -1 and 1.

- **Solution criteria**: the environment is considered as solved when the agent gets an average score of **+30 over 100 consecutive episodes**.

## Set-up

To run this code in your own machine, please follow the instructions [here](https://github.com/udacity/deep-reinforcement-learning#dependencies) and [here](https://github.com/udacity/deep-reinforcement-learning/tree/master/p2_continuous-control#getting-started).

Note: To develop in my machine, I used an updated version of Pytorch (`1.3.1`). You can reproduce the conda environment exactly following the instructions in `conda-requirements.txt`

## How to run

- **`Report.ipynb`** contains a detailed description of the implementation and allows you to visualize the performance of a trained agent.
- Running **`Continuous_Control.ipynb`** trains the agent from scratch
- The parameters needed to clone the trained agent can be found in `models/`. Refer to the report for more details.
- The agent is defined in `ddpg_agent.py`
- The actual actor-critic networks are defined in `ddpg_model.py`