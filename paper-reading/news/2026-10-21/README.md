# 2026-10-21 Paper Reading

本日精读对应[日报](../../../news/2026-10-21.md)。22日上午通过官方月列表补齐后续投稿后，五篇必读为SuperMimic、COWBOY、PhysCanvas、UniWALM、SpatialDex；雷达最高分AdaDex已完成精读，另保留本期早先完成的SceneRig。

共七篇笔记已完成，23张图片materialized / 8处placeholder。新增两篇均通过Grounding Lint、Final Note Lint全部8项、Final Quality Review、Final Readability Review与正式保存SHA校验；原五篇正文与图片逐文件SHA-256保持不变。占位保留提取与裁剪的质量边界，相关全文结果已核实。机构/会议动态页面等来源仍有覆盖限制，详见日报。

## SuperMimic: Scaling Humanoid Whole-Body Control with One Differentiable World Model

- 论文：[arXiv:2610.28480v1](https://arxiv.org/abs/2610.28480)
- 笔记：[supermimic/supermimic.md](supermimic/supermimic.md)
- 核心思想：交替采集、拟合可微动力学和想象BPTT，用共享模型摊销动作库。
- 代表图：[supermimic/images/page_004_fig_figure_2_review.png](supermimic/images/page_004_fig_figure_2_review.png)（方法或平台总览，身份与视觉审查通过）
- 状态：笔记已完成（4 图 materialized / 0 placeholder）。无占位；训练集零失败与跨硬件预算、匹配PPO消融已分开。
- 质量：Grounding Lint、Final Note Lint（8项）、Final Quality Review、Final Readability Review全部通过。
- SHA-256：`b026cb55d74a4ef84182f05611df6b3c01c893872eeb5802eea740a13ac4ba33`；正式保存笔记与最后一次lint字节一致，图片与已审查SHA-256一致。

## Physical Canvas: A Vision Tactile World Model For Robot Policy Evaluation And Learning

- 论文：[arXiv:2610.28613v1](https://arxiv.org/abs/2610.28613)
- 笔记：[physcanvas/physcanvas.md](physcanvas/physcanvas.md)
- 核心思想：统一视觉触觉画布与三类一致性监督，使想象保留真实成功和失败。
- 代表图：[physcanvas/images/page_004_fig_figure_3_review.png](physcanvas/images/page_004_fig_figure_3_review.png)（方法或平台总览，身份与视觉审查通过）
- 状态：笔记已完成（2 图 materialized / 2 placeholder）。表3候选被质量门拒绝；图8一次修复仍缺任务标题，保留两处占位与全文数值。
- 质量：Grounding Lint、Final Note Lint（8项）、Final Quality Review、Final Readability Review全部通过。
- SHA-256：`40d675546582171f8ddfad93ca42a40b91c11eb4c5b318c58adc7a2065864f77`；正式保存笔记与最后一次lint字节一致，图片与已审查SHA-256一致。

## UniWALM: Unified World Action Language Model for Embodied Robot Control

- 论文：[arXiv:2610.28626v1](https://arxiv.org/abs/2610.28626)
- 笔记：[uniwalm/uniwalm.md](uniwalm/uniwalm.md)
- 核心思想：同步生成动作与语言，并跨步重消费文本，按任务区分视觉锚与完成门控。
- 代表图：[uniwalm/images/page_004_fig_figure_2_review.png](uniwalm/images/page_004_fig_figure_2_review.png)（方法或平台总览，身份与视觉审查通过）
- 状态：笔记已完成（3 图 materialized / 1 placeholder）。表5未取得独立完整候选，保留占位；图12一次几何修复后重新审查通过。
- 质量：Grounding Lint、Final Note Lint（8项）、Final Quality Review、Final Readability Review全部通过。
- SHA-256：`5bf01e1294912a5a1a20aa813d1acb5eb8da1bd3dedc2158490c9cc8abb85fb9`；正式保存笔记与最后一次lint字节一致，图片与已审查SHA-256一致。

## Learning Adaptable Dexterous Skills via Hybrid Dexterous Mimicking

- 论文：[arXiv:2610.28628v1](https://arxiv.org/abs/2610.28628)
- 笔记：[adadex/adadex.md](adadex/adadex.md)
- 核心思想：共享actor同时接受密集参考追踪与大扰动目标训练，兼顾技巧和适应。
- 代表图：[adadex/images/page_004_fig_figure_2_review.png](adadex/images/page_004_fig_figure_2_review.png)（方法或平台总览，身份与视觉审查通过）
- 状态：笔记已完成（4 图 materialized / 0 placeholder）。无占位；两主表一次几何修复后通过，平均进度与全部十目标成功分开。
- 质量：Grounding Lint、Final Note Lint（8项）、Final Quality Review、Final Readability Review全部通过。
- SHA-256：`8088030b71b2a324da6995c07b16fc4ead05b610233f0cd4d64dd2382bed90c5`；正式保存笔记与最后一次lint字节一致，图片与已审查SHA-256一致。

## SceneRig: An Agentic System for Simulation-Ready 3D Scene Reconstruction from Single Images

- 论文：[arXiv:2610.28585v1](https://arxiv.org/abs/2610.28585)
- 笔记：[scenerig/scenerig.md](scenerig/scenerig.md)
- 核心思想：用持久支撑图、有界位姿工具和物理接受门重建可用于机器人测试的场景。
- 代表图：[scenerig/images/page_004_fig_figure_2_review.png](scenerig/images/page_004_fig_figure_2_review.png)（方法或平台总览，身份与视觉审查通过）
- 状态：笔记已完成（4 图 materialized / 0 placeholder）。无占位；两表一次几何修复后通过，RGBD应用输入和回合一致率边界保留。
- 质量：Grounding Lint、Final Note Lint（8项）、Final Quality Review、Final Readability Review全部通过。
- SHA-256：`776f1f4b72bf7e71be0ef666ab8014c1410b82cdd6851fffd249766cd37c2e24`；正式保存笔记与最后一次lint字节一致，图片与已审查SHA-256一致。

## Reconstruction-Augmented Visuomotor Pre-Training of 3D-Grounded Bimanual Dexterity from RGB-Only Human Videos

- 论文：[arXiv:2610.29716v1](https://arxiv.org/abs/2610.29716)
- 笔记：[spatialdex/spatialdex.md](spatialdex/spatialdex.md)
- 核心思想：视频级尺度统一手与场景，双门控几何融合和腕条件手指生成。
- 代表图：[spatialdex/images/page_004_fig_fig_3_review.png](spatialdex/images/page_004_fig_fig_3_review.png)（方法总览，身份与300dpi视觉审查通过）
- 状态：笔记已完成（2图materialized / 3 placeholder）。三张罗马编号结果表未获得独立匹配候选，保留占位与已核实结果。
- 质量：Grounding Lint、Final Note Lint（8项）、Final Quality Review、Final Readability Review全部通过。
- SHA-256：`af5bc3990e15e89702a643489ff753c976b7f0a3f97b1f6a3df03827c3e5dcea`；正式保存笔记与最后一次lint字节一致，图片与审查SHA-256一致。

## COWBOY: A Scalable Sim-to-Real Framework for Learning Contextual Whole-Body Manipulation

- 论文：[arXiv:2610.28948v1](https://arxiv.org/abs/2610.28948)
- 笔记：[cowboy/cowboy.md](cowboy/cowboy.md)
- 核心思想：向量化WBC与兼容局部专家生成教师，部分点云DAgger蒸馏单一全身策略。
- 代表图：[cowboy/images/page_006_fig_figure_4_review_repair1.png](cowboy/images/page_006_fig_figure_4_review_repair1.png)（方法总览，身份与300dpi视觉审查通过）
- 状态：笔记已完成（4图materialized / 2 placeholder）。表3无独立候选；表4唯一修复后仍有外部表题碎片，保留两处占位。
- 质量：Grounding Lint、Final Note Lint（8项）、Final Quality Review、Final Readability Review全部通过。
- SHA-256：`e523abd2dadf660d5c4f0234ac91f9432c82048a38191005e136369aabcfd595`；正式保存笔记与最后一次lint字节一致，图片与审查SHA-256一致。

以上是论文全文与图像核查，不代表独立模型训练、仿真或真实机器人复现。
