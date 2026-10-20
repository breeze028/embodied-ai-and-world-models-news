# 2026-10-19 Paper Reading

本日精读对应[日报](../../../news/2026-10-19.md)：四篇必读论文与雷达最高分 Fréchet Forcing。

共五篇笔记已完成，12 张图片 materialized / 5 处 placeholder；占位是图像审查的保留状态，正文分析与全文证据已完成。

## Learn the Task, Not the Schedule: Reducing Spurious Cross-Arm Coupling in Bimanual Imitation Learning

- 论文：[arXiv:2610.26507v1](https://arxiv.org/abs/2610.26507)
- 笔记：[ctr/ctr.md](ctr/ctr.md)
- 核心思想：约束保持的局部时序重组扩大双臂进度支持，减少偶然时间表捷径。
- 代表图：[ctr/images/page_005_fig_figure_1_review.png](ctr/images/page_005_fig_figure_1_review.png)（方法/管线总览，已通过身份和视觉审查）
- 状态：笔记已完成（2 图 materialized / 2 placeholder）。主表1未形成独立完整候选，表2候选未过视觉质量门；保留两处占位与正文核实数值。
- 质量：Grounding Lint、Final Note Lint（8 项）、Final Quality Review、Final Readability Review 全部通过。
- SHA-256：`cff0dc6bdb8466ba09ce23d279a93b8fb8c5d75788cbc2014901abdb84418719`；正式保存笔记与最后一次 lint 的字节完全一致，图片与已审查 SHA-256 一致。

## Vector-Quantized World Model: Latent Feedback Motion Planning for Robot Manipulation

- 论文：[arXiv:2610.25600v1](https://arxiv.org/abs/2610.25600)
- 笔记：[vq-wm/vq-wm.md](vq-wm/vq-wm.md)
- 核心思想：用控制器首次到达估计构造码本，在离散规划和连续反馈之间对齐可达性。
- 代表图：[vq-wm/images/page_004_fig_fig_2_review.png](vq-wm/images/page_004_fig_fig_2_review.png)（方法/管线总览，已通过身份和视觉审查）
- 状态：笔记已完成（3 图 materialized / 0 placeholder）。无占位。
- 质量：Grounding Lint、Final Note Lint（8 项）、Final Quality Review、Final Readability Review 全部通过。
- SHA-256：`1224773bfee37091ae4a2a5f57539218e05678e2c6767696a204fe3dee1d05cc`；正式保存笔记与最后一次 lint 的字节完全一致，图片与已审查 SHA-256 一致。

## TILDE: Teacher-in-the-Loop Distillation from Embodied Foundation Models

- 论文：[arXiv:2610.25376v1](https://arxiv.org/abs/2610.25376)
- 笔记：[tilde/tilde.md](tilde/tilde.md)
- 核心思想：让教师执行恢复，补齐学生错误状态之后的轨迹，再以分来源动作目标蒸馏。
- 代表图：[tilde/images/page_004_fig_figure_2_review.png](tilde/images/page_004_fig_figure_2_review.png)（方法/管线总览，已通过身份和视觉审查）
- 状态：笔记已完成（2 图 materialized / 1 placeholder）。表4候选实际为表3，身份不符已拒绝；保留恢复效率表占位及全文数值。
- 质量：Grounding Lint、Final Note Lint（8 项）、Final Quality Review、Final Readability Review 全部通过。
- SHA-256：`17fc7ba5e7204ed21c23cf65fe053bb2e93622fd070829e8b0d24f54d92395c6`；正式保存笔记与最后一次 lint 的字节完全一致，图片与已审查 SHA-256 一致。

## TrajWAM: An Efficient Trajectory-Guided World Action Model for Dynamic Robotic Manipulation

- 论文：[arXiv:2610.25763v1](https://arxiv.org/abs/2610.25763)
- 笔记：[trajwam/trajwam.md](trajwam/trajwam.md)
- 核心思想：掩码轨迹引导未来视频，分阶段蒸馏维持一步动作接口。
- 代表图：[trajwam/images/page_003_fig_fig_2_review.png](trajwam/images/page_003_fig_fig_2_review.png)（方法/管线总览，已通过身份和视觉审查）
- 状态：笔记已完成（3 图 materialized / 1 placeholder）。真机表II未取得独立完整候选，保留占位；图7一次几何修复后通过完整视觉审查。
- 质量：Grounding Lint、Final Note Lint（8 项）、Final Quality Review、Final Readability Review 全部通过。
- SHA-256：`5c2ec7e0b31fa089fe73386d3a263b54f7b9dd63b0f4fbf099a67f45b4ab14f8`；正式保存笔记与最后一次 lint 的字节完全一致，图片与已审查 SHA-256 一致。

## Frechet Forcing: Training Long-Horizon Streaming World Models from Short Clips

- 论文：[arXiv:2610.25666v1](https://arxiv.org/abs/2610.25666)
- 笔记：[frechet-forcing/frechet-forcing.md](frechet-forcing/frechet-forcing.md)
- 核心思想：对部署采样器自由rollout施加生成锚定、场景中心化及感知真实感约束。
- 代表图：[frechet-forcing/images/page_014_fig_figure_2_review.png](frechet-forcing/images/page_014_fig_figure_2_review.png)（已通过身份和视觉审查；主结果图，论文无方法总览图）
- 状态：笔记已完成（2 图 materialized / 1 placeholder）。算法1候选未过视觉质量门，保留占位；论文没有方法管线总览图，代表图改用主结果Figure 2并说明协议。
- 质量：Grounding Lint、Final Note Lint（8 项）、Final Quality Review、Final Readability Review 全部通过。
- SHA-256：`b938aa20330cfc1dd6ff67f619fa751d481984d14bc2bf7c9a1b13faaa3c1cd1`；正式保存笔记与最后一次 lint 的字节完全一致，图片与已审查 SHA-256 一致。

全文及图像核查不代表在本机复现模型训练、仿真基准或真机部署。来源覆盖边界详见日报；不因可访问官方页面而宣称已穷尽全天更新。
