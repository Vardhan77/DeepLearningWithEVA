# EndGameProject

EngGameAssignment

# I. Project Overview

## Problem Statement

For this project a map of a city with the roads is provided as an image. Also a car is provided. My task is:

1. To go from any initialization to goal A

2. To reach goal in minimum number of time steps.

   In this project I have created a framework for Deep Reinforcement Learning.

Youtube Video Link:
https://youtu.be/kJgPeYgygp8

Highlights of various activities I have done in the project

- Used Twin Delayed Deep Deterministic (TD3) algorithm  for training
- Used Convolutional Neural Network(CNN) based DNN model
- For state space, mask is superimposed with a square car 
- Random sampling of actions initially to fill up the replay buffer initially
- Both Actor and Critic Models after each episode is stored
- Based on Analytics  on collected Metrics for evaluation and training episodes I have chosen appropriate model for testing

# II. Solution approach

![](https://i.imgur.com/li7BMPW.png)

In this project I have used Twin Delayed Deep Deterministic (TD3) algorithm (https://arxiv.org/pdf/1706.02275.pdf ) for training. 

 It uses Actor Critic approach where Actor function specifies action given the current state of the environments. Critic value function specifies a signal (TD Error) to criticize the actions made by the actor.
TD3 uses Actor and Critic principle. TD3 uses two Critic Networks and One Actor network 
TD3 uses experience replay where experience tuples (S,A,R,S`) are added to replay buffer and are randomly sampled from the replay buffer so that samples are not correlated.  
TD3 algorithm also uses separate target neural network for both Actor and Critic for each of the agent. 
There are six neural networks used in T3D
i.	Local network for Actor
ii.	Target network for Actor
iii.	Two networks for Critic
iv.	Two Target network for Critic
This algorithm uses time delay for updating Actor after a certain number of iterations. Also, Target Actor and Critic networks are updated periodically after certain number of iterations using Polyak averaging.
Name Twin in the algorithm is used because there are two Critics used.

### Actor Input: 

The Actor Network takes Input as one element tuple: 
80x80 numpy array representing  sand with superimposed square 



### Convolution Layer: 

(8, 3x3, Relu, BN), (12, 3x3, Relu, BN), (16, 3x3, stride=2, Relu, BN), (8, 1x1, Relu, BN), (12, 3x3, Relu, BN), (16, 3x3, Relu, BN), (AdaptiveAveragePool), Flatten, Dense layer of latent dim 16 to 8 to action_dim* 

### FC Layer:

There are three full connected layers. 
