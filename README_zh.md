# 生产力技能 v2.0 — 智能执行引擎

**[English](./README.md) | [中文](./README_zh.md)**

---

[![GitHub stars](https://img.shields.io/github/stars/yewubin-jpg/productivity-skill.svg?style=social&label=Star)](https://github.com/yewubin-jpg/productivity-skill/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/yewubin-jpg/productivity-skill.svg?style=social&label=Fork)](https://github.com/yewubin-jpg/productivity-skill/network/members)
[![MIT 许可证](https://img.shields.io/badge/license-MIT-green.svg)](https://github.com/yewubin-jpg/productivity-skill/blob/main/LICENSE)
[![ClawHub](https://img.shields.io/badge/ClawHub-productivity--skill-orange.svg)](https://clawhub.ai/)
[![版本](https://img.shields.io/badge/version-2.0-blue.svg)](https://github.com/yewubin-jpg/productivity-skill/releases)

> **不只是知识库 — 这是一个AI驱动的智能执行系统。** 基于叶武滨国家发明专利时间管理方法论，喜马拉雅播放量超1.5亿。

这个技能将您的AI助手转变为一个**主动的生产力执行官**，它会主动评估您的能量状态、将任务与目标对齐，并通过日历/清单双轨制来管理您的所有事务 — 全部具备持久化记忆和自动提醒功能。

## v2.0 重大升级

v2.0 是一次完整的架构重写，从被动的知识库进化为主动的、有状态的智能执行引擎。

| 功能 | v1.x（知识型） | v2.0（执行型） |
| :--- | :--- | :--- |
| **能量评估** | 理论中提及 | AI在每次决策前主动评估您的L1-L4能量状态 |
| **目标管理** | 描述了水滴520方法 | AI引导您完成完整的520流程，并将目标存入持久化记忆 |
| **任务分类** | 解释了ABC分类 | AI使用决策矩阵（能量×目标）自动分类每一个任务 |
| **日历** | 描述了两周日历概念 | AI将事件写入持久化日历文件，并**设置自动提醒** |
| **清单** | 描述了弹性清单 | AI管理5+子清单（A/B/C/等待/某天），支持上下文标签和PNAS分解 |
| **记忆** | 无 | 完整的持久化记忆系统：用户档案、目标、日历、任务清单 |

## 工作原理

技能在每次交互中都遵循严格的工作流：

```
输入 → 能量评估 → 目标对齐 → 优先级分类 → 双轨执行
```

**优先级引擎**使用决策矩阵，结合您的能量水平和目标关联性来分类每一个任务：

| | **高目标关联** | **低目标关联** |
| :--- | :--- | :--- |
| **高能量 (L3/L4)** | **A类：高能要事** → 进入日历或A清单 | **C类：计划中的干扰** → 进入C清单或建议删除 |
| **低能量 (L1/L2)** | **B类：能量错配** → 推迟到能量恢复后 | **D类：琐事** → 建议删除或委托 |

**双轨执行**将任务路由到合适的系统：

| 轨道 | 用途 | 特点 |
| :--- | :--- | :--- |
| **日历** | 硬性约束事件 | 少而精、严格时间绑定、自动提醒、进入长期记忆 |
| **清单** | 弹性任务 | 多而活、灵活分类、可调整、支持PNAS项目分解 |

## 快速开始

安装后，直接对AI助手说以下任何一句话即可触发：

| 触发语 | 触发效果 |
| :--- | :--- |
| "帮我规划今天" | 日回顾：能量检查 → 日历概览 → 今日A类任务 |
| "我有个新任务" | 完整工作流：能量 → 目标 → 优先级 → 执行 |
| "规划我的一周" | 周回顾：两周日历视图 + 全部清单回顾 |
| "我好累" | AI识别L1能量，建议休息，推迟重要任务 |
| "设定我的目标" | 触发水滴520目标设定协议 |
| "下周二下午3点有个会" | 日历轨道：存储事件 + 设置自动提醒 |

## 文件结构

```
productivity-skill/
├── skill.md                         # 核心执行逻辑（大脑）
├── references/
│   ├── energy_engine.md             # 能量评估规则 (L1-L4)
│   ├── goal_engine.md               # 目标管理（水滴520 + 八大关注）
│   ├── priority_engine.md           # 高能要事决策矩阵
│   ├── calendar_rules.md            # 日历系统规则（硬性约束）
│   ├── list_rules.md                # 清单系统规则（弹性任务）
│   ├── core-theory.md               # 九段效能系统理论
│   └── core-methodology.md          # ABC255、PNAS 等方法论
├── memory/                          # （运行时由AI自动创建）
│   ├── profile.md                   # 用户能量节律和偏好
│   ├── goals.md                     # 年度目标（水滴520）+ 八大关注领域
│   ├── calendar.md                  # 有时间约束的事件及提醒
│   └── lists/
│       ├── a_tasks.md               # 高能要事
│       ├── b_tasks.md               # 推迟的重要任务
│       ├── c_tasks.md               # 低优先级任务
│       ├── someday.md               # 某天/也许
│       └── waiting.md               # 委托他人的任务
├── README.md
├── README_zh.md
└── LICENSE
```

## 如何安装

**通过 ClawHub CLI（推荐）：**

```shell
npx clawhub@latest install productivity-skill
```

**通过 GitHub 链接（粘贴到AI助手对话中）：**

```
https://github.com/yewubin-jpg/productivity-skill
```

**手动安装：**

```shell
git clone https://github.com/yewubin-jpg/productivity-skill.git
cp -r productivity-skill ~/.openclaw/skills/
```

## 关于方法论

本技能基于**叶武滨**先生的研究成果。叶武滨是易效能创始人，中国领先的时间管理教育机构创办者。该方法论受**中国国家发明专利**保护，基于15年研究、10个国家1000+场线下工作坊、数百万实践者的经验。核心著作《高能要事》和喜马拉雅课程《时间管理100讲》（播放量超1.5亿，连续两年教育榜第一）构成了理论基础。

了解更多：[www.yixiaoneng.com](https://www.yixiaoneng.com) | 喜马拉雅搜索"时间管理100讲"

## 支持本技能

如果这个技能对您有帮助，请考虑：

*   在 [GitHub](https://github.com/yewubin-jpg/productivity-skill) 上给我们一个 **Star**
*   在 [ClawHub](https://clawhub.ai) 上**点赞**和**评论**
*   **分享**给需要时间管理的朋友
*   **Fork** 并贡献改进

> "每一个Star、分享和评论都能帮助更多人摆脱效率陷阱。您的支持对我们意义重大。"

## 贡献

欢迎贡献！请随时提交Pull Request或开Issue讨论您的想法。

## 许可证

本项目采用 MIT 许可证 — 详见 [LICENSE](LICENSE) 文件。

---

*v2.0 — 完整重写：从知识库升级为智能执行引擎，具备持久化记忆、自动提醒和日历/清单双轨系统。*
