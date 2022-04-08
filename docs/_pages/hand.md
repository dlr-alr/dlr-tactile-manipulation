---
permalink: /hand
layout: page
title: Hand
usemathjax: true
---

We use the [DLR Hand II](https://www.dlr.de/rm/en/Portaldata/52/Resources/Roboter_und_Systeme/Hand/icra2001next.pdf){:target="_blank"}.

![Hand](./assets/imgs/hand/hand_size_small.png)

||$$q_1$$|$$q_2$$|$$q_3$$|
$$\Theta_{\text{min}}$$|$$-30^{\circ}$$|$$-20^{\circ}$$|$$-10^{\circ}$$
$$\Theta_{\text{max}}$$|$$30^{\circ}$$|$$86^{\circ}$$|$$105^{\circ}$$
$$\Theta_{\text{lower}}$$|$$-30^{\circ}$$|$$-10^{\circ}$$|$$-5^{\circ}$$
$$\Theta_{\text{upper}}$$|$$30^{\circ}$$|$$30^{\circ}$$|$$30^{\circ}$$
$$K_\text{P}$$|$$3.69 \frac{\text{Nm}}{\text{rad}}$$|$$3.69 \frac{\text{Nm}}{\text{rad}}$$|$$3.69 \frac{\text{Nm}}{\text{rad}}$$
$$K_\text{D}$$|$$0.25 \frac{\text{Nm s}}{\text{rad}}$$|$$0.25 \frac{\text{Nm s}}{\text{rad}}$$|$$0.25 \frac{\text{Nm s}}{\text{rad}}$$
$$K_\text{e}$$|$$25 \frac{\text{Nm}}{\text{rad}}$$|$$25 \frac{\text{Nm}}{\text{rad}}$$|$$25 \frac{\text{Nm}}{\text{rad}}$$
$$F_\text{static}$$|$$0.02\text{Nm}$$|$$0.02\text{Nm}$$|$$0.02\text{Nm}$$

Hand dimensions as well as the angles and their limits. $$\Theta_{\text{min}}$$ and $$\Theta_{\text{max}}$$ denote the physical limits of the real kinematics while $$\Theta_{\text{lower}}$$ and $$\Theta_{\text{upper}}$$ are used for the simulated hand as well as the scaling of the network output. The PD Impedance Controller is parameterized by $$K_{\text{P}}$$ and $$K_{\text{D}}$$. The parasitic stiffness is modeled by $$K_{\text{e}}$$. $$F_{\text{static}}$$ denotes the static friction force.