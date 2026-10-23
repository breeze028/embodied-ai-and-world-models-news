# 2026-10-22 Paper Reading

对应 [本日日报](../../../news/2026-10-22.md)。四篇均完成全文阅读、Grounding Lint、八项 Final Note Lint、质量与可读性审查、正式保存和复制后 SHA-256 校验。

- [Agentic World Action Models](aw0/aw0.md) · [arXiv:2610.30136](https://arxiv.org/abs/2610.30136)。代码、视频与动作通过C→V→A块因果注意力联合去噪，使程序表征参与连续控制。  
  代表图：`aw0/images/page_003_fig_figure_2_review_repair1.png`（方法总览，视觉审查通过）。  
  笔记已完成（5 图 materialized / 0 placeholder；SHA-256 与 lint 一致：`44ea857a4395441afd4cf158f635dc7d21e285b8d341cef715dc70cb73e32043`）。
- [CW-WAM: A Structured Contact-Wrench World Action Model for Force-Sensitive Manipulation](cwwam/cwwam.md) · [arXiv:2610.30117](https://arxiv.org/abs/2610.30117)。把动作与接触wrench按物理先后配对生成，并用慢模型加快导纳与阻抗环执行。  
  代表图：`cwwam/images/page_002_fig_fig_2_review.png`（方法总览，视觉审查通过）。  
  笔记已完成（3 图 materialized / 1 placeholder；SHA-256 与 lint 一致：`67883fa95e06efb999f368e204bbe9d0cf8e3e377cc11c4bd5bd87eea714e5ff`）。
  占位原因：预测误差表未找到匹配的完整独立图像候选，保留原文数值与标准占位。
- [ALPS: Visual State Encoders for World Models](alps/alps.md) · [arXiv:2610.30120](https://arxiv.org/abs/2610.30120)。静态图文多任务预训练加冻结教师跨裁剪对齐，在同组patch token中平衡状态、语义和像素。  
  代表图：`alps/images/page_003_fig_figure_2_review.png`（方法总览，视觉审查通过）。  
  笔记已完成（4 图 materialized / 0 placeholder；SHA-256 与 lint 一致：`a14e51fc08e64b0eb95930b4e78ef506b4b9f87bb28a910fe00e9cd2b2016a52`）。
- [PhysiCalWorld: In-Context Physics Calibration for World Models](physicalworld/physicalworld.md) · [arXiv:2610.30125](https://arxiv.org/abs/2610.30125)。把同一物理配置的另一段交互压缩为64维描述符，条件化冻结视觉表示上的动态预测器。  
  代表图：`physicalworld/images/page_004_fig_figure_2_review.png`（方法总览，视觉审查通过）。  
  笔记已完成（4 图 materialized / 0 placeholder；SHA-256 与 lint 一致：`d4f9f0f0605048d6d75ce7c0313dffb4fbf8ed22d373754a76a96800ce88b4ec`）。
