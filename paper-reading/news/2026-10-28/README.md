# 2026-10-28 Paper Reading

对应[当日日报](../../../news/2026-10-28.md)。本次精读 5 篇：日报「今日必读」4 篇与雷达最高分 1 篇；均完成全文提取、图表视觉审查、grounding、八项笔记 lint、质量/可读性审查与正式保存。

> **来源检查不完整：** 本次运行时 arXiv 最新公告批次为 2026-10-28，实际只覆盖到北京时间 10-28 01:59；10-28 02:00–23:59 的投稿尚未公告，因此当日可行窗口只有约两小时。下列精读均来自该窗口与 48 小时补充窗口，不能据此断言 10-28 全天没有其他重要工作。

## [ThinkWorld: World Imagination Reinforces Chain-of-Dynamics Reasoning](thinkworld/thinkworld.md)

标识：[arXiv:2610.37666v1](https://arxiv.org/abs/2610.37666)；短 slug：`thinkworld`；[bundle 入口](thinkworld/thinkworld.md)。

用共享离散运动 token 链表示动作，再用冻结 DINO 特征空间中的想象未来与真实未来之差做 GRPO 奖励；部署时删除推理路径。

代表图：[page_004_fig_figure_2_review.png](thinkworld/images/page_004_fig_figure_2_review.png)，为方法/管线总览图。

**笔记已完成**（6 图 materialized / 0 placeholder；Grounding Lint、八项 Final Note Lint、Final Quality Review、Final Readability Review 通过；原保存脚本成功，正式正文与全部图片 SHA-256 匹配）。

正文 SHA-256：`b77618e2066ccf1ace3cc1916d09800b6ae8b529ed9158e90571e740a888c0d1`。

## [Pushing Dexterity and Safety for In-Hand Object Pose Reaching That Works Remarkably Well](dexsafe/dexsafe.md)

标识：[arXiv:2610.37652v1](https://arxiv.org/abs/2610.37652)；短 slug：`dexsafe`；[bundle 入口](dexsafe/dexsafe.md)。

用生成抓取数据集定义目标与 reset，经特权教师-状态/深度学生蒸馏，再在冻结策略上学残差安全过滤器；4,800 个真机目标验证到达与掉落权衡。

代表图：[page_005_fig_fig_4_review.png](dexsafe/images/page_005_fig_fig_4_review.png)，为方法/管线总览图。

**笔记已完成**（4 图 materialized / 0 placeholder；Grounding Lint、八项 Final Note Lint、Final Quality Review、Final Readability Review 通过；原保存脚本成功，正式正文与全部图片 SHA-256 匹配）。

正文 SHA-256：`dd62acf64438bead2578d9059f8bc7f9e1f5eee8446ea06b5195300cc1f82929`。

## [World Dreamer v5-lite: A Multi-Robot World Action Model with One Dreamer](worlddreamer/worlddreamer.md)

标识：[arXiv:2610.37518v1](https://arxiv.org/abs/2610.37518)；短 slug：`worlddreamer`；[bundle 入口](worlddreamer/worlddreamer.md)。

把多相机特征按几何写入固定大小的三平面共享世界状态，每机器人保留独立动作流，仅通过姿态感知查询交互协调。

代表图：[page_002_fig_figure_1_review.png](worlddreamer/images/page_002_fig_figure_1_review.png)，为方法/管线总览图。

**笔记已完成**（4 图 materialized / 0 placeholder；Grounding Lint、八项 Final Note Lint、Final Quality Review、Final Readability Review 通过；原保存脚本成功，正式正文与全部图片 SHA-256 匹配）。

正文 SHA-256：`d08e68eb7c68fb265c6c9791b7069d234421bae8dab3027ec37d7da972645a18`。

## [Learning Visuomotor Quadrotor Flight Through Dynamic Narrow Gaps via Differentiable Simulation](quadrotor/quadrotor.md)

标识：[arXiv:2610.37557v1](https://arxiv.org/abs/2610.37557)；短 slug：`quadrotor`；[bundle 入口](quadrotor/quadrotor.md)。

用时变缝隙平面的符号距离门控居中、对齐与碰撞代价，经可微四旋翼动力学做 BPTT，从随机初始化直接训练视觉-惯性穿越策略。

代表图：[page_004_fig_figure_3_review.png](quadrotor/images/page_004_fig_figure_3_review.png)，为方法/管线总览图。

**笔记已完成**（5 图 materialized / 0 placeholder；Grounding Lint、八项 Final Note Lint、Final Quality Review、Final Readability Review 通过；原保存脚本成功，正式正文与全部图片 SHA-256 匹配）。

正文 SHA-256：`b2f1e7ad0af5fcdd0d48918e294923b29945db5d4537c4c6643b5f498a88f6bb`。

## [TAPESTRY: A Single Backbone for Video Generation and Robot Control](tapestry/tapestry.md)

标识：[arXiv:2610.36823v1](https://arxiv.org/abs/2610.36823)；短 slug：`tapestry`；[bundle 入口](tapestry/tapestry.md)。

把每个动作时间步当作视频 VAE 的单 patch token，复用预训练视频扩散 DiT；零终端 SNR 支持单步 DDIM，动作块 84 ms、9 GB 显存。

代表图：[page_003_fig_figure_1.png](tapestry/images/page_003_fig_figure_1.png)，为方法/管线总览图。

**笔记已完成**（4 图 materialized / 0 placeholder；Grounding Lint、八项 Final Note Lint、Final Quality Review、Final Readability Review 通过；原保存脚本成功，正式正文与全部图片 SHA-256 匹配）。

正文 SHA-256：`646af8e6d99a245c4b0e4173632392a3f7a6a01f1df4b94a887e58bdb75a92eb`。

共 5 篇、23 张图片。本次没有执行模型训练、推理或机器人实验。来源检查缺口与各篇实际提交时间见日报。
