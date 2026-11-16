# Embodied AI & World Models News

> 具身智能与世界模型每日研究动态与论文精读。

**最新一期：2026-11-15** ｜ [日报原文](news/2026-11-15.md) · [历史归档](#历史归档)

---

<!-- 本段由 codex-deployment/update_readme.py 从 news/2026-11-15.md 自动镜像，请勿手工编辑 -->

## 2026-11-15 Embodied AI & World Models Daily

> 主窗口为北京时间 11 月 15 日，补充窗口 13–14 日。来源检查不完整，不能把以下已验证范围解释为全天没有其他资讯。

### 🔥 今日必读

本期未确认需在此展开的重大新论文；工程条目见下。已有论文按事件去重，未为凑数量重发。

### 📄 论文雷达

直接检查四类 arXiv recent 和月列表并核验 902 个去重候选的摘要及版本时间：主窗口首次提交 0，补充窗口 54，窗口外 848。官方公告已到 16 日；公告日期与投稿日期不同，周末未公告投稿仍存在覆盖缺口。AI/LG 月列表仅前 2,000 项，其他补充窗口候选未逐篇完成全文比较，本期不声称穷尽。

### 🛠 工程与开源

#### 【运动与全身控制】M1mic-MLX：把世界模型动作跟踪训练移到 Apple Silicon

**来源：** [作者仓库与训练记录](https://github.com/VittorioPastore/m1mic-mlx)  
**类型：** open_source  
**时间：** 仓库创建于北京时间 2026-11-15 11:14:36；不是论文首发日期。  
**评分：** 77.5/100  
**关键词：** World-Model RL · MLX · Humanoid

**核心贡献：** CPU 运行 MuJoCo 仿真，MLX 在 GPU 上训练世界模型、策略和 critic，通过想象轨迹反向传播优化 G1 全身动作跟踪。

- 作者报告 M1 Pro 16GB、40 段 LAFAN1 动作，79 分钟训练得到归一化回报 0.824、零失败片段；后续检查点保持阈值。内存报告为 2.6GB。这是一台机器的一次训练，未经过本期独立复现，也不是真机成功率。
- 工程改动包括 CPU 仿真线程池、适合 Metal 的小矩阵计算、缩小 batch、限制 MLX 缓存和以 numpy 保存回放。默认使用 1,024 个仿真世界，避免照搬数据中心规模导致共享内存换页。
- README 提供非有限损失跳过、激活梯度修正和评测协议；数值对照是作者自检，不能替代独立验证。实现继承既有可微世界模型训练路线，不能把后端适配称为全新控制算法。

**为什么值得关注：** 为缺少数据中心 GPU 的工程研究提供可检查的训练入口。复用前应核对硬件、数据、批量大小、速度与评测阈值，尤其不能将仿真跟踪成绩推导为部署可靠性。

**资源：** [代码](https://github.com/VittorioPastore/m1mic-mlx) · [作者技术报告](https://www.vittoriopastore.com/m1mic-mlx-report.pdf)。本条仅完成工程说明与公开训练记录阅读，未完成技术报告全文精读，未运行代码。

### 💬 社区信号

已查询 GitHub 与 Hacker News。未以星数、公司组织或产品新闻替代科研证据；暂无已核实、值得单列的独立复现。

### 🔎 补充窗口筛选记录

[PEAR](https://github.com/mit-han-lab/pear)仓库北京时间 14 日 01:43:06 创建，已在[14 日日报](2026-11-14.md)收录，本期排除重复。[13 日精读](paper-reading/news/2026-11-13/README.md)与[14 日精读](paper-reading/news/2026-11-14/README.md)保留原归期，不改写成 15 日新论文。

### 📊 今日技术趋势

本期核验的工程变化在于计算预算与执行后端：将可微世界模型训练拆到 CPU 仿真和笔记本 GPU，收益需要与吞吐、数值稳定性和评测范围一起看。训练回报、跟踪片段失败数与真实操作成功率属于不同证据。

### 来源覆盖与评分

已直接检查 [cs.RO](https://arxiv.org/list/cs.RO/recent)、[cs.AI](https://arxiv.org/list/cs.AI/recent)、[cs.LG](https://arxiv.org/list/cs.LG/recent)、[cs.CV](https://arxiv.org/list/cs.CV/recent) 及月列表；扫描 GEAR、PI、DeepMind、Skild、1X、Figure、RAI、TRI、Stanford、CMU、MIT、上海 AI 实验室等官方入口，及 CoRL/RSS/ICRA/IROS、四个仿真与学习库 release、GitHub 与 HF 渠道。

**来源检查不完整：** PI 429，IROS 403，Berkeley 与 HF 模型 API 超时；机构首页扫描不代表全部子项目覆盖。本期未完成所有补充窗口候选的优先级比较，后续可补记，不应解读为已全面排除。

M1mic-MLX 双评分向量依次为 significance/novelty/evidence/relevance/community：7/8/8/10/2 与 7/7/8/10/3。open_source 权重 2/2/2/3/1，两次 78、77，平均 77.5；官方实现作为一手技术说明，成绩仍保留作者报告边界。

本期新增论文精读 0 篇：收录项按工程实现处理，未将未读全文伪称完成。[本期精读状态](paper-reading/news/2026-11-15/README.md)。

---

## 历史归档

| 日期 | 日报 | 精读 |
| --- | --- | --- |
| 2026-11-15 | [日报](news/2026-11-15.md) | — |
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
