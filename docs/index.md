---
layout: page
title: Overview
---

---
This site complements the paper [Learning Purely Tactile In-Hand Manipulation with a Torque-Controlled Hand](https://arxiv.org/abs/2204.03698){:target="_blank"} by
[Leon Sievers\*](https://www.linkedin.com/in/leon-sievers/){:target="_blank"}, [Johannes Pitz\*](https://www.linkedin.com/in/johannes-pitz/){:target="_blank"} and [Berthold Bäuml](https://scholar.google.com/citations?hl=en&user=fjvpDsEAAAAJ){:target="_blank"}.

Here we are providing more information on the robotic hardware as well as the parameters used during training.

<p align="center">
<iframe width="746" height="420" src="https://www.youtube.com/embed/ilDlO94lm1g" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</p>

[comment]: ![Justin](/assets/imgs/index/cube_justin_new.jpg)

# Abstract

---
We show that a purely tactile dextrous in-hand manipulation task with continuous regrasping, requiring permanent force closure, can be learned from scratch and executed robustly on a torque-controlled humanoid robotic hand. The task is rotating a cube without dropping it, but in contrast to [OpenAI's seminal cube manipulation task](https://openai.com/blog/learning-dexterity/){:target="_blank"}, the palm faces downwards and no cameras but only the hand's position and torque sensing are used. Although the task seems simple, it combines for the first time all the challenges in execution as well as learning that are important for using in-hand manipulation in real-world applications. We efficiently train in a precisely modeled and identified rigid body simulation with off-policy deep reinforcement learning, significantly sped up by a domain adapted curriculum, leading to a moderate 600 CPU hours of training time. The resulting policy is robustly transferred to the real humanoid DLR Hand-II, e.g., reaching more than 46 full 2π rotations of the cube in a single run and allowing for disturbances like different cube sizes, hand orientation, or pulling a finger.
