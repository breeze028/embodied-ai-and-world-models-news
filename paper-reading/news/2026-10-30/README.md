# 2026-10-30 Paper Reading

本页是 [2026-10-30 日报](../../../news/2026-10-30.md) 的论文精读索引，覆盖「今日必读」全部 4 篇与「论文雷达」最高分 1 篇。

## 精读列表

### touchbridge

- **论文：** TouchBridge: Tactile-Conditioned Human-to-Robot Transfer for Dexterous Manipulation（[arXiv:2610.40349](https://arxiv.org/abs/2610.40349)）
- **核心思想：** 用测量到的指尖接触（接触块中心、活跃 taxel、多指接触图）而不是指尖位姿做跨本体对应，把人类示教直接转成机器人域训练数据。
- **代表图：** `images/page_004_fig_fig_3.png`（Tac-Retarget 三项约束；总览图 1 因裁切混入标题与图注、一次修复后仍含图注首行，未采用）
- **状态：** 笔记已完成（1 图 materialized / 0 占位；SHA-256 `3364c0e3889d9b3d06f29af07e78d1b48439c324cb046cc6bb2c485d0e803ce8` 与 Final Note Lint 一致）

### swapbot

- **论文：** SwapBot: Tool-Centric Robot Manipulation via Interchangeable End-Effectors and Tactile Sensing（[arXiv:2610.40646](https://arxiv.org/abs/2610.40646)）
- **核心思想：** 机器人侧只留电磁耦合接口，工具侧用廉价 3D 打印适配器把家用工具变成带压阻触觉的末端执行器，再以工具选择器加工具专用扩散策略完成长程任务。
- **代表图：** `images/page_003_fig_fig_2_review.png`（系统总览与传感器叠层）
- **状态：** 笔记已完成（2 图 materialized / 0 占位；SHA-256 `5915740c9493cdeaa2ab6493e49d749da6be4d36886c196efd2a7db6049181c6` 与 Final Note Lint 一致）

### primew0

- **论文：** PRIME W0: Physical Priors from World Models for Embodied Manipulation（[arXiv:2610.39528](https://arxiv.org/abs/2610.39528)）
- **核心思想：** 把 VLM 逐层 KV、世界模型异步预测的子目标图与 DINOv2 历史帧三路条件汇入协方差噪声驱动的流匹配动作专家，在 LIBERO 与自建真机上报告 SOTA。
- **代表图：** `images/page_006_fig_figure_2_review.png`（四阶段训练流程）
- **状态：** 笔记已完成（1 图 materialized / 0 占位；SHA-256 `7b8a219c612b9acaa06da33c86def031f521d86aeb255dd4037ef92a37ed04a9` 与 Final Note Lint 一致）

### event2reward

- **论文：** Event2Reward: Learning Robotic Rewards from Progress Relations（[arXiv:2610.39212](https://arxiv.org/abs/2610.39212)）
- **核心思想：** 用真实执行事件构造同一轨迹内的进度比较关系，与归一化时间标签联合训练进度模型，再把进度差作为势函数塑形奖励。
- **代表图：** `images/page_002_fig_figure_1_review.png`（方法总览与主要结果面板）
- **状态：** 笔记已完成（1 图 materialized / 0 占位；SHA-256 `d9aec065e56194367917ab1072f4d82b1a33ee946b94c2f91eaf5d2e9ec30756` 与 Final Note Lint 一致）

### hifor

- **论文：** HiFOR: Hierarchical Foresight with Action-Guided World Grounding for Vision-Language-Action Model（[arXiv:2610.40373](https://arxiv.org/abs/2610.40373)）
- **核心思想：** 用层级依赖掩码联合预测短期、里程碑与目标三层未来，再按时间、视角、空间组织成结构化潜世界，由动作表示在去噪中做因子化检索。
- **代表图：** `images/page_004_fig_figure_2.png`（总体框架）
- **状态：** 笔记已完成（1 图 materialized / 0 占位；SHA-256 `a4af392c3b5fe1379ec130e82f02ce39fe7740985041455e981630321d6a0d34` 与 Final Note Lint 一致）

## 说明

- 五篇论文均从 arXiv 官方 PDF 完整提取正文（另含附录），grounding lint 与八项最终 lint 全部通过，正式保存由 `write_markdown_note.py` 完成，保存后复核笔记与图片 SHA-256。
- 图片均经 300 dpi 裁剪与视觉审查，正文没有保留占位；裁剪不合格的总览图已如实登记为视觉缺陷并使用可用的方法图或框架图替代。
- 本次未执行任何训练、推理或机器人实验，笔记中的数字均来自论文报告。
