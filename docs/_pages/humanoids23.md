---
layout: page
title: Submitted to Humanoids 2023
usemathjax: true
---
# Estimator-Coupled Reinforcement Learning for Robust Purely Tactile In-Hand Manipulation

This site complements our paper **Estimator-Coupled Reinforcement Learning for Robust Purely Tactile In-Hand Manipulation** submitted to the _International Conference on Humanoid Robots 2023_ by
[Lennart Röstel](https://scholar.google.com/citations?user=BPUd5h0AAAAJ&hl=en&oi=sra), [Johannes Pitz](https://www.linkedin.com/in/johannes-pitz/){:target="_blank"}, [Leon Sievers](https://www.linkedin.com/in/leon-sievers/){:target="_blank"} and [Berthold Bäuml](https://scholar.google.com/citations?hl=en&user=fjvpDsEAAAAJ){:target="_blank"}.

<p align="center">
<iframe width="746" height="420" src="https://www.youtube.com/embed/0VvSIvtHTq0" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
</p>

# Abstract

This paper identifies the culprits of naively combining learning-based controllers and state estimators for robotic in-hand manipulation. Specifically, we tackle the challenging task of purely tactile, goal-conditioned dextrous in-hand reorientation with the hand pointing downwards. Here, we observe that due to the limited sensing available, many control strategies that are feasible in simulation do not allow for accurate state estimation. Hence, separately training the controller and the estimator, and combining the two at test time, leads to poor performance. Our proposed solution to this problem involves training a control policy by reinforcement learning coupled with the state estimator in simulation. We show that this approach leads to more robust state estimation and overall higher performance on the task while maintaining an interpretability advantage over fully end-to-end learning approaches. Learning takes only 5h to 8h on a single GPU using IsaacSim. In simulation experiments with the DLR-Hand II and for four significantly different object shapes, we provide an in-depth analysis of the performance of our approach. Finally, we show the successful sim2real transfer with rotating the objects to all 24 possible π/2-orientations.