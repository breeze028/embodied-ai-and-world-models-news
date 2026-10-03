# 2026-10-03 Paper Reading

本日精读对应日报 [news/2026-10-03.md](../../../news/2026-10-03.md)。当日为 arXiv 周末公告空窗（周五 ET 后提交并入周一批次），精读对象全部来自补充窗口实际提交的论文，按「今日必读论文优先、雷达高分次之」处理 4 篇；PRISM 为开源事件类条目（非论文类），按规则不纳入精读。

| # | bundle（短 slug） | 论文 | 最强验证标识符 | 一句话核心思想 | 代表图 | 状态 |
|---|---|---|---|---|---|---|
| 1 | [wmm/](wmm/) | World Motion Models: Flexible Sequence Modeling of SE(3) Trajectories | [arXiv:2610.01742v1](https://arxiv.org/abs/2610.01742)（NeurIPS 2026 Spotlight） | 稀疏刚体 SE(3) 位姿轨迹作为 4D 世界的统一生成语言；per-token 噪声级 flow matching 让策略/世界模型/补全/retargeting 全变成同一网络上的不同掩码 | images/page_005_fig_figure_3_review.png（五类分解式注意力架构总览，Fig. 3） | 笔记已完成（7 图 materialized / 0 placeholder；SHA-256 与 lint 一致；Grounding Lint、Final Note Lint 8 门、Final Quality Review、Final Readability Review 全部通过） |
| 2 | [ewam/](ewam/) | EWAM: Emergent Depth-Wise Specialization in a Unified Embodied Model -- From Semantic Understanding through Visual Foresight to Action | [arXiv:2609.39973v1](https://arxiv.org/abs/2609.39973) | 动作流作为唯一整合界面的非对称注意力统一模型；浅层读语义、中层看预测未来、深层管动作的深度分工经分层屏蔽与反事实注入的因果验证 | images/page_006_fig_figure_2_review.png（三专家非对称联合注意力总览，Fig. 2） | 笔记已完成（16 图 materialized / 0 placeholder；SHA-256 与 lint 一致；四类 lint/review 全部通过） |
| 3 | [dill/](dill/) | Disentangling Spurious Correlations in Vision-Language-Action Models via Predicting Domain-Invariant Latent Lookahead | [arXiv:2609.37165v1](https://arxiv.org/abs/2609.37165)（CoRL 2026） | VLA 捷径学习的关键不是「要不要预测未来」而是「预测未来的什么表征」：域不变前瞻 latent + 当前表征解耦，捷径度 0.73→0.05 | images/page_004_fig_figure_2_review.png（Task-Domain Encoder 与策略学习双面板总览，Fig. 2） | 笔记已完成（11 图 materialized / 0 placeholder；SHA-256 与 lint 一致；四类 lint/review 全部通过） |
| 4 | [d-and-r/](d-and-r/) | Divide-and-Remember: Recursive Action-Relevant Memory for Long-Horizon VLA Policies | [arXiv:2610.00982v1](https://arxiv.org/abs/2610.00982) | 「记什么」形式化为最大化 I(action; memory | observation)：递归 2K→top-K 选择器在预训练单元空间端到端训练，64 token 做 RoboMME SOTA | images/page_005_fig_figure_3_review.png（递归记忆选择与调制模块总览，Fig. 3） | 笔记已完成（9 图 materialized / 0 placeholder；SHA-256 与 lint 一致；四类 lint/review 全部通过） |

## 精读范围说明

- 「今日必读」3 条中 2 条为论文类（WMM、EWAM）→ 已精读；PRISM（#2）为开源事件条目（论文本体 09-29 提交、超窗，窗口内事件为代码/数据开源），按「工程/开源条目不纳入精读」规则跳过。
- 「论文雷达」6 篇中双评分最高的 2 篇：DILL（76/100）、Divide-and-Remember（74/100）→ 已精读。
- 语言契约：全链路 output_language=zh-CN（4 篇 bundle 的 writing_contract.language 与全部 lint 工件一致）。
