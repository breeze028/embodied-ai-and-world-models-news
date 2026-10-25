# 2026-10-24 Paper Reading

本日精读对应[科研日报](../../../news/2026-10-24.md)：必读论文 1 篇及雷达分数最高的 2 篇。

## RoboJev: An Open Vision-Language Judge for Robot Success Detection

**笔记：** [robojev/robojev.md](robojev/robojev.md) · [作者固定 PDF](https://huggingface.co/josefchen/RoboJev-27B/resolve/b1873c298b85344afa1b249d473f0766122bd5f2/paper/RoboJev.pdf)  
**核心思想：** 稀疏多视图终局判别，适配收益必须与域外排序和概率校准一起检查。  
**代表图：** [robojev/images/page_003_fig_figure_2_review.png](robojev/images/page_003_fig_figure_2_review.png)（方法总览）  
**状态：** 笔记已完成（3 图 materialized / 0 placeholder；Grounding Lint、八项 Final Note Lint、Final Quality Review、Final Readability Review 均通过；正式保存与 lint SHA-256 一致）。  
**SHA-256：** `a3facbc7c54821a12643a04d9aebc5e59c168cc54e3545c8af33e430a2f9eebb`

## DRILL: Training World Models to Improve Policies, Not Predict Pixels

**笔记：** [drill/drill.md](drill/drill.md) · [arXiv:2610.30814v1](https://arxiv.org/abs/2610.30814)  
**核心思想：** 按想象更新后的策略回报学习世界模型，VWI 与 IMG 交换计算和环境交互成本。  
**代表图：** [drill/images/page_004_fig_figure_1_review.png](drill/images/page_004_fig_figure_1_review.png)（方法总览）  
**状态：** 笔记已完成（4 图 materialized / 0 placeholder；Grounding Lint、八项 Final Note Lint、Final Quality Review、Final Readability Review 均通过；正式保存与 lint SHA-256 一致）。  
**SHA-256：** `b147ce5c766617b3f91a9f950e530bc4b1d1437a424e89e547f81762971eb1fd`

## Memory before Goal: Role of Pre-History Memory for Humanoid Loco-Manipulation

**笔记：** [memory/memory.md](memory/memory.md) · [arXiv:2610.31166v1](https://arxiv.org/abs/2610.31166)  
**核心思想：** 用物体事件保留消失的线索，把记忆接入动作专家并隔离记忆决策与操作成功。  
**代表图：** [memory/images/page_003_fig_fig_3_review.png](memory/images/page_003_fig_fig_3_review.png)（方法总览）  
**状态：** 笔记已完成（3 图 materialized / 2 placeholder；Grounding Lint、八项 Final Note Lint、Final Quality Review、Final Readability Review 均通过；正式保存与 lint SHA-256 一致）。  
**SHA-256：** `0998c7b809c82578357888da92cfda7b934e9acc2d51393eb1751d4d0c87ad54`

保留第 7 页 Table IV / V 占位：没有独立完整表格候选，已对照完整 300 dpi 原页核对消融及真机计数，数值在正文重排；3 张方法/任务图均通过视觉审查。

三篇均保留方法总览，无需以结果图替代。RoboJev 全文含数据/评测附录；DRILL 全文含实现、预算及敏感性附录。没有下载的 PDF、抽取 JSON 或运行脚本进入正式产物。
