---
layout: page
title: ICRA 23 (submitted)
usemathjax: true
---
# Dextrous Tactile In-Hand Manipulation Using a Modular Reinforcement Learning Architecture

This site complements our paper **Dextrous Tactile In-Hand Manipulation Using a Modular Reinforcement Learning Architecture** by
[Johannes Pitz](https://www.linkedin.com/in/leon-sievers/){:target="_blank"}, Lennart Röstel, [Johannes Pitz](https://www.linkedin.com/in/johannes-pitz/){:target="_blank"} and [Berthold Bäuml](https://scholar.google.com/citations?hl=en&user=fjvpDsEAAAAJ){:target="_blank"}.

![Sequence](../assets/imgs/icra23/sequence.png)

# Abstract

Dextrous in-hand manipulation with a multifingered robotic hand is a challenging task, esp. when performed
with the hand oriented upside down, demanding for permanent
force-closure, and when no external sensors are used. For the
task of reorienting an object to a given goal orientation (vs.
infinitely spinning it around an axis) the latter is an additional
fundamental challenge as the state of the object has to be
estimated all the time , e.g., to detect when the goal is reached.
In this paper we show that the task of reorienting a cube
to any of the 24 possible goal orientations in a π/2-raster
using the torque controlled DLR-Hand II is possible. The
task is learned from scratch in simulation using a modular
deep reinforcement learning architecture: the actual policy
has only a small observation time window of 0.5 s but gets
the cube state as an explicit input which is estimated via a
deep differentiable particle filter trained on data generated
by running the policy. In simulation we reach a success rate
of 92% while applying significant domain randomization. Via
zero-shot Sim2Real-transfer on the real robotic system, all 24
goal orientations can be reached with a high success rate.

---
## Learning Hyperparameters
Here we are providing more information on the parameters used during training.

### State Estimator
For state estimation, we employ the *Deep Differentiable Proposal Particle Filter* method with the following hyperparameters

|# particles (inference)|50
|# particles (training)|20
|hidden units (proposal & update models)|512
|hidden layers (proposal & update models)|2
|learning rate|1e-3
|training sequence length|100
|weight decay|1e-6
|dropout rate|0.1
|batchsize|320
|gradient clipping by value|5.0

### Policy
We use the [Soft Actor-Critic](https://arxiv.org/abs/1812.05905v2){:target="_blank"} Alogirthm with the following hyperparameters.

|replay buffer size|1.5e6
|# workers|80
|hidden layers|2
|hidden units|512

### Reward

|$$\lambda_{\text{pos}}$$|5.0e6
|$$\lambda_{\text{clip}}$$|10.0
|$$\lambda_{\text{drop}}$$|-5.0
|$$\lambda_{\text{succ}}$$|500.0
|$$\lambda_{\theta}$$|10.0
|$$\epsilon_{\theta}$$|0.3
|$$\lambda_{\text{pos}}''$$|1.0e5
|$$\lambda_{\phi}$$|200.0
|$$\lambda_{\text{clip}}''$$|20.0



---
## Simulation
The overall simulation setup in PyBullet is similar to our [previous work](icra22.md). 

