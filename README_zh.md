# 生产力技能 v2.3 — 智能教练

**[English](./README.md) | [中文](./README_zh.md)**

---

[![GitHub stars](https://img.shields.io/github/stars/yewubin-jpg/productivity-skill.svg?style=social&label=Star)](https://github.com/yewubin-jpg/productivity-skill/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/yewubin-jpg/productivity-skill.svg?style=social&label=Fork)](https://github.com/yewubin-jpg/productivity-skill/network/members)
[![MIT 许可证](https://img.shields.io/badge/license-MIT-green.svg)](https://github.com/yewubin-jpg/productivity-skill/blob/main/LICENSE)
[![ClawHub](https://img.shields.io/badge/ClawHub-productivity--skill-orange.svg)](https://clawhub.ai/)
[![版本](https://img.shields.io/badge/version-2.3-blue.svg)](https://github.com/yewubin-jpg/productivity-skill/releases)

> **不只是助手 — 是一个智能生产力教练。** 基于叶武滨国家发明专利时间管理方法论，喜马拉雅播放量超1.5亿。

v2.3 引入了**动态优先级评分引擎**，为每个任务计算 0-100 分的优先级分数，综合考虑您的实时精力、目标、紧急度和情景。您的 AI 助手不再是被动的记录员，而是一个能告诉您**现在该做什么**以及**为什么**的主动教练。

## v2.3 新特性

| 功能 | v2.2 | v2.3 |
| :--- | :--- | :--- |
| **任务推荐** | 静态能量/目标矩阵 | **动态优先级分数 (0-100)**，由4个加权维度计算 |
| **能量评估** | 单一 L1-L4 等级 | **三维评估**：当前状态 + 时间节律 + 历史反馈 |
| **推荐风格** | "这是您的任务" | **"任务X得分95，因为..."** — 有理有据的教练式推荐 |
| **学习能力** | 无 | **自我进化**：通过 `task_history.md` 从任务完成反馈中学习 |
| **备选方案** | 无 | 始终展示**前3个任务及其分数**，供用户选择 |

## 优先级评分引擎

这是 v2.3 的核心创新。对于每一个 A 类（计划内）任务，引擎计算：

`优先级分数 = (能量分数 * 40%) + (目标分数 * 40%) + (紧急度分数 * 15%) + (情景分数 * 5%)`

### 四大评分维度

| 维度 | 权重 | 衡量什么 | 关键因素 |
| :--- | :--- | :--- | :--- |
| **能量分数** | 40% | 您现在能做好这个任务吗？ | 当前 L1-L4 等级、时间节律匹配、历史成功经验 |
| **目标分数** | 40% | 这个任务能推动您的目标吗？ | 核心5大目标关联、八大关注领域、语义相似度、"临门一脚"奖励 |
| **紧急度分数** | 15% | 这个任务有多紧迫？ | 截止日期临近度、活跃时间窗口 |
| **情景分数** | 5% | 您现在能在这里做这个任务吗？ | 位置/情景匹配（@在家、@办公室等） |

### 推荐示例

> "根据您目前的 L4 能量状态、上午的精力高峰期，以及这个任务与您'完成Q1报告'的核心目标直接相关，我计算出**'起草报告初稿'**是您当前最高分的任务（95分）。我建议您现在就集中精力处理它。
>
> 备选方案：'准备周五的演示文稿'（82分）、'回复CEO的邮件'（75分）。"

## 完整系统架构

```
                    ┌─────────────┐
                    │   收件箱     │  ← "记录：买牛奶"（即时捕获）
                    │  （C类事件） │
                    └──────┬──────┘
                           │ （在回顾时处理）
                           ▼
┌──────────────────────────────────────────────┐
│          ABC 分类引擎（第一层）                │
│  A = 计划内 → 做    B = 紧急 → 推迟           │
│  C = 临时记录 → 进入收件箱                     │
└──────┬───────────────────────┬───────────────┘
       │ A类                   │ A类
       ▼                       ▼
┌──────────────┐     ┌─────────────────────────┐
│    日历       │     │   优先级评分引擎          │
│  （承诺）     │     │     （v2.3 全新）        │
│  少而精       │     │                         │
│  自动提醒     │     │  能量分数      (40%)    │
│  优先展示     │     │  目标分数      (40%)    │
│              │     │  紧急度分数    (15%)    │
│              │     │  情景分数       (5%)    │
│              │     │         ↓               │
│              │     │  排序后的任务列表         │
│              │     │  "现在做这个（95分）"     │
└──────────────┘     └─────────────────────────┘
```

## 三维能量评估

v2.3 从三个维度评估能量，而不仅仅是一个等级。

| 维度 | 捕捉什么 | 如何使用 |
| :--- | :--- | :--- |
| **当前状态 (L1-L4)** | 用户此刻的感受 | 基础能量分数 |
| **时间节律（生物钟）** | 用户的自然精力高峰/低谷时段 | 节律匹配 +15 分，不匹配 -15 分 |
| **历史反馈** | 过去的成功/失败模式 | 历史成功条件 +10 分 |

## 快速开始

| 触发语 | 教练会做什么 |
| :--- | :--- |
| "记录：买牛奶" | **收件箱捕获** — 瞬间保存，不问任何问题 |
| "我现在该做什么？" | **完整评分**：评估能量 → 为所有任务计算分数 → 推荐最高分任务并解释原因 |
| "帮我规划今天" | **日回顾**：先展示日历 → 处理收件箱 → 评分排序所有任务 |
| "我好累" | 识别 L1 状态，建议休息，推迟所有高耗能任务 |
| "设定我的目标" | 水滴520目标设定协议 |

## 文件结构

```
productivity-skill/
├── skill.md                         # 核心执行逻辑（大脑）
├── references/
│   ├── priority_engine.md           # 动态优先级评分引擎（v2.3）
│   ├── energy_engine.md             # 三维能量评估（v2.3）
│   ├── inbox_rules.md               # 收件箱子技能规则
│   ├── goal_engine.md               # 目标管理（水滴520 + 八大关注）
│   ├── calendar_rules.md            # 日历系统规则
│   ├── list_rules.md                # 清单系统规则（简单 & 高级模式）
│   ├── core-theory.md               # 九段效能系统理论
│   └── core-methodology.md          # ABC255、PNAS 等方法论
├── memory/                          # （运行时由AI自动创建）
│   ├── inbox.md                     # 通用收件箱
│   ├── profile.md                   # 用户偏好 + 能量节律
│   ├── goals.md                     # 年度目标 + 八大关注领域
│   ├── calendar.md                  # 有时间约束的事件及提醒
│   ├── task_history.md              # （新增）任务完成反馈，用于学习
│   └── lists/                       # 任务清单（简单或高级模式）
├── README.md
├── README_zh.md
└── LICENSE
```

## 如何安装

**通过 ClawHub CLI（推荐）：**
```shell
npx clawhub@latest install productivity-skill
```

**通过 GitHub 链接：**
```
https://github.com/yewubin-jpg/productivity-skill
```

**手动安装：**
```shell
git clone https://github.com/yewubin-jpg/productivity-skill.git
cp -r productivity-skill ~/.openclaw/skills/
```

## 关于方法论

本技能基于**叶武滨**先生的研究成果。叶武滨是易效能创始人，中国领先的时间管理教育机构创办者。该方法论受**中国国家发明专利**保护，基于15年研究、10个国家1000+场线下工作坊、数百万实践者的经验。

了解更多：[www.yixiaoneng.com](https://www.yixiaoneng.com) | 喜马拉雅搜索"时间管理100讲"（播放量超1.5亿）

## 支持本技能

如果这个技能对您有帮助，请考虑：

*   在 [GitHub](https://github.com/yewubin-jpg/productivity-skill) 上给我们一个 **Star**
*   在 [ClawHub](https://clawhub.ai) 上**点赞**和**评论**
*   **分享**给需要时间管理的朋友

> "每一个Star、分享和评论都能帮助更多人摆脱效率陷阱。您的支持对我们意义重大。"

## 许可证

MIT 许可证 — 详见 [LICENSE](LICENSE) 文件。

---

*v2.3 — 动态优先级评分引擎、三维能量评估、自我进化任务历史、教练式推荐。*
