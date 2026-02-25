# 生产力技能 v2.1 — 智能执行引擎

**[English](./README.md) | [中文](./README_zh.md)**

---

[![GitHub stars](https://img.shields.io/github/stars/yewubin-jpg/productivity-skill.svg?style=social&label=Star)](https://github.com/yewubin-jpg/productivity-skill/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/yewubin-jpg/productivity-skill.svg?style=social&label=Fork)](https://github.com/yewubin-jpg/productivity-skill/network/members)
[![MIT 许可证](https://img.shields.io/badge/license-MIT-green.svg)](https://github.com/yewubin-jpg/productivity-skill/blob/main/LICENSE)
[![ClawHub](https://img.shields.io/badge/ClawHub-productivity--skill-orange.svg)](https://clawhub.ai/)
[![版本](https://img.shields.io/badge/version-2.1-blue.svg)](https://github.com/yewubin-jpg/productivity-skill/releases)

> **不只是知识库 — 这是一个AI驱动的智能执行系统。** 基于叶武滨国家发明专利时间管理方法论，喜马拉雅播放量超1.5亿。

这个技能将您的AI助手转变为一个**主动的生产力执行官**，它会主动评估您的能量状态、将任务与目标对齐，并通过日历/清单双轨制来管理您的所有事务 — 全部具备持久化长期记忆、情景过滤和自动提醒功能。

## v2.1 新特性

v2.1 引入了**情景清单管理**、**日历优先展示逻辑**和**外部系统集成**。

| 功能 | v2.0 | v2.1 |
| :--- | :--- | :--- |
| **清单组织** | A/B/C/等待/某天 子清单 | **情景清单**：@在家、@办公室、@外出、@电话、@电脑、@委托AI、@等待、某天 |
| **任务日期** | 清单无日期支持 | 每个任务支持**开始日期**和**截止日期** |
| **展示逻辑** | 简单列表展示 | **日历优先** → 再根据能量、情景、时间过滤清单 |
| **外部集成** | 仅内部记忆 | **自动同步到 Google 日历**等外部工具 |
| **智能过滤** | 手动选择 | AI 根据**情景 + 能量 + 可用时间 + 截止日期**智能过滤 |

## 工作原理

技能在每次交互中都遵循严格的工作流：

```
输入 → 能量评估 → 目标对齐 → 优先级分类 → 双轨执行
```

### 优先级引擎

使用决策矩阵，结合能量水平和目标关联性来分类任务：

| | **高目标关联** | **低目标关联** |
| :--- | :--- | :--- |
| **高能量 (L3/L4)** | **A类：高能要事** → 进入日历或A清单 | **C类：计划中的干扰** → 进入C清单或删除 |
| **低能量 (L1/L2)** | **B类：能量错配** → 推迟到能量恢复后 | **D类：琐事** → 删除或委托 |

### 双轨执行 (v2.1)

| 轨道 | 用途 | 特点 |
| :--- | :--- | :--- |
| **日历** | 硬性约束事件（承诺） | 少而精、严格时间绑定。自动同步外部日历。设置自动提醒。存入长期记忆。**永远优先展示。** |
| **清单** | 弹性任务（灵活安排） | 多而活、灵活分类。按**情景**组织（@在家、@办公室等）。支持开始/截止日期。根据能量、时间和位置过滤。 |

### "我现在该做什么？"的智能逻辑

当您问"今天该做什么？"时，AI 遵循以下精确逻辑：

1.  **日历优先**：展示今天所有已承诺的事件。这些是不可协商的。
2.  **情景确认**：询问您在哪里（@在家、@办公室等）、能量水平（L1-L4）、有多少空闲时间。
3.  **智能过滤**：只读取相关情景的清单，然后按优先级、能量匹配度、可用时间和临近截止日期过滤。
4.  **推荐**：呈现一个简短的、可执行的任务列表——您*现在*就能做的事。

## 情景清单 (v2.1)

任务现在按**执行情景**组织：

| 情景 | 文件 | 示例任务 |
| :--- | :--- | :--- |
| @在家 | `@home.md` | 整理书房、收拾衣柜 |
| @办公室 | `@office.md` | 撰写Q1报告、审阅合同 |
| @外出 | `@errands.md` | 买菜、取快递、去银行 |
| @电话 | `@calls.md` | 打电话给牙医、跟进供应商 |
| @电脑 | `@computer.md` | 更新网站、处理报销单 |
| @委托AI | `@ai.md` | 竞品调研、会议纪要整理 |
| @等待 | `@waiting.md` | 等待张三的反馈、等待快递 |
| 某天 | `someday.md` | 学西班牙语、写一本小说 |

每个任务包含可选的**开始日期**和**截止日期**字段，支持时间感知过滤。

## 快速开始

安装后，直接对AI助手说以下任何一句话即可触发：

| 触发语 | 触发效果 |
| :--- | :--- |
| "帮我规划今天" | 日回顾：日历优先 → 情景确认 → 智能任务推荐 |
| "我有个新任务" | 完整工作流：能量 → 目标 → 优先级 → 情景 → 执行 |
| "规划我的一周" | 周回顾：14天日历视图 + 全部情景清单回顾 |
| "我好累" | AI识别L1能量，建议休息，推迟重要任务 |
| "设定我的目标" | 触发水滴520目标设定协议 |
| "下周二下午3点有个会" | 日历轨道：存储事件 + 同步外部日历 + 设置提醒 |
| "我现在能做什么？" | 基于情景的智能推荐：根据位置、能量和时间 |

## 文件结构

```
productivity-skill/
├── skill.md                         # 核心执行逻辑（大脑）
├── references/
│   ├── energy_engine.md             # 能量评估规则 (L1-L4)
│   ├── goal_engine.md               # 目标管理（水滴520 + 八大关注）
│   ├── priority_engine.md           # 高能要事决策矩阵
│   ├── calendar_rules.md            # 日历系统规则（硬性约束）
│   ├── list_rules.md                # 清单系统规则（情景清单）
│   ├── core-theory.md               # 九段效能系统理论
│   └── core-methodology.md          # ABC255、PNAS 等方法论
├── memory/                          # （运行时由AI自动创建）
│   ├── profile.md                   # 用户能量节律和偏好
│   ├── goals.md                     # 年度目标（水滴520）+ 八大关注领域
│   ├── calendar.md                  # 有时间约束的事件及提醒
│   └── lists/
│       ├── @home.md                 # 在家情景任务
│       ├── @office.md               # 办公室情景任务
│       ├── @errands.md              # 外出办事任务
│       ├── @calls.md                # 电话任务
│       ├── @computer.md             # 电脑任务
│       ├── @ai.md                   # 委托AI的任务
│       ├── @waiting.md              # 等待他人的任务
│       └── someday.md               # 某天/也许
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

*v2.1 — 情景清单管理、日历优先展示逻辑、任务日期支持、智能过滤和外部日历集成。*
