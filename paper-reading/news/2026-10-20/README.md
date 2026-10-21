# 2026-10-20 Paper Reading

本日精读对应[日报](../../../news/2026-10-20.md)：三篇必读论文与雷达最高分PACT-VLA；Isaac Lab工程条目不纳入论文精读。

共四篇笔记已完成，13 张图片 materialized / 2 处 placeholder。占位保留图像质量边界，正文分析与相关全文证据已核验。

## Ropedia W0: Scaling Loco-Manipulation World Models across Embodiments with Human Experience

- 论文：[arXiv:2610.26855v1](https://arxiv.org/abs/2610.26855)
- 笔记：[ropedia-w0/ropedia-w0.md](ropedia-w0/ropedia-w0.md)
- 核心思想：以相机和投影骨架统一异构人机经验，再做人机混合训练与四步流式蒸馏。
- 代表图：[ropedia-w0/images/page_008_fig_figure_4_review.png](ropedia-w0/images/page_008_fig_figure_4_review.png)（方法或平台总览，身份与视觉审查通过）
- 状态：笔记已完成（3 图 materialized / 1 placeholder）。表S7未取得可用完整候选，保留占位及全文核实的预训练比较数值。
- 质量：Grounding Lint、Final Note Lint（8项）、Final Quality Review、Final Readability Review全部通过。
- SHA-256：`2fbab0da564fdd4e8c9cb6963c0ca08915c619bbc092165c7de0a96edb625d09`；正式保存笔记与最后一次lint字节一致，图片与已审查SHA-256一致。

## HandsOn: A Large-Scale Simulation Benchmark for Generalizable Dexterous Manipulation

- 论文：[arXiv:2610.26765v1](https://arxiv.org/abs/2610.26765)
- 笔记：[handson/handson.md](handson/handson.md)
- 核心思想：把模拟遥操作、成功谓词、专家时长预算与独立迁移任务绑定，分析灵巧操作泛化缺口。
- 代表图：[handson/images/page_001_fig_figure_1_review_repair1.png](handson/images/page_001_fig_figure_1_review_repair1.png)（方法或平台总览，身份与视觉审查通过）
- 状态：笔记已完成（3 图 materialized / 1 placeholder）。表6候选被质量门拒绝，保留占位和正文核实的成功/进度；代表图1一次几何修复后重新通过审查。
- 质量：Grounding Lint、Final Note Lint（8项）、Final Quality Review、Final Readability Review全部通过。
- SHA-256：`cbad83c6cad2499c37ef325a1e5e884d3062a90013edcb480ace60ad1c1bd911`；正式保存笔记与最后一次lint字节一致，图片与已审查SHA-256一致。

## De-Diffusing WAMs: Action-Sufficient Direct Prediction for Robot Control

- 论文：[arXiv:2610.28122v1](https://arxiv.org/abs/2610.28122)
- 笔记：[directwam/directwam.md](directwam/directwam.md)
- 核心思想：先训练一步动作专家，再冻结它以最终动作误差监督确定性未来预测器。
- 代表图：[directwam/images/page_002_fig_figure_1_review.png](directwam/images/page_002_fig_figure_1_review.png)（方法或平台总览，身份与视觉审查通过）
- 状态：笔记已完成（4 图 materialized / 0 placeholder）。无占位；模型侧计时与真机小样本边界均保留。
- 质量：Grounding Lint、Final Note Lint（8项）、Final Quality Review、Final Readability Review全部通过。
- SHA-256：`91c8f1cc14d6fdadf04951a78a4df27f7c075f6cbfa26b1d423a2b88f5ecb940`；正式保存笔记与最后一次lint字节一致，图片与已审查SHA-256一致。

## PACT-VLA: Speculative Action-Chunk Verification with Pre-Commit Observations

- 论文：[arXiv:2610.28019v1](https://arxiv.org/abs/2610.28019)
- 笔记：[pact-vla/pact-vla.md](pact-vla/pact-vla.md)
- 核心思想：先采样固定候选，再用提交前较新观测计算流场一致性，只选择不重生成。
- 代表图：[pact-vla/images/page_004_fig_figure_2_review.png](pact-vla/images/page_004_fig_figure_2_review.png)（方法或平台总览，身份与视觉审查通过）
- 状态：笔记已完成（3 图 materialized / 0 placeholder）。无占位；表4一次几何修复后重新通过审查，P99毫秒与控制拍数分开。
- 质量：Grounding Lint、Final Note Lint（8项）、Final Quality Review、Final Readability Review全部通过。
- SHA-256：`a382b4c76a763ebc230cff27de2d2d0b918eb7a5568e5960f906f48f65b91452`；正式保存笔记与最后一次lint字节一致，图片与已审查SHA-256一致。

以上是论文全文与图像核查，不代表完成模型训练、仿真或真实机器人独立复现。动态机构和会议来源覆盖不完整，详见日报说明。
