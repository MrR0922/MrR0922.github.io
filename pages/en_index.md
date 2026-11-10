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

### π0.5 Post-Training and Real-World Deployment for Bimanual SO-101

**Tech stack:** LeRobot, π0.5, PyTorch, FSDP2, Behavior Cloning, RECAP, SO-101

- **Bimanual system and data engineering:** Built a test-tube organization system with two SO-101 Followers and scene/dual-wrist cameras, recording 12-D absolute joint actions at 30 Hz. Curated two LeRobot datasets totaling 152 real-robot demonstrations and 139,564 frames, including trajectory repair, integrity validation, language annotation, and provenance tracking.
- **Full-parameter π0.5 post-training:** Fine-tuned the PyTorch `lerobot/pi05_base` policy with Behavior Cloning / SFT on 8×RTX 4090 GPUs using FSDP2, BF16, and gradient checkpointing, and validated distributed checkpoint save/resume.
- **Distributed training engineering:** Ported `JointDecoderLayerPair` as an FSDP wrapping unit for π0.5's coupled decoder, fixed PaliGemma shared-weight aliasing during DCP optimizer recovery, and introduced sequential per-rank loading to operate within a 128 GB host-memory limit.
- **Real-world inference and RECAP extension:** Implemented three-camera receding-horizon inference, safety limits, and bimanual mapping checks on a 12 GB RTX 4080. Prototyped a RECAP-style visual critic, advantage conditioning, reward/success annotations, and an online replay buffer for future online RL experiments.

### LingBot-VLA2 Post-Training for Bimanual Manipulation in RoboTwin (In Progress)

**Tech stack:** LingBot-VLA2, RoboTwin, PyTorch, SFT, Behavior Cloning

- **VLA adaptation plan:** Studying the visual-observation, language-instruction, and action-output interfaces of LingBot-VLA2 for RoboTwin bimanual manipulation tasks and defining the model-to-simulator integration workflow.
- **Supervised post-training plan:** Designing an SFT / Behavior Cloning pipeline using official RoboTwin demonstrations, including data preprocessing, action-label alignment, and policy fine-tuning.
- **Simulation evaluation design:** Studying RoboTwin task environments and evaluation protocols, and planning the inference, robot-control, and task-success evaluation pipeline for subsequent experiments.

### ACT-Based Imitation Learning for Robotic Grasping

Implemented Action Chunking with Transformers, using a CVAE to encode demonstration sequences for smooth action generation. Collected more than 50 teleoperated demonstrations and evaluated generalization to seen and novel objects.

## Technical Focus

- **Robot Learning:** π0.5, Behavior Cloning, RECAP, ACT, imitation learning
- **Embodied AI:** VLA, open-vocabulary perception, manipulation, sim-to-real
- **Computer Vision:** ViT, CLIP, DINO, CNN, Transformer, DDPM
- **Platforms:** LeRobot, PyTorch / FSDP2, ROS / ROS2, MoveIt, Isaac Lab

## Honors

- ICAN AI Challenge — National Second Prize, 2025
- National College Student Electronic Design Competition — Provincial Second Prize, 2025
- RISC-V Innovation & Entrepreneurship Competition — National Third Prize, 2025

## Contact

- Email: [tianle66666@gmail.com](mailto:tianle66666@gmail.com)
- GitHub: [github.com/MrR0922](https://github.com/MrR0922)
- Location: Shenzhen, China
