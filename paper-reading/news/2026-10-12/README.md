# 2026-10-12 Paper Reading

对应 [当日日报](../../../news/2026-10-12.md)。完成 5 篇全文精读：今日必读 3 篇，以及论文雷达得分最高的 2 篇。正式产物仅包含本登记、中文 Markdown 笔记与相对路径图片。

| 论文 | 原文身份 | 核心结论与边界 | 状态 | 插图 / 占位 |
|---|---|---|---|---|
| [Splat2Act: From Captured Scenes to Personalized VLA Manipulation](splat2act/splat2act.md) | [arXiv:2610.13945v1](https://arxiv.org/abs/2610.13945) | 数字孪生生成抓取示范用于场景个性化；基线包含本体差异，跨场景仍弱 | 完成 | 4 / 1 |
| [Dream to Remember: Continual Steering of Generalist Robot Policies with World Models](dream-to-remember/dream-to-remember.md) | [arXiv:2610.13816v1](https://arxiv.org/abs/2610.13816) | 想象可用于保留旧技能；不够准确的世界模型不能替代新技能真实训练 | 完成 | 3 / 3 |
| [Noise Space Learning for VLA Adaptation](noise-space-vla/noise-space-vla.md) | [arXiv:2610.13943v1](https://arxiv.org/abs/2610.13943) | 冻结VLA后学习噪声分布；更新计算不等于训练墙钟，真机SAC有接触失败 | 完成 | 10 / 2 |
| [Chronos Policy: Learning Robot Policies on Physical Time](chronos-policy/chronos-policy.md) | [arXiv:2610.13929v1](https://arxiv.org/abs/2610.13929) | 采集与执行时间进入策略；真机得分含半分完成，部分任务出现退化 | 完成 | 10 / 2 |
| [BT-Agent: Deploying Onboard Robot Agents with Behavior Trees and Multi-Fidelity Evaluation](bt-agent/bt-agent.md) | [arXiv:2610.13862v1](https://arxiv.org/abs/2610.13862) | 本地行为树接慢速推理；操作员批准与预定义技能仍是部署假设 | 完成 | 4 / 1 |

五篇均读取可用全文、方法、实验与附录；Grounding 检查和 8 项正文校验全部通过，最终质量与可读性审查通过。正式保存脚本输出的正文 SHA-256 与最终校验一致；31 张插图均逐张检查候选及原始页预览，保存后的图片校验值与视觉审查记录一致。

9 处占位保留了原图表编号、用途及未插图原因。Dream to Remember 的 Table 1、Chronos 的 Table 6 在一次裁切修复后仍有视觉缺陷，停止修复并保留占位；关键数值通过原始页转写。其他占位来自资产缺失或不合格裁切。没有把占位当作已审图片，也没有将相邻正文碎片发布为图表。

阅读时以每篇“实验支持什么、尚不能证明什么”的边界为准。MC-EvoBench 与 HorizonNav 当日仅进入文字雷达，没有完成全文精读，不列入本完成表。
