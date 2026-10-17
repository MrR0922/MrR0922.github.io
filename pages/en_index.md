---
layout: page
home-title: Tyler Ren · Robot Learning Notes
description: Robot Learning · Embodied AI · VLA · Sim-to-Real
permalink: /en/index.html
langs: ["zh-Hans", "en"]
lang: "en"
cover: '/assets/img/hero-robotics-lab.png'
---

# Introduction

## About Me

I am **Tyler Ren (任天乐)**. My interests lie in **robot learning, embodied AI, and vision-language-action models (VLA)**. I build systems that enable robots to understand language, perceive their surroundings, and perform dexterous manipulation.

## Education

- **B.E. in Electronic Information Engineering, Shenzhen University**, 2023–2026
- **National University of Singapore (Suzhou) Research Institute**, 2026–present.

## Selected Projects

### VLA Post-Training and Sim-to-Real Transfer for the SO-101 Arm with GR00T N1

**Tech stack:** NVIDIA GR00T N1, Isaac Sim / Isaac Lab, LeRobot, NVIDIA Cosmos, PyTorch

- **VLA adaptation and post-training:** Adapted the pretrained GR00T N1 model to an SO-101 test-tube organization task in a simulated chemistry lab, converted Isaac Sim / Isaac Lab manipulation trajectories into LeRobot format, and completed model post-training.
- **Multi-source co-training:** Collected approximately 75 real-robot demonstrations through teleoperation, combined them with simulation trajectories for co-training, and augmented the training set with NVIDIA Cosmos-generated data to study the effects of different data sources on manipulation policies.
- **Visual domain randomization and Sim-to-Real:** Randomized lighting, object textures, scene backgrounds, and camera poses to diversify visual observations and reduce the visual distribution gap between simulation and the real world.
- **Real-robot deployment and evaluation:** Deployed the post-trained policy on a physical SO-101 arm and evaluated test-tube organization performance under different training-data configurations.

### LingBot-VLA2 Post-Training for Bimanual Manipulation in RoboTwin (In Progress)

**Tech stack:** LingBot-VLA2, RoboTwin, PyTorch, SFT, Behavior Cloning

- **VLA adaptation plan:** Studying the visual-observation, language-instruction, and action-output interfaces of LingBot-VLA2 for RoboTwin bimanual manipulation tasks and defining the model-to-simulator integration workflow.
- **Supervised post-training plan:** Designing an SFT / Behavior Cloning pipeline using official RoboTwin demonstrations, including data preprocessing, action-label alignment, and policy fine-tuning.
- **Simulation evaluation design:** Studying RoboTwin task environments and evaluation protocols, and planning the inference, robot-control, and task-success evaluation pipeline for subsequent experiments.

### ACT-Based Imitation Learning for Robotic Grasping

Implemented Action Chunking with Transformers, using a CVAE to encode demonstration sequences for smooth action generation. Collected more than 50 teleoperated demonstrations and evaluated generalization to seen and novel objects.

## Technical Focus

- **Robot Learning:** ACT, Diffusion Policy, PPO, imitation learning
- **Embodied AI:** VLA, open-vocabulary perception, manipulation, sim-to-real
- **Computer Vision:** ViT, CLIP, DINO, CNN, Transformer, DDPM
- **Platforms:** Isaac Lab / Isaac Sim, ROS / ROS2, MoveIt, LeRobot, PyTorch

## Honors

- ICAN AI Challenge — National Second Prize, 2025
- National College Student Electronic Design Competition — Provincial Second Prize, 2025
- RISC-V Innovation & Entrepreneurship Competition — National Third Prize, 2025

## Contact

- Email: [tianle66666@gmail.com](mailto:tianle66666@gmail.com)
- GitHub: [github.com/MrR0922](https://github.com/MrR0922)
- Location: Shenzhen, China
