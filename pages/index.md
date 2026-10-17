---
layout: page
home-title: Tyler Ren · Robot Learning Notes
description: 机器人学习 · 具身智能 · VLA · Sim-to-Real
permalink: /index.html
langs: ["zh-Hans", "en"]
lang: "zh-Hans"
cover: '/assets/img/hero-robotics-lab.png'
---

# 个人介绍

## 关于我

我是 **任天乐（Tyler Ren）**，研究兴趣集中在 **机器人学习、具身智能和视觉-语言-动作模型（VLA）**。我希望构建能够理解自然语言、感知环境并完成灵巧操作的机器人系统。

## 教育经历

- **深圳大学 · 电子信息工程学士**，2023–2026
- **新加坡国立大学苏州研究院**，2026–现在。

## 代表项目

### 基于 GR00T N1 的 SO-101 机械臂 VLA 后训练与 Sim-to-Real 迁移

**技术栈：** NVIDIA GR00T N1、Isaac Sim / Isaac Lab、LeRobot、NVIDIA Cosmos、PyTorch

- **VLA 模型适配与后训练：** 基于 GR00T N1 预训练模型，面向模拟化学实验中的试管收纳任务开展 SO-101 机械臂策略适配，将 Isaac Sim / Isaac Lab 仿真操作轨迹转换为 LeRobot 格式，完成模型后训练。
- **多源数据联合训练：** 通过遥操作采集约 75 条真实机器人示范轨迹，结合仿真数据开展 Co-training，并引入 NVIDIA Cosmos 生成数据扩充训练集，探索多源数据对机器人操作策略的影响。
- **视觉域随机化与 Sim-to-Real 优化：** 在仿真环境中对光照、物体纹理、场景背景及相机位姿进行随机化，增加视觉观测多样性，缓解仿真与真实环境之间的视觉分布差异。
- **真实机器人部署与评测：** 在 SO-101 实体机械臂上部署后训练策略，针对试管收纳任务开展真实环境测试，评估不同训练数据配置下的机器人操作表现。

### 基于 LingBot-VLA2 的 RoboTwin 双臂机器人操作策略后训练（进行中）

**技术栈：** LingBot-VLA2、RoboTwin、PyTorch、SFT、Behavior Cloning

- **VLA 模型适配方案：** 面向 RoboTwin 双臂机器人操作任务，研究 LingBot-VLA2 预训练模型的视觉观测、语言指令及动作输出接口，规划模型与仿真环境的适配流程。
- **监督后训练方案：** 基于 RoboTwin 官方示范数据，设计 SFT / Behavior Cloning 后训练流程，规划数据预处理、动作标签对齐及策略微调方案。
- **仿真评测设计：** 研究 RoboTwin 任务环境及评测协议，规划模型推理、机器人动作执行与任务成功率评估流程，为后续实验对比提供基础。

### 基于 ACT 的机器人抓取模仿学习

实现 Action Chunking with Transformers，以 CVAE 表征示教序列并生成平滑动作。通过遥操作采集 50+ 条任务示教，在已见物体和未见物体上评估策略泛化能力。

## 技术方向

- **机器人学习：** ACT、Diffusion Policy、PPO、Imitation Learning
- **具身智能：** VLA、开放词汇感知、机器人操作、Sim-to-Real
- **计算机视觉：** ViT、CLIP、DINO、CNN、Transformer、DDPM
- **平台工具：** Isaac Lab / Isaac Sim、ROS / ROS2、MoveIt、LeRobot、PyTorch

## 荣誉与竞赛

- ICAN 人工智能挑战赛，全国二等奖（2025）
- 全国大学生电子设计竞赛 A 题，省二等奖（2025）
- RISC-V 创新创业大赛，全国三等奖（2025）

## 联系我

- Email：[tianle66666@gmail.com](mailto:tianle66666@gmail.com)
- GitHub：[github.com/MrR0922](https://github.com/MrR0922)
- 所在地：深圳，中国
