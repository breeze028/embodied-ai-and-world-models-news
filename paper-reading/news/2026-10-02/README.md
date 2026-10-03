# 2026-10-02 Paper Reading

> 本日精读对应日报 [news/2026-10-02.md](../../news/2026-10-02.md)。7 篇 = 今日必读 5 篇 + 论文雷达双评分最高的 2 篇（Kinematic MeanFlow、Magic-W0）。全部经 deep-paper-reading skill 完整工作流（确定性管线 → Visual Review Gate → note plan → grounding lint → 笔记 → 8-gate note lint → 两类 review → 正式保存），语言 zh-CN。

| # | bundle（短 slug） | 论文 | 最强标识符 | 一句话核心 | 代表图 | 状态 |
|---|---|---|---|---|---|---|
| 1 | `rpg-robot/` | Reconstruct, Practice, Go Real: Guided Self-Improvement for Embodied Agents | [arXiv:2610.02204](https://arxiv.org/abs/2610.02204) | 不更新权重：仿真中练习 + 诊断修订符号技能与 system prompt + 跨任务门控合并回滚，held-out 成功率 28.6%→95.0%，真机 30/30 | `images/page_001_fig_figure_1_review.png`（Fig 1，框架总览三面板） | 笔记已完成（6 图 materialized / 0 placeholder；SHA-256 与 lint 一致） |
| 2 | `humanoidtoolbench/` | HumanoidToolBench: Benchmarking Humanoid Tool Use from Selection to Mobile Execution | [arXiv:2610.02089](https://arxiv.org/abs/2610.02089) | 3 场景 × 3 执行层级 × 2 工具集模式 = 18 任务 + ToolBook 3.1k 演示；量化出 L2 移动执行（76%→9%）与「够得着≠选得对」（98.8%→44.2%）两断崖 | `images/page_001_fig_fig_1_review.png`（Fig 1，总览） | 笔记已完成（7 图 materialized / 0 placeholder；SHA-256 与 lint 一致） |
| 3 | `uniwam/` | UniWAM: Unified World-Action Model | [arXiv:2610.02054](https://arxiv.org/abs/2610.02054) | 三专家 MoT（物理推理器/世界生成器/动作预测器）+ 三源监督分配 + 物理语言动作编码；LIBERO 99.2 / LIBERO-Plus 92.6 / C2R 68.32，附 log-linear scaling law 与 1k 小时人类数据阈值 | `images/page_001_fig_figure_1_review.png`（Figure 1，总览海报） | 笔记已完成（10 图 materialized / 0 placeholder；SHA-256 与 lint 一致） |
| 4 | `interevolve/` | InterEvolve: Test-Time Evolution of Reward Programs for Humanoid Loco-Manipulation | [arXiv:2610.02196](https://arxiv.org/abs/2610.02196) | 控制器冻结，reward program（分层奖励+完成条件+常数）作为可编辑策略：LLM 改结构 / CMA-ES 调常数双循环 + FB 模型零重训执行；固定程序 34.6%→86.5%，真机 G1 自主执行 | `images/page_004_fig_figure_2_review.png`（Figure 2，总览三面板） | 笔记已完成（9 图 materialized / 5 low_priority 项保留 placeholder 说明；SHA-256 与 lint 一致） |
| 5 | `sklewam/` | SkeleWAM: Skeleton World-Action Modeling for Efficient Robotic Manipulation | [arXiv:2610.02120](https://arxiv.org/abs/2610.02120) | 稀疏 3D 骨架（关节+物体中心+交互点）当 WAM 状态空间：未来骨架监督只进训练、推理砍分支；57.1M 参数 LIBERO-Plus 85.9%，相机维 93.4，layout 66.6 为明示弱点 | `images/page_004_fig_figure_2_review.png`（Figure 2，架构总览） | 笔记已完成（8 图 materialized / 0 placeholder；SHA-256 与 lint 一致） |
| 6 | `k-mf/` | Kinematic MeanFlow: One-Step Action Generation Policy for Robotic Foundation Models | [arXiv:2610.00864](https://arxiv.org/abs/2610.00864) | RFM 速度场「末期激增 76×+散布展宽」使 MeanFlow 自举崩溃；运动学恒等式在中间点解耦时间导数——一步生成 94.5 匹配四步 FM，动作头延迟 -67.5~-74.4% | `images/page_004_fig_figure_2_review.png`（Figure 2，机制对比三面板） | 笔记已完成（10 图 materialized / 0 placeholder；SHA-256 与 lint 一致） |
| 7 | `magic-w0/` | Magic-W0: A Structured World-Action Foundation Model for Physical Intelligence | [arXiv:2609.39870](https://arxiv.org/abs/2609.39870) | 结构化世界转移（几何→运动→语义）+ 层对齐世界-动作交互 + 201.4 万 episode 四域预训练；RoboDojo 27.10 居 WAM 首位，真机 94.6 vs π0.5 91.8，两组机制干预证世界头真用动作 | `images/page_004_fig_figure_2_review.png`（Figure 2，四路架构对比） | 笔记已完成（11 图 materialized / 0 placeholder；SHA-256 与 lint 一致） |

## 备注

- 精读优先级：今日必读 5 篇按日报排序（RPG → HumanoidToolBench → UniWAM → InterEvolve → SkeleWAM），随后雷达最高双评分 2 篇（Kinematic MeanFlow 79 分、Magic-W0 79 分）。
- Magic-W0 实际提交时间为北京时间 2026-09-30 22:49（v1），属日报补充窗口；已按补充窗口规则标注实际发布时间收录。
- 每篇 bundle 内 `images/` 为该论文图片资产，`<短slug>.md` 为正式笔记；bundle 相对日报的路径约定见各笔记首行引用。
