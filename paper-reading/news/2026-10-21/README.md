# 2026-10-21 Paper Reading

本日精读对应[日报](../../../news/2026-10-21.md)：四篇必读论文与雷达最高分SceneRig。日报在22日凌晨补做，22日08:30补检后官方可访问列表/RSS仍停在21日批次，其他官方接口超时；下一批投稿覆盖仍未完成，已有本版不代表可以跳过后续补查。五篇已完成精读的正文和图片本轮未改动，已逐文件核对原保存SHA-256。

共五篇笔记已完成，17 张图片 materialized / 3 处 placeholder。占位保留图像质量边界，正文分析与相关全文证据已核验。

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

以上是论文全文与图像核查，不代表完成模型训练、仿真或真实机器人独立复现。动态机构和会议来源覆盖不完整，详见日报说明。
