# 2026-10-26 Paper Reading

本索引对应[当日日报](../../../news/2026-10-26.md)。必读论文世界模型损失消融与雷达最高分Zero-HLM、Predictable Latents均已完成精读。

## [What Does World Modeling Actually Improve in Robot Action Learning?](world-loss/world-loss.md)

标识：[arXiv:2610.34593v1](https://arxiv.org/abs/2610.34593)；[bundle目录](world-loss/world-loss.md) 使用短slug `world-loss`。

固定训练架构、数据、初始化与步数，隔离未来视频监督收益，区分熟悉任务执行与分布外迁移。

代表图：[page_003_fig_figure_1_review.png](world-loss/images/page_003_fig_figure_1_review.png)，为审查通过的方法/管线总览图。

**笔记已完成**：4图materialized / 0 placeholder。Grounding Lint、八项Final Note Lint、Final Quality Review、Final Readability Review通过；原脚本正式保存后正文和全部图片SHA-256复核一致。

正文SHA-256：`8370c416f33a02471c80946a5fdec89b14f9343d533f92e5dac285d12f6f09c5`。

## [Zero-HLM: Generalizable Humanoid Loco-Manipulation without Real Robot Data](zero-hlm/zero-hlm.md)

标识：[arXiv:2610.35075v1](https://arxiv.org/abs/2610.35075)；[bundle目录](zero-hlm/zero-hlm.md) 使用短slug `zero-hlm`。

用真实场景重建、运动与环境协同适配和执行回放生成移动操作示范；区分零真实动作训练与现实采集成本。

代表图：[page_004_fig_figure_2_review.png](zero-hlm/images/page_004_fig_figure_2_review.png)，为审查通过的方法/管线总览图。

**笔记已完成**：5图materialized / 0 placeholder。Grounding Lint、八项Final Note Lint、Final Quality Review、Final Readability Review通过；原脚本正式保存后正文和全部图片SHA-256复核一致。

正文SHA-256：`42928ef55ce93506285a17edfcedfef8ce5091000b31377ac87bfa38685cc5e0`。

## [Video World Models Need Predictable Latents](latent/latent.md)

标识：[arXiv:2610.34663v1](https://arxiv.org/abs/2610.34663)；[bundle目录](latent/latent.md) 使用短slug `latent`。

让潜空间更容易预测，并用历史条件解码器保留像素细节；分开评估误差、采样预算与策略排名。

代表图：[page_002_fig_figure_1_review.png](latent/images/page_002_fig_figure_1_review.png)，为审查通过的方法/管线总览图。

**笔记已完成**：3图materialized / 1 placeholder。Grounding Lint、八项Final Note Lint、Final Quality Review、Final Readability Review通过；原脚本正式保存后正文和全部图片SHA-256复核一致。

占位原因：图6原裁剪混入非图正文；允许的一次有界修复仍未解决，冻结为visual_defect，笔记明确说明且未插入缺陷图片。这是配图缺口，不是未读全文或隐藏精读失败。

正文SHA-256：`a80681210e41ec8baef5df6ff8377eeb5dcb9d4dec48d709a0607867a33d54da`。

本次分别核读18、23、54页全文与相关附录，全部插图经过视觉审查。合计3篇、12张materialized图片、1处占位；没有执行模型推理、训练或机器人复现。来源检查缺口与时间归属见日报。
