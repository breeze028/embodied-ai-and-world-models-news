# 2026-10-16 Paper Reading

本日精读对应[日报](../../../news/2026-10-16.md)：四篇必读论文与雷达最高分 CoDA。

共五篇笔记已完成，14 张图片 materialized / 4 处 placeholder；占位是图像审查的保留状态，正文分析与全文证据已完成。

## T2-z: Test-Time Optimization of Environment Latents for Robotic World Models

- 论文：[arXiv:2610.22364v1](https://arxiv.org/abs/2610.22364)
- 笔记：[t2-z/t2-z.md](t2-z/t2-z.md)
- 核心思想：用少量交互优化32维环境变量，让冻结世界模型在新环境验证候选动作。
- 代表图：[t2-z/images/page_004_fig_figure_3_review_repair1.png](t2-z/images/page_004_fig_figure_3_review_repair1.png)（方法/管线总览，已通过身份和视觉审查）
- 状态：笔记已完成（4 图 materialized / 0 placeholder）。无占位。
- 质量：Grounding Lint、Final Note Lint（8 项）、Final Quality Review、Final Readability Review 全部通过。
- SHA-256：`b2686d61e56568396ca8c77adc053bfff8a6e08401ca9dd54644da4151a3d5ed`；正式保存笔记与最后一次 lint 的字节完全一致，图片与已审查 SHA-256 一致。

## Spark-0: Scaling Spatially Aligned Tactile Pretraining for Robot Dexterous Manipulation

- 论文：[arXiv:2610.22342v1](https://arxiv.org/abs/2610.22342)
- 笔记：[spark-0/spark-0.md](spark-0/spark-0.md)
- 核心思想：通过空间接触和几何训练监督及缺失感知触觉融合，连接人类预训练与灵巧策略。
- 代表图：[spark-0/images/page_004_fig_figure_3_review.png](spark-0/images/page_004_fig_figure_3_review.png)（方法/管线总览，已通过身份和视觉审查）
- 状态：笔记已完成（2 图 materialized / 1 placeholder）。Table 3候选身份错误，保留真机表占位；正文数值依源文核对。
- 质量：Grounding Lint、Final Note Lint（8 项）、Final Quality Review、Final Readability Review 全部通过。
- SHA-256：`78fdeff958dda6f57a408232d7fb97b1e347eb8e01f939fa96f1ee5a9dfdfac7`；正式保存笔记与最后一次 lint 的字节完全一致，图片与已审查 SHA-256 一致。

## REKI: Registering Knowledge in VLAs

- 论文：[arXiv:2610.22178v1](https://arxiv.org/abs/2610.22178)
- 笔记：[reki/reki.md](reki/reki.md)
- 核心思想：保存动作噪声无关的观测寄存器，复用历史KV并降低多步流积分的记忆成本。
- 代表图：[reki/images/page_005_fig_figure_3_review_repair1.png](reki/images/page_005_fig_figure_3_review_repair1.png)（方法/管线总览，已通过身份和视觉审查）
- 状态：笔记已完成（4 图 materialized / 0 placeholder）。无占位。
- 质量：Grounding Lint、Final Note Lint（8 项）、Final Quality Review、Final Readability Review 全部通过。
- SHA-256：`173eb57486d621e590176c72c57e3ac3508ec248fbc7777cb3e3984879898bbb`；正式保存笔记与最后一次 lint 的字节完全一致，图片与已审查 SHA-256 一致。

## Whole-Body Dexterity

- 论文：[arXiv:2610.22184v1](https://arxiv.org/abs/2610.22184)
- 笔记：[whole-body-dexterity/whole-body-dexterity.md](whole-body-dexterity/whole-body-dexterity.md)
- 核心思想：稳定抓握、支撑模式和专家蒸馏支撑粗粒度遥操作下的身体接触技能。
- 代表图：[whole-body-dexterity/images/page_002_fig_fig_2_review.png](whole-body-dexterity/images/page_002_fig_fig_2_review.png)（方法/管线总览，已通过身份和视觉审查）
- 状态：笔记已完成（2 图 materialized / 2 placeholder）。Table I、II没有取得安全完整的表体图片，保留两处占位及正文数值。
- 质量：Grounding Lint、Final Note Lint（8 项）、Final Quality Review、Final Readability Review 全部通过。
- SHA-256：`90a7d5befd50e88df6a1a8cb3276e1ac56d90d9318d218815d28f18df8e87704`；正式保存笔记与最后一次 lint 的字节完全一致，图片与已审查 SHA-256 一致。

## CoDA: Co-Evolution of Data Engines and Action Policies

- 论文：[arXiv:2610.22362v1](https://arxiv.org/abs/2610.22362)
- 笔记：[coda/coda.md](coda/coda.md)
- 核心思想：把因子化失败诊断和持久记忆编译成环境与势函数，驱动策略后训练。
- 代表图：[coda/images/page_003_fig_figure_2_review.png](coda/images/page_003_fig_figure_2_review.png)（方法/管线总览，已通过身份和视觉审查）
- 状态：笔记已完成（2 图 materialized / 1 placeholder）。Table 1一次修复后仍有外部标题污染，保留主表占位。
- 质量：Grounding Lint、Final Note Lint（8 项）、Final Quality Review、Final Readability Review 全部通过。
- SHA-256：`43d3b502b648a3c7e6e43c0e4895cb853c68e0c866c01a7813a3814f7ef59f55`；正式保存笔记与最后一次 lint 的字节完全一致，图片与已审查 SHA-256 一致。

全文及图像核查不代表在本机复现模型训练、仿真基准或真机部署。来源覆盖边界详见日报；不因可访问官方页面而宣称已穷尽全天更新。
