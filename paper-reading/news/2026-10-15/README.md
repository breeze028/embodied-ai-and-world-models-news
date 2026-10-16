# 2026-10-15 Paper Reading

本日精读对应 [科研日报](../../../news/2026-10-15.md)：今日必读 4 篇，外加雷达最高分 KinoGen。

全部完成全文与附录覆盖检查、Grounding Lint、八项 Final Note Lint、最终质量审查与可读性审查；13 张插图均逐张查看并核对 SHA-256，保留 5 处重要图表占位。

## 1. When Do Discrete Actions Make Good Continuous Controllers?

[arXiv:2610.20429](https://arxiv.org/abs/2610.20429) · [discrete-actions 笔记](discrete-actions/discrete-actions.md) · [bundle](discrete-actions/)。

动作量化、时间依赖与概率引导应分开比较。

代表图：[images/page_001_fig_figure_1_repair1.png](discrete-actions/images/page_001_fig_figure_1_repair1.png)（方法/管线总览，Visual Review 通过）。

状态：**笔记已完成**（2 图 materialized / 1 placeholder）。表 1 无可用独立图像。

Grounding Lint、Final Note Lint 8/8、Final Quality Review、Final Readability Review 均通过；正式笔记 SHA-256 与最后 lint 一致：`2aaff6a211e34e3a7c86a59ed371c796a39894998686871ed93aaae5bbd2ca8b`。

## 2. Physical Time as a Missing Dimension of Robot Policy Memory Dynamics

[arXiv:2610.20524](https://arxiv.org/abs/2610.20524) · [temporal-flow 笔记](temporal-flow/temporal-flow.md) · [bundle](temporal-flow/)。

测量时间差通过指数保留率驱动记忆更新。

代表图：[images/page_004_fig_figure_2_review.png](temporal-flow/images/page_004_fig_figure_2_review.png)（方法/管线总览，Visual Review 通过）。

状态：**笔记已完成**（4 图 materialized / 0 placeholder）。无保留占位。

Grounding Lint、Final Note Lint 8/8、Final Quality Review、Final Readability Review 均通过；正式笔记 SHA-256 与最后 lint 一致：`b0ddac43a3ae138c6f951622d10dbf3d6c743055cda7edb1cac7d0a913244a14`。

## 3. Hierarchical Residual Policy Learning for Real-World Mobile Manipulation with Sparse Human Guidance

[arXiv:2610.20607](https://arxiv.org/abs/2610.20607) · [hire-moma 笔记](hire-moma/hire-moma.md) · [bundle](hire-moma/)。

底盘先于手臂的条件残差结合专家价值对齐。

代表图：[images/page_003_fig_figure_2_review.png](hire-moma/images/page_003_fig_figure_2_review.png)（方法/管线总览，Visual Review 通过）。

状态：**笔记已完成**（2 图 materialized / 2 placeholder）。表 1 质量未达门槛；表 4 缺独立图像，关键值已转写。

Grounding Lint、Final Note Lint 8/8、Final Quality Review、Final Readability Review 均通过；正式笔记 SHA-256 与最后 lint 一致：`0cf5a24b58fac0591a70a4454c31a657947946261e59a376631cd09a4b652c8a`。

## 4. Graph-Reweighted Behavior Cloning with Human Interventions for Precise Robotic Manipulation

[arXiv:2610.20504](https://arxiv.org/abs/2610.20504) · [gr-bc 笔记](gr-bc/gr-bc.md) · [bundle](gr-bc/)。

轨迹图剩余路径为实际执行动作块赋权。

代表图：[images/page_002_fig_figure_1_review.png](gr-bc/images/page_002_fig_figure_1_review.png)（方法/管线总览，Visual Review 通过）。

状态：**笔记已完成**（3 图 materialized / 1 placeholder）。表 2 候选未通过视觉审查。

Grounding Lint、Final Note Lint 8/8、Final Quality Review、Final Readability Review 均通过；正式笔记 SHA-256 与最后 lint 一致：`acb93ef04204d2cacd231a6575bae8c70c935269d11caa367f67497b18d686a5`。

## 5. KinoGen: Customizable Humanoid Loco-Manipulation References via Kinematically Grounded Video Generation

[arXiv:2610.20552](https://arxiv.org/abs/2610.20552) · [kinogen 笔记](kinogen/kinogen.md) · [bundle](kinogen/)。

机器人渲染条件与分阶段运动学重建连接视频和控制参考。

代表图：[images/page_001_fig_fig_1_review.png](kinogen/images/page_001_fig_fig_1_review.png)（方法/管线总览，Visual Review 通过）。

状态：**笔记已完成**（2 图 materialized / 1 placeholder）。图 2 候选页码映射错误，拒绝错图；以合格图 1 为方法总览。

Grounding Lint、Final Note Lint 8/8、Final Quality Review、Final Readability Review 均通过；正式笔记 SHA-256 与最后 lint 一致：`249b45b9bae837b668922d057fba7bbb904f304676bdfac2177af9a4a243e55d`。
