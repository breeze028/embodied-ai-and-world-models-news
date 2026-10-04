# 2026-10-04 Paper Reading

本日精读对应日报 [news/2026-10-04.md](../../../news/2026-10-04.md)。当日为 arXiv 周末公告空窗（周日 ET 批次未发布），精读对象来自补充窗口尾巴（实际提交北京 10-02 00:00–02:00、cs.CV/cs.AI/cs.LG 主分类、前两日日报按 cs.RO 主线覆盖后的剩余），按「今日必读论文优先、雷达高分次之」处理 4 篇；Reliability-Aware World Model（必读 #3）为开源事件类条目（论文在投无 arXiv 号、拿不到可用全文），按「工程/开源条目不纳入精读」规则跳过。

| # | bundle（短 slug） | 论文 | 最强验证标识符 | 一句话核心思想 | 代表图 | 状态 |
|---|---|---|---|---|---|---|
| 1 | [world-observer/](world-observer/) | World Observer: Joint Actor-Observer Generation for Persistent World Modeling | [arXiv:2610.02162v1](https://arxiv.org/abs/2610.02162) | 把观察从行动解耦：共享 DiT 联合生成 actor 透视流 + 全景 observer 流，画外物体在 observer 里持续演化；OOV-F/OOV-Dgt/OOV-Dself 把四种 out-of-view 失败变成可计算判据 | images/page_005_fig_figure_4_review.png（主架构 + Observer Sink 双面板总览，Fig. 4） | 笔记已完成（10 图 materialized / 0 placeholder；SHA-256 与 lint 一致；Grounding Lint、Final Note Lint 8 门、Final Quality Review、Final Readability Review 全部通过） |
| 2 | [pyrua-lean/](pyrua-lean/) | Fewer Tokens, Better Action: GPT-6 Astra Robot Agents with 14% Higher Success Rate but 65% Fewer Tokens | [arXiv:2610.01939v1](https://arxiv.org/abs/2610.01939) | 同 planner 同原语等预算下只换接口：`python(code)` + 持久命名空间 + 选择性观察让成功率 +8.6pt、输入量 -65%；反事实证明单独做按需回图反而有害 | images/page_004_fig_figure_2_review.png（tool calling vs PyRUA-Lean vs 几何放置示例三面板，Fig. 2） | 笔记已完成（10 图 materialized / 0 placeholder；SHA-256 与 lint 一致；四类 lint/review 全部通过） |
| 3 | [latent-foresight/](latent-foresight/) | Latent-Foresight: End-to-End Learning Predictable Representations for Latent World Models | [arXiv:2610.01942v1](https://arxiv.org/abs/2610.01942) | tokenizer 也该吃预测梯度：四件稳定化设计（归一化 / 双向 stop-grad / 辅助重建 / logit-normal）让端到端潜空间为可预测性塑形，两行 Training Collapse 划出安全边界 | images/page_004_fig_figure_1_review.png（VFM→AE→Flow 三路损失端到端总览，Fig. 1） | 笔记已完成（12 图 materialized / 0 placeholder；SHA-256 与 lint 一致；四类 lint/review 全部通过） |
| 4 | [rowbench/](rowbench/) | ROWBench: Do Video Models Render What the Program Specifies? | [arXiv:2610.02205v1](https://arxiv.org/abs/2610.02205) | 可重放引擎记录当 ground truth：LRA/ISR 测「程序规定事件有没有被画出来」；代理条件化碾压相机条件化，长时程与跨视角身份绑定是当前最大缺口 | images/page_004_fig_figure_2_review.png（三面板生成管线总览：世界合成→控制编译→最终验证，Fig. 2） | 笔记已完成（7 图 materialized / 0 placeholder；SHA-256 与 lint 一致；四类 lint/review 全部通过） |

## 精读范围说明

- 「今日必读」3 条中 2 条为论文类（World Observer、PyRUA-Lean）→ 已精读；Reliability-Aware World Model（#3）为开源事件条目（ICLR 2027 在投、无 arXiv 号、仅项目页与代码仓、拿不到可用全文），按规则跳过并在日报注明。
- 「论文雷达」5 篇中双评分最高的 2 篇：Latent-Foresight（76/100）、PROWBench/ROWBench（74/100）→ 已精读。
- 语言契约：全链路 output_language=zh-CN（4 篇 bundle 的 writing_contract.language 与全部 lint 工件一致）。
- 代表图说明：4 篇均按「方法/管线总览优先」选择；World Observer 选 Fig. 4（架构 + Observer Sink 双面板）、PyRUA-Lean 选 Fig. 2（接口对比三面板）、Latent-Foresight 选 Fig. 1（端到端总览）、ROWBench 选 Fig. 2（数据管线三面板），日报嵌图路径与各 bundle 的 images/ 文件一致。
