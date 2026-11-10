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

### 基于 π0.5 的 SO-101 双臂 VLA 后训练与真实机器人部署

**技术栈：** LeRobot、π0.5、Flow Matching、PyTorch、FSDP2、Behavior Cloning、DAgger、RECAP、SO-101

**项目链接：** [GitHub](https://github.com/MrR0922/pi05-so101-bimanual) · [Hugging Face](https://huggingface.co/TylerRen66/pi05-so101-bimanual-tube-storage)

- **场景搭建与数据集构建：** 搭建由两台 SO-101 Follower 和场景、左右腕部三路相机构成的试管收纳平台，以 30 Hz 采集 12 维绝对关节动作；构建并治理两套共 152 条、139,564 帧的 LeRobot 真机示范数据，完成异常轨迹修复、语言指令标注、完整性校验与数据溯源。数据集：[huggingface.co/datasets/TylerRen66/so101-bimanual-clean](https://huggingface.co/datasets/TylerRen66/so101-bimanual-clean)
- **多卡全参数训练：** 基于 `lerobot/pi05_base` 进行 Behavior Cloning / SFT，在 8×RTX 4090 上使用 FSDP2、BF16 与 gradient checkpointing 训练；为耦合解码器移植 `JointDecoderLayerPair`，修复 PaliGemma 共享权重的 DCP 恢复问题，并验证 checkpoint 保存与恢复。
- **DAgger 与 RECAP 后训练：** 围绕策略失效样本设计 DAgger 式数据采集与回灌流程；原型化 RECAP 视觉 critic、advantage conditioning、奖励/成功标注及在线 replay buffer，为后续真机在线优化建立接口。

### 基于 LingBot-VLA2 的 RoboTwin 双臂机器人操作策略后训练（进行中）

**技术栈：** LingBot-VLA2、RoboTwin、PyTorch、SFT、Behavior Cloning

- **VLA 模型适配方案：** 面向 RoboTwin 双臂机器人操作任务，研究 LingBot-VLA2 预训练模型的视觉观测、语言指令及动作输出接口，规划模型与仿真环境的适配流程。
- **监督后训练方案：** 基于 RoboTwin 官方示范数据，设计 SFT / Behavior Cloning 后训练流程，规划数据预处理、动作标签对齐及策略微调方案。
- **仿真评测设计：** 研究 RoboTwin 任务环境及评测协议，规划模型推理、机器人动作执行与任务成功率评估流程，为后续实验对比提供基础。

### 基于 ACT 的机器人抓取模仿学习

实现 Action Chunking with Transformers，以 CVAE 表征示教序列并生成平滑动作。通过遥操作采集 50+ 条任务示教，在已见物体和未见物体上评估策略泛化能力。

## 技术方向

- **机器人学习：** π0.5、Flow Matching、Behavior Cloning、DAgger、RECAP、ACT
- **具身智能：** VLA、开放词汇感知、机器人操作、Sim-to-Real
- **计算机视觉：** ViT、CLIP、DINO、CNN、Transformer、DDPM
- **平台工具：** LeRobot、PyTorch / FSDP2、MoveIt、Isaac Lab

## 荣誉与竞赛

- ICAN 人工智能挑战赛，全国二等奖（2025）
- 全国大学生电子设计竞赛 A 题，省二等奖（2025）
- RISC-V 创新创业大赛，全国三等奖（2025）

## 联系我

- Email：[tianle66666@gmail.com](mailto:tianle66666@gmail.com)
- GitHub：[github.com/MrR0922](https://github.com/MrR0922)
- 所在地：深圳，中国
