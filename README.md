# Embodied AI & World Models News

> 具身智能与世界模型每日研究动态与论文精读。

**最新一期：2026-11-14** ｜ [日报原文](news/2026-11-14.md) · [精读索引](paper-reading/news/2026-11-14/README.md) · [历史归档](#历史归档)

---

<!-- 本段由 codex-deployment/update_readme.py 从 news/2026-11-14.md 自动镜像，请勿手工编辑 -->

## 2026-11-14 Embodied AI & World Models Daily

> 主窗口：北京时间 11 月 14 日；补充窗口：11 月 12–13 日。本期核验 PEAR 新代码事件，并完成 EgoX、Reins 两篇补充窗口论文的全文精读。**来源检查不完整：arXiv 最新公告仍为 13 日，不能据此断言 14 日没有投稿；其他访问缺口见文末。**

### 🔥 今日必读

#### 1. 【开源项目】PEAR：将仿真机器人 RL 接入推理模型后训练

**来源：** [MIT HAN Lab 官方代码](https://github.com/mit-han-lab/pear) · [官方技术说明](https://mit-han-lab.github.io/pear-blog/)  
**类型：** Open Source · open_source  
**时间依据：** 仓库创建于北京时间 2026-11-14 01:43:06；这是代码仓库创建时间，不用于断言论文也于当天首次公开。  
**评分：** 83/100  
**关键词：** Robot-Use RL · Reasoning Model · Simulation

**核心贡献：** 开放面向 agentic robotics 的后训练基础设施，让推理模型从相机和状态直接输出末端目标，在仿真任务成功反馈下学习机器人使用。

- 训练基于 veRL 的异步 RL、GRPO、动态采样及 Score Centering；Ray 集群同时承载 MuJoCo CPU 和 Isaac Sim GPU 环境。长上下文训练使用 FSDP、序列并行、梯度检查点和激活卸载，回合前缀 KV 缓存经 LMCache 向 CPU 卸载。
- 官方项目说明报告：27B 基础模型在 LIBERO 从 1.6% 到 74.4%；同场景换指令为 57.4%，对照 π0.5 为 0.75%。这些是作者报告的不同协议成绩，本期未做独立复现。
- “不需 harness”指没有额外感知工具、抓取规划器或技能库；实际执行仍由逆运动学和机器人控制器完成，不能写成直接生成电机信号。
- 复现成本应分开看：模型服务文档列单 RTX 5090/GB300 部署路径，而完整 quick start 要求 32 个 GPU 节点（8 个训练、24 个 rollout；每节点 8 H100 或 4 GB300）。单卡推理不代表单卡可重现完整训练。

**为什么值得关注：** 研究对象从模仿动作轨迹转向推理模型的多轮物理交互后训练。工程价值在训练、模拟器和部署接口整合；任务收益、服务成本及跨机器人泛化仍应按各自试验条件评估。

**资源：** [代码与 Apache-2.0 许可](https://github.com/mit-han-lab/pear) · [训练说明](https://github.com/mit-han-lab/pear/blob/main/docs/getting_started/quickstart.md) · [官方模型入口](https://huggingface.co/collections/mit-han-lab/pear)。本条按开源事件收录，未列为已完成论文精读；未下载或执行训练与权重。

#### 2. 【模仿学习与策略】EgoX：用模态接口连接本体，再预测身体的未来

**来源：** [arXiv:2611.16728v1](https://arxiv.org/abs/2611.16728)（CMU、Bosch、UT Arlington、UC Berkeley、NVIDIA）  
**类型：** Paper · research_paper  
**实际提交时间：** 北京时间 2026-11-12 20:40:24，补充窗口；本期是全文展开，非 14 日新投稿。  
**评分：** 85/100  
**关键词：** Cross-Embodiment · Egocentric Data · Latent Prediction

**核心贡献：** 为本体各模态保留独立观察编码和动作专家，以共享 Transformer 迁移经验，再用训练时的未来本体潜变量监督辅助操作学习。

![EgoX 模态接口、共享主干与未来监督](paper-reading/news/2026-11-14/egox/images/page_005_fig_figure_3_review.png)

- 腕、末端关键点和躯干采用明确的参考坐标系，不把不同机器人的关节硬拼成同一控制向量。新本体仍需人工模态对应、坐标转换和控制器集成。
- EMA 教师提供未来视觉与本体潜变量目标。部署删除未来预测专家与教师，但保留从当前状态聚合本体词元的学生编码器。
- 4,851 条轨迹、34.38 小时数据；五任务、六本体共 13 个组合，五种真机、一种仿真。跨本体预训练使平均**归一化任务进度**从 0.63 到 0.80，分布外从 0.53 到 0.77；附录对应成功率从 0.35 到 0.56，二者不能混用。
- 目标任务示范排除于预训练，之后仍用于微调。分布外相对于该目标任务示范，相关条件可能出现于其他本体数据。七设置 dreaming 消融同时移除整组组件，不能唯一归因于预测损失。

**为什么值得关注：** 共享操作经验需要同时处理语义接口、动力学和数据混合。模块化接口避免粗粒度策略在预训练后某些任务上退化，但论文未证明无需示范即可直接控制全新硬件。

**资源：** [项目页](https://egox-dream.github.io/) · [作者代码入口](https://github.com/egox-dream/egox) · [全文精读](paper-reading/news/2026-11-14/egox/egox.md)。已核对项目页与仓库可达，未运行复现。

#### 3. 【操作与抓取】Reins：让模型动作链随物理检查停止

**来源：** [arXiv:2611.16632v1](https://arxiv.org/abs/2611.16632)（MIT CSAIL、Harvard）  
**类型：** Paper · research_paper  
**实际提交时间：** 北京时间 2026-11-12 19:05:11，补充窗口；本期是全文展开。  
**评分：** 83.5/100  
**关键词：** Guarded Actions · Asynchronous Perception · Long-Horizon

**核心贡献：** 用可测量接触和夹持结果的原子动作组成条件链，失败即停；独立叙述模型持续观察，把决策等待期间发生的变化带回下一轮。

![Reins 的条件动作链和视觉叙述](paper-reading/news/2026-11-14/reins/images/page_001_fig_figure_1_review.png)

- 18 种工具覆盖三维感知、运动、夹爪及任务台账。单链最多八种调用、十六次运行，每步结果必须通过检查，不是开放式重放。
- Sol 在五项双臂真机任务中完成 22/25 回合，即 88%。猜杯完整系统 5/5，去掉叙述者 2/5，去掉 harness 0/5；每条件只有五次，抽屉与扫物提示含抓取、姿态建议。
- 模型等待占总时长 41%–78%。每秒采样并不等于每秒理解；叙述报告仍落后现场约一至两次调用延迟。模型间还使用不同速度档位，不宜将结果当成等时延纯能力排名。
- 单帧重建的孪生里 14 个可动物体中 11 个通过门槛，五场景脚本可完成任务；这套工具**未用于真机评测**，脚本由 mocap 手执行，不能写成仿真规划已提高真实成功率。

**为什么值得关注：** 比扩大动作步长更关键的是保留中间证据、失败停止条件与时间戳。研究仍受单平台、小样本、有限接触反馈和慢叙述限制。

**资源：** [项目页](https://reins-robot.github.io/) · [全文精读](paper-reading/news/2026-11-14/reins/reins.md)。论文写明代码计划发表时发布，本期未确认公开实现，不把演示页当代码开源。

### 📄 论文雷达

本期不重复列入 13 日已详细介绍的 SALA、InneR、ACE-CaP-0、FORGE、HEIR、UAV-Flow++ 等事件。两篇本期重点补充论文已在上方展开。其余补充窗口候选仍有待深入比较，本期不声称全部覆盖，也不以未展开候选推导“没有值得看的论文”。

### 🛠 工程与开源

PEAR 的训练基础设施、部署和模型入口已聚簇为上方一个开源事件，不重复计数。[MuJoCo 官方版本](https://github.com/google-deepmind/mujoco/releases)、[Isaac Lab](https://github.com/isaac-sim/IsaacLab/releases)、[Genesis](https://github.com/Genesis-Embodied-AI/Genesis/releases)、[LeRobot](https://github.com/huggingface/lerobot/releases) 已查；这些已获取的最新 release 均早于本期主窗口，未包装为 14 日新发布。

[SimReady 资产抓放教程](https://huggingface.co/blog/nvidia/simready-assets-robot-pick-and-place)标注 11 月 13 日、无可靠时区；作为补充工程参考。它区分资产 profile 检查与组合场景运行，例子使用固定位置、脚本路径、有限碰撞检查；不证明真机鲁棒性。其信息增量不足以进入本期必读。

### 💬 社区信号

已查询 Hacker News robotics 的近期条目。主窗口所见公司组织调整、配送网络等讨论不作为科研成果收录；候选热度不能替代原文、代码和基准证据。PEAR 仓库星数也不用于证明模型能力。本期未核实到需单列的高价值独立复现或技术争议。

### 🔎 补充窗口筛选记录

- [EgoX](https://arxiv.org/abs/2611.16728)于北京时间 12 日 20:40:24 提交，[Reins](https://arxiv.org/abs/2611.16632)于 12 日 19:05:11 提交：13 日已有简短筛选记录，本期首次在本任务中完成全文笔记，明确标为补记。
- [SALA](https://arxiv.org/abs/2611.17110)于 13 日 01:04:50、[InneR](https://arxiv.org/abs/2611.17159)于 13 日 01:38:48、[FORGE](https://arxiv.org/abs/2611.17142)于 13 日 01:30:11、[HEIR](https://arxiv.org/abs/2611.17238)于 13 日 02:25:41 提交：已有[上一期精读](paper-reading/news/2026-11-13/README.md)，排除重复事件。
- [ACE-CaP-0](https://arxiv.org/abs/2611.16872)于 12 日 22:38:40 提交：上一期已完成全文，本期不重新计为新论文。
- [ProTEUS](https://arxiv.org/abs/2611.13348)于北京时间 10 日 07:19:33 提交：追加月列表分页候选核验显示首次提交在本期窗口之外，且研究对象为蛋白质演化，排除具身智能日报。
- [InstantAMP](https://github.com/RoboticsResearchHubVN/InstantAMP)仓库创建于北京时间 13 日 14:44:30：README 描述可微世界模型和模拟 G1 训练，尚未独立验证“单卡三十分钟”及实现来源边界；按非官方实现候选评价，未达到 T2 入选线，不以标题充当已复现结论。

### 📊 今日技术趋势

本期主窗口确认的新代码是推理模型机器人 RL 的基础设施开放；两篇补记分别强调跨本体学习接口和执行过程中的条件反馈。三者对应训练、迁移和运行时三个不同问题，不能用某一项的成功率替代整个系统的泛化能力。实际部署仍须核对坐标转换、底层控制器、服务延迟和测试条件。

### 来源覆盖与精读状态

- 直接抓取官方 [cs.RO](https://arxiv.org/list/cs.RO/recent)、[cs.AI](https://arxiv.org/list/cs.AI/recent)、[cs.LG](https://arxiv.org/list/cs.LG/recent)、[cs.CV](https://arxiv.org/list/cs.CV/recent) recent 与 11 月列表。月列表另补读 AI 的 443 项和 LG 的 539 项末页，避免前 2,000 项截断。859 个去重预筛候选均取得摘要和版本时间：主窗口 v1 为 0，补充窗口 65，窗口外 794；未发现已核验候选在 14 日的 v2+ 更新。这是已公告列表的核验结果，不是未公告投稿的数量。
- **来源检查不完整：** 最新公告为 13 日，周末投稿可能延后公告。TRI 页面直接请求超时、网页补查仍 403；IROS 403 且补查失败。HF 两个模型 API 请求超时，已改查 NVIDIA、LeRobot 官方组织页，但不能替代完整、带绝对时间的模型更新清单。PI 直接请求 429，网页补查成功。机构首页扫描也不代表全部实验室子项目穷尽。
- 机构及会议扫描含 GEAR、PI、DeepMind、Skild、1X、Figure、RAI、TRI、Stanford、Berkeley、CMU、MIT、上海 AI 实验室、Unitree、CoRL、RSS、ICRA、IROS。相关论文优先回到 PDF 和作者项目页，代码与论文按事件去重。GitHub 主窗口新建与补充窗口仓库均有查询，未以创建时间替代论文首次发表时间。
- 两篇笔记均完成全文与附录核对、grounding、八项笔记 lint、最终质量及中文可读性审查、正式保存和 SHA-256 校验。共 4 张已审图片，0 张占位图。[精读索引](paper-reading/news/2026-11-14/README.md)。PEAR 是本期核验的开源条目，没有冒充全文精读完成。
- 两轮评分向量依次为 significance / novelty / evidence / relevance / community。research_paper 权重 4/3/2/1/0，open_source 为 2/2/2/3/1，engineering_tech 为 3/1/2/3/1。T1≥62、T1.5≥68、T2≥75；未核实社区讨论不给高热度分。

| 事件 | 类型 | 第一轮 | 第二轮 | 平均分 |
| --- | --- | --- | --- | ---: |
| EgoX | research_paper | 9/8/8/10/1 | 8/8/9/10/1 | 85 |
| Reins | research_paper | 8/9/8/10/1 | 8/8/8/10/1 | 83.5 |
| PEAR 代码 | open_source | 9/9/8/10/2 | 9/8/8/10/2 | 83 |
| SimReady 抓放教程 | engineering_tech | 5/4/8/9/2 | 5/4/8/9/2 | 64 |
| InstantAMP 非官方实现 | open_source | 6/6/6/9/1 | 6/6/5/9/1 | 63 |

---

## 历史归档

| 日期 | 日报 | 精读 |
| --- | --- | --- |
| 2026-11-14 | [日报](news/2026-11-14.md) | [2 篇](paper-reading/news/2026-11-14/README.md) |
| 2026-11-13 | [日报](news/2026-11-13.md) | [5 篇](paper-reading/news/2026-11-13/README.md) |
| 2026-11-12 | [日报](news/2026-11-12.md) | [4 篇](paper-reading/news/2026-11-12/README.md) |
| 2026-11-11 | [日报](news/2026-11-11.md) | [5 篇](paper-reading/news/2026-11-11/README.md) |
| 2026-11-10 | [日报](news/2026-11-10.md) | [5 篇](paper-reading/news/2026-11-10/README.md) |
| 2026-11-09 | [日报](news/2026-11-09.md) | [6 篇](paper-reading/news/2026-11-09/README.md) |
| 2026-11-08 | [日报](news/2026-11-08.md) | [1 篇](paper-reading/news/2026-11-08/README.md) |
| 2026-11-07 | [日报](news/2026-11-07.md) | [1 篇](paper-reading/news/2026-11-07/README.md) |
| 2026-11-06 | [日报](news/2026-11-06.md) | [2 篇](paper-reading/news/2026-11-06/README.md) |
| 2026-11-05 | [日报](news/2026-11-05.md) | [2 篇](paper-reading/news/2026-11-05/README.md) |
| 2026-11-04 | [日报](news/2026-11-04.md) | [2 篇](paper-reading/news/2026-11-04/README.md) |
| 2026-11-03 | [日报](news/2026-11-03.md) | [2 篇](paper-reading/news/2026-11-03/README.md) |
| 2026-11-02 | [日报](news/2026-11-02.md) | [3 篇](paper-reading/news/2026-11-02/README.md) |
| 2026-11-01 | [日报](news/2026-11-01.md) | [4 篇](paper-reading/news/2026-11-01/README.md) |
| 2026-10-31 | [日报](news/2026-10-31.md) | [5 篇](paper-reading/news/2026-10-31/README.md) |
| 2026-10-30 | [日报](news/2026-10-30.md) | [5 篇](paper-reading/news/2026-10-30/README.md) |
| 2026-10-29 | [日报](news/2026-10-29.md) | [4 篇](paper-reading/news/2026-10-29/README.md) |
| 2026-10-28 | [日报](news/2026-10-28.md) | [5 篇](paper-reading/news/2026-10-28/README.md) |
| 2026-10-27 | [日报](news/2026-10-27.md) | [3 篇](paper-reading/news/2026-10-27/README.md) |
| 2026-10-26 | [日报](news/2026-10-26.md) | [3 篇](paper-reading/news/2026-10-26/README.md) |
| 2026-10-25 | [日报](news/2026-10-25.md) | [3 篇](paper-reading/news/2026-10-25/README.md) |
| 2026-10-24 | [日报](news/2026-10-24.md) | [3 篇](paper-reading/news/2026-10-24/README.md) |
| 2026-10-23 | [日报](news/2026-10-23.md) | [4 篇](paper-reading/news/2026-10-23/README.md) |
| 2026-10-22 | [日报](news/2026-10-22.md) | [4 篇](paper-reading/news/2026-10-22/README.md) |
| 2026-10-21 | [日报](news/2026-10-21.md) | [7 篇](paper-reading/news/2026-10-21/README.md) |
| 2026-10-20 | [日报](news/2026-10-20.md) | [4 篇](paper-reading/news/2026-10-20/README.md) |
| 2026-10-19 | [日报](news/2026-10-19.md) | [5 篇](paper-reading/news/2026-10-19/README.md) |
| 2026-10-18 | [日报](news/2026-10-18.md) | — |
| 2026-10-17 | [日报](news/2026-10-17.md) | — |
| 2026-10-16 | [日报](news/2026-10-16.md) | [5 篇](paper-reading/news/2026-10-16/README.md) |
| 2026-10-15 | [日报](news/2026-10-15.md) | [5 篇](paper-reading/news/2026-10-15/README.md) |
| 2026-10-14 | [日报](news/2026-10-14.md) | [5 篇](paper-reading/news/2026-10-14/README.md) |
| 2026-10-13 | [日报](news/2026-10-13.md) | — |
| 2026-10-12 | [日报](news/2026-10-12.md) | [5 篇](paper-reading/news/2026-10-12/README.md) |
| 2026-10-11 | [日报](news/2026-10-11.md) | [6 篇](paper-reading/news/2026-10-11/README.md) |
| 2026-10-10 | [日报](news/2026-10-10.md) | [7 篇](paper-reading/news/2026-10-10/README.md) |
| 2026-10-09 | [日报](news/2026-10-09.md) | [6 篇](paper-reading/news/2026-10-09/README.md) |
| 2026-10-08 | [日报](news/2026-10-08.md) | [6 篇](paper-reading/news/2026-10-08/README.md) |
| 2026-10-07 | [日报](news/2026-10-07.md) | [6 篇](paper-reading/news/2026-10-07/README.md) |
| 2026-10-06 | [日报](news/2026-10-06.md) | [6 篇](paper-reading/news/2026-10-06/README.md) |
| 2026-10-05 | [日报](news/2026-10-05.md) | [6 篇](paper-reading/news/2026-10-05/README.md) |
| 2026-10-04 | [日报](news/2026-10-04.md) | [4 篇](paper-reading/news/2026-10-04/README.md) |
| 2026-10-03 | [日报](news/2026-10-03.md) | [4 篇](paper-reading/news/2026-10-03/README.md) |
| 2026-10-02 | [日报](news/2026-10-02.md) | [7 篇](paper-reading/news/2026-10-02/README.md) |

## 目录结构

| 目录 | 内容 |
| --- | --- |
| `news/YYYY-MM-DD.md` | 每日研究动态日报 |
| `paper-reading/news/YYYY-MM-DD/<短slug>/` | 论文精读笔记（`<短slug>.md` + `images/`） |
| `paper-reading/news/YYYY-MM-DD/README.md` | 当日精读索引 |

## 内容许可

- 本仓库全部文字内容（日报与精读笔记）以 [CC BY 4.0](LICENSE) 授权——转载、改写、商用均可，仅需署名。
- 精读笔记中嵌入的论文插图版权归论文原作者 / 出版社所有（figures © original authors），仅作学术评述之引用；本仓库的 CC BY 4.0 授权不覆盖这些图片。

## 自动化

每天北京时间 08:30，无人值守任务生成前一自然日的日报、对入选论文执行全文精读，并把当日日报镜像到本页后提交推送。arXiv 公告存在批次延迟，部分日期的当日投稿只能部分覆盖，具体缺口写在该期日报的「检索覆盖与精读状态」一节。
