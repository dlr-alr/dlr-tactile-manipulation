---
permalink: /learning
layout: page
title: Learning
usemathjax: true
---

### Reward Constants

|$$\lambda_{\text{spin}}$$|16
|$$\lambda_{\text{Z}}$$|100
|$$\lambda_{\text{plane}}$$|300
|$$\lambda_{\text{rot}}$$|50
|$$\lambda_{\text{proxy}}$$|25

### Learning Configuration
#### Initial Learning

|num_worker|12
|local_steps_per_update|25
|gradient_steps_per_update|100
|batch_size|256
|initial_no_update|2000
|initial_random_steps|10000
|curriculum_start|2e6
|curriculum_length|4e6
|num_layers|2
|hidden_size|512
|replay_size|1.5e5
|entropy_target|-6
|alpha_initial|0.2
|gamma|0.9
|lambda_weight_decay|2.5e-4
|max_episode_length|100
|num_observation_stack|5
|max_reward_rotation|1 $$\frac{\text{rad}}{\text{s}}$$

#### Continue Learning

|replay_size|1.5e6
|entropy_target|-8
|gamma|0.92
|lambda_weight_decay|2.5e-4
|max_episode_length|200
|num_observation_stack|5
|max_reward_rotation|0.7 $$\frac{\text{rad}}{\text{s}}$$