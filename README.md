DDPG: Deep Deterministic Policy Gradients
=========================================

A clean python implementation of an Agent for Reinforcement Learning with Continuous Control using Deep 
Deterministic Policy Gradients.

![](https://github.com/rmst/ddpg/raw/master/readme/ipend.gif?raw=true ) ![](https://github.com/rmst/ddpg/raw/master/readme/reacher.gif?raw=true) ![](https://github.com/rmst/ddpg/raw/master/readme/pend.gif?raw=true)
[![DDPG on TORCS](http://img.youtube.com/vi/Tb5gASEJIRM/0.jpg)](http://www.youtube.com/watch?v=Tb5gASEJIRM "Video Title")

# Overview:

DDPG is a reinforcement learning algorithm that uses deep neural networks to approximate policy and value functions. If you are interested in how the algorithm works in detail, you can read the original DDPG paper here

[Continuous control with deep reinforcement learning](https://arxiv.org/pdf/1509.02971v5.pdf)

The algorithm consists of two networks, an Actor and a Critic network, which approximate the policy and value functions of a reinforcement learning problem.

The name DDPG, or Deep Deterministic Policy Gradients, refers to how the networks are trained. The value function is trained with normal error and backpropagation, while the Actor network is trained with gradients found from the critic network. You can read the fascinating original paper on deterministic policy gradients here.

[Deterministic Policy Gradient Algorithms](http://www.jmlr.org/proceedings/papers/v32/silver14.pdf)

The DDPG algorithm is useful because, in very few lines of code (this project is approximately 150 lines excluding comments), you can learn a control algorithm for many different agents, including ones with complex configurations, continuous actions, and high dimensional state spaces (e.g. image data).
Even better, the same code can be used to train a humanoid robot, a drone, or a car, or any robotic configuration you can think of, Making this project highly reusable.

## Actor Network

The actor network approximates the policy function:

A(s) -> a

where s represents a state, and a represents an action.

## Critic Network

The critic network approximates the value function:

C(s, a) -> q

where s represents a state, a represents an action, and q represents the 
value of the given state action pair.

# Future:
Some ideas for future improvements are as follows:

* Support for convolutional neural networks in order to support high dimensional states (such as pixels from camera input)
* Support for Recurrent Networks for input data

Let me know of any other ideas you may have :)

# Thanks to:

This project is inspired by 
* The paper [Continuous control with deep reinforcement learning](https://arxiv.org/pdf/1509.02971v5.pdf) by Lillicrap et al.
* This python implementation, [DDPG](https://github.com/rmst/ddpg)
* Also Ben Lau's Article on [Using Keras and Deep Deterministic Policy Gradient to play TORCS](https://yanpanlau.github.io/2016/10/11/Torcs-Keras.html)