---
title: "WestWorld: A Knowledge-Encoded Scalable Trajectory World Model for Diverse Robotic Systems"
collection: publications
permalink: /publication/2026-03-01-ICML-WestWorld
date: 2026-03-01
venue: "International Conference on Machine Learning (ICML)"
citation: "Wang, Y., Kong, J., Wei, S., Li, X., Lin, H., Zhao, H., Zhou, T., Gan, L., & Shao, H. (2026). WestWorld: A Knowledge-Encoded Scalable Trajectory World Model for Diverse Robotic Systems. International Conference on Machine Learning (ICML)."
header:
  teaser: publications/ICML-2026-westworld.png
authors: "**Yuchen Wang**<sup>*</sup>, Jiangtao Kong<sup>*</sup>, Sizhe Wei, Xiaochang Li, Haohong Lin, Hongjue Zhao, Tianyi Zhou, Lu Gan, and Huajie Shao."
paperurl: "https://arxiv.org/abs/2603.14392"
projecturl: "https://westworldrobot.github.io/"
codeurl: "https://github.com/511205787/WestWorld"
badge: "Spotlight (2.2%)"
abstract: >-
  Trajectory world models play a crucial role in robotic dynamics learning, planning, and control. While recent works have explored trajectory world models for diverse robotic systems, they struggle to scale to a large number of distinct system dynamics and overlook domain knowledge of physical structures. To address these limitations, we introduce WestWorld, a knowledge-encoded scalable trajectory world model for diverse robotic systems. To tackle the scalability challenge, we propose a novel system-aware Mixture-of-Experts (Sys-MoE) that dynamically combines and routes specialized experts for different robotic systems via a learnable system embedding. To further enhance zero-shot generalization, we incorporate domain knowledge of robot physical structures by introducing a structural embedding that aligns trajectory representations with morphological information. After pretraining on 89 complex environments spanning diverse morphologies across both simulation and real-world settings, WestWorld achieves significant improvements over competitive baselines in zero- and few-shot trajectory prediction. Additionally, it shows strong scalability across a wide range of robotic environments and significantly improves performance on downstream model-based control for different robots. Finally, we deploy our model on a real-world Unitree Go1, where it demonstrates stable locomotion performance. The code is available at https://github.com/511205787/WestWorld.
---
**Yuchen Wang**<sup>*</sup>, Jiangtao Kong<sup>*</sup>, Sizhe Wei, Xiaochang Li, Haohong Lin, Hongjue Zhao, Tianyi Zhou, Lu Gan, and Huajie Shao.

[Paper link](https://arxiv.org/abs/2603.14392)

[Project Link](https://westworldrobot.github.io/)

[Github Link](https://github.com/511205787/WestWorld)
