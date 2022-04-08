---
permalink: /simulator
layout: page
title: Simulator
usemathjax: true
---

We are using [PyBullet](https://pybullet.org/){:target="_blank"} as our rigid body simulator.

### Simulator Configuration
#### Initial Learning

|earth_acceleration|9.81 $$\frac{\text{m}}{\text{s}^2}$$
|simulation_frequency|500 $$\text{Hz}$$
|network_frequency|10 $$\text{Hz}$$
|steps_before_gravity_onset|4
|friction_lateral_tip|0.9
|friction_lateral_others|0.09
|friction_lateral_tip_random|0.0
|friction_spinning|0.1
|cube_mass|0.05 $$\text{kg}$$
|cube_length|0.08 $$\text{m}$$
|cube_mass_random|0.005 $$\text{kg}$$
|cube_position_random|\[0.001, 0.001, 0.005\] $$\text{m}$$
|cube_rotation_random|\[0.01, 0.01, 0.1\] $$\text{rad}$$
|motor_noise_std|0.002 $$\text{rad}$$
|sticky_action_probability|0.1

#### Continue Learning

|friction_lateral_tip_random|0.1
|friction_spinning|0.1
|motor_noise_std|0.02 $$\text{rad}$$