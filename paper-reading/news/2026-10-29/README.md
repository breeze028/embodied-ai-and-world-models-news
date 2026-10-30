# 2026-10-29 Paper Reading

对应[当日日报](../../../news/2026-10-29.md)。本次精读 4 篇：日报「今日必读」3 篇与雷达最高分 1 篇；均完成全文提取、图表视觉审查、grounding、八项笔记 lint、质量/可读性审查与正式保存。

> **来源检查不完整：** 本次运行时 arXiv 最新公告批次仍为 2026-10-28，按实际提交时间只覆盖到北京时间 10-28 01:59；10-29 主窗口没有可用公告批次。下列精读均来自 48 小时补充窗口，不能据此断言 10-29 全天没有其他重要工作。

## [TOPS: Reshaping Flow Source and Transport for Multi-Task Robot Manipulation](tops/tops.md)

标识：[arXiv:2610.36694v1](https://arxiv.org/abs/2610.36694)；短 slug：`tops`；[bundle 入口](tops/tops.md)。

按任务反演专家动作并拟合低秩 MPPCA 源，在高斯 OT 特征基里只对扩张方向做先慢后快插值；一步两阶段采样在 LIBERO-10 上从 53.44% 提升到 69.67%。

代表图：[page_004_fig_figure_2_review.png](tops/images/page_004_fig_figure_2_review.png)，为方法/管线总览图。

**笔记已完成**（2 图 materialized / 0 placeholder；Grounding Lint、八项 Final Note Lint、Final Quality Review、Final Readability Review 通过；原保存脚本成功，正式正文与全部图片 SHA-256 匹配）。

正文 SHA-256：`98d1814738cb22e4206b37fcdd5ec00e5916638dd04c46aee01175968caf122a`。

## [Learning Multi-Phase Robot Loco-Manipulation via Phase-Conditioned Policy Optimization](locomanip/locomanip.md)

标识：[arXiv:2610.36270v1](https://arxiv.org/abs/2610.36270)；短 slug：`locomanip`；[bundle 入口](locomanip/locomanip.md)。

用环境状态机切阶段、阶段门控奖励、辅助阶段预测与阶段条件残差 critic，再加多阶段重置课程；在 Unitree G1 与 Boston Dynamics Spot 上部署单个多阶段策略。

代表图：[page_004_fig_fig_3_review.png](locomanip/images/page_004_fig_fig_3_review.png)，为方法/管线总览图。

**笔记已完成**（2 图 materialized / 0 placeholder；Grounding Lint、八项 Final Note Lint、Final Quality Review、Final Readability Review 通过；原保存脚本成功，正式正文与全部图片 SHA-256 匹配）。

正文 SHA-256：`e414633b1e919ddb83b4cf3c58721a75389e966020156a19b13ed568807ab9b0`。

## [HIDRA: Hierarchical Dual-Routing Attention for Replay-Free Lifelong Imitation Learning](hidra/hidra.md)

标识：[arXiv:2610.36374v1](https://arxiv.org/abs/2610.36374)；短 slug：`hidra`；[bundle 入口](hidra/hidra.md)。

冻结多模态主干加可扩展 LoRA 专家库，先用语言检索锚定专家并限制候选集为更早专家，再在候选集内按上下文细化，最后用键空间任务内对齐与任务间正交正则稳定路由。

代表图：[page_009_fig_figure_3_review.png](hidra/images/page_009_fig_figure_3_review.png)，为主结果图 3（方法总览图 2 的自动裁切分辨率不足且检测到 bbox 外内容，未通过视觉审查，正文保留 1 张占位）。

**笔记已完成**（1 图 materialized / 1 placeholder；Grounding Lint、八项 Final Note Lint、Final Quality Review、Final Readability Review 通过；原保存脚本成功，正式正文与全部图片 SHA-256 匹配）。

正文 SHA-256：`2c717c3574697b22e843eec9b345184e2af53a52da4ff6e2dc78c8d59d1774e6`。

## [SWIM: Learning What Matters from Behaviors for JEPA World Models](swim/swim.md)

标识：[arXiv:2610.36662v1](https://arxiv.org/abs/2610.36662)；短 slug：`swim`；[bundle 入口](swim/swim.md)。

用门控逆动力学从离线动作学状态坐标权重，冻结后把加权状态距离替换 SCALE 的均匀目标；逆动力学只在训练期使用，部署仍是图像潜空间规划。

代表图：[page_007_fig_figure_1_review.png](swim/images/page_007_fig_figure_1_review.png)，为方法/管线总览图。

**笔记已完成**（2 图 materialized / 0 placeholder；Grounding Lint、八项 Final Note Lint、Final Quality Review、Final Readability Review 通过；原保存脚本成功，正式正文与全部图片 SHA-256 匹配）。

正文 SHA-256：`5b446ecf8f143f449246f0a52cfab64ba9776783f93500765076879353f6d44d`。

共 4 篇、7 张图片 materialized、1 张占位（HIDRA 方法总览图）。本次没有执行模型训练、推理或机器人实验。来源检查缺口与各篇实际提交时间见日报。
