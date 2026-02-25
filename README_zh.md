# 生产力技能 v2.2 — 智能执行引擎

**[English](./README.md) | [中文](./README_zh.md)**

---

[![GitHub stars](https://img.shields.io/github/stars/yewubin-jpg/productivity-skill.svg?style=social&label=Star)](https://github.com/yewubin-jpg/productivity-skill/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/yewubin-jpg/productivity-skill.svg?style=social&label=Fork)](https://github.com/yewubin-jpg/productivity-skill/network/members)
[![MIT 许可证](https://img.shields.io/badge/license-MIT-green.svg)](https://github.com/yewubin-jpg/productivity-skill/blob/main/LICENSE)
[![ClawHub](https://img.shields.io/badge/ClawHub-productivity--skill-orange.svg)](https://clawhub.ai/)
[![版本](https://img.shields.io/badge/version-2.2-blue.svg)](https://github.com/yewubin-jpg/productivity-skill/releases)

> **不只是知识库 — 这是一个AI驱动的智能执行系统。** 基于叶武滨国家发明专利时间管理方法论，喜马拉雅播放量超1.5亿。

这个技能将您的AI助手转变为一个**主动的生产力执行官**。它具备通用收件箱即时收集、ABC255分类引擎（做A、推B、记C）、日历/清单双轨执行系统，以及持久化长期记忆。

## v2.2 新特性

| 功能 | v2.1 | v2.2 |
| :--- | :--- | :--- |
| **ABC 分类** | 能量×目标矩阵 | **真正的 ABC255**：A=计划内/做，B=紧急/推迟，C=临时/记录 |
| **收件箱子技能** | 无 | **通用收件箱**：随时说"记录"即可瞬间捕获任何想法 |
| **清单模式** | 仅情景模式 | **双模式**：简单模式（A/B/C清单）适合入门，高级模式（情景清单）适合忙碌用户 |
| **双层系统** | 单一分类 | **第一层**：ABC性质分类。**第二层**：能量/目标矩阵优化A类执行 |
| **3问4D处理** | 未集成 | 收件箱项目在回顾时使用**3问+4D**框架处理 |

## 完整系统架构

```
                    ┌─────────────┐
                    │   收件箱     │  ← "记录：买牛奶"（即时捕获）
                    │  （C类事件） │
                    └──────┬──────┘
                           │ （在回顾时处理）
                           ▼
┌──────────────────────────────────────────────┐
│              ABC 分类引擎                     │
│                                              │
│  A = 计划内事件 → 做                         │
│  B = 紧急事件   → 推迟                       │
│  C = 临时记录   → 记录（进入收件箱）          │
└──────┬───────────────────────┬───────────────┘
       │ A类                   │ A类
       ▼                       ▼
┌──────────────┐     ┌─────────────────┐
│    日历       │     │     清单         │
│  （承诺）     │     │  （弹性安排）    │
│  少而精       │     │  多而活          │
│  自动提醒     │     │                 │
│  优先展示     │     │  简单模式：      │
│              │     │   A/B/C 文件     │
│              │     │  高级模式：      │
│              │     │   @在家 @办公室   │
│              │     │   @外出 等       │
└──────────────┘     └─────────────────┘
```

## ABC255 分类系统

这是系统的核心。每个进入的任务按其**性质**分类，而非简单的重要程度。

| 类别 | 名称 | 含义 | 处理方式 |
| :--- | :--- | :--- | :--- |
| **A** | 计划内事件 | 来源于目标、计划或回顾的任务 | **做** — 进入日历或清单 |
| **B** | 紧急事件 | 意外的打断，别人的优先级 | **推迟** — 保护你的A类计划 |
| **C** | 临时记录 | 原始想法或念头，重要性未知 | **记录** — 进入收件箱，稍后处理 |

> **核心原则：做A，推B，记C**

对于 **A类任务**，第二层优化使用能量/目标矩阵来确定最佳执行时间和方式。

## 收件箱：收集一切

收件箱是一个始终活跃的子技能。随时说"记录"或"备注"，AI 会立即捕获您的想法——零摩擦、不提问、不分类。项目在日回顾或周回顾时使用 **3问+4D** 框架统一处理。

**3问**：要不要做？我想要的结果？第一步行动是什么？

**4D**：删除、推迟、委托（含委托AI）、做。

## 日历 vs 清单

| | **日历（承诺）** | **清单（弹性安排）** |
| :--- | :--- | :--- |
| **性质** | 硬性约束，不可协商 | 弹性任务，顺便做 |
| **数量** | 少而精 | 多而活 |
| **时间** | 严格绑定日期和时间 | 可选开始/截止日期 |
| **展示** | **永远优先展示** | 日历之后，按情景过滤展示 |
| **提醒** | 自动设置提醒 | 仅截止日期临近时提醒 |
| **记忆** | 永久长期保存 | 永久长期保存 |

## 两种清单模式

| 模式 | 适合谁 | 工作方式 |
| :--- | :--- | :--- |
| **简单模式**（默认） | 新用户、任务量少 | 三个简单文件：`a_tasks.md`、`b_tasks.md`、`c_tasks.md` |
| **高级模式**（情景） | 忙碌用户、任务量大 | 按情景分文件：@在家、@办公室、@外出、@电话、@电脑、@委托AI、@等待、某天 |

当您的清单超过15项时，AI 会自动建议升级到高级模式。

## 快速开始

| 触发语 | 触发效果 |
| :--- | :--- |
| "记录：买牛奶" | **收件箱捕获** — 瞬间保存，不问任何问题 |
| "帮我规划今天" | **日回顾**：日历优先 → 处理收件箱 → 推荐任务 |
| "我有个新任务" | **ABC分类**：判断是A（做）、B（推迟）还是C（记录） |
| "规划我的一周" | **周回顾**：14天日历 + 全面处理收件箱 + 清单回顾 |
| "下周二下午3点有个会" | **日历轨道**：存储事件 + 同步外部日历 + 设置提醒 |
| "我好累" | 识别低能量，建议休息，推迟A类任务 |
| "设定我的目标" | 水滴520目标设定协议 |

## 文件结构

```
productivity-skill/
├── skill.md                         # 核心执行逻辑（大脑）
├── references/
│   ├── inbox_rules.md               # 收件箱子技能规则（收集与处理）
│   ├── priority_engine.md           # ABC255 分类引擎
│   ├── energy_engine.md             # 能量评估规则 (L1-L4)
│   ├── goal_engine.md               # 目标管理（水滴520 + 八大关注）
│   ├── calendar_rules.md            # 日历系统规则（硬性约束）
│   ├── list_rules.md                # 清单系统规则（简单 & 高级模式）
│   ├── core-theory.md               # 九段效能系统理论
│   └── core-methodology.md          # ABC255、PNAS 等方法论
├── memory/                          # （运行时由AI自动创建）
│   ├── inbox.md                     # 通用收件箱
│   ├── profile.md                   # 用户偏好和清单模式设置
│   ├── goals.md                     # 年度目标（水滴520）+ 八大关注领域
│   ├── calendar.md                  # 有时间约束的事件及提醒
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

*v2.2 — 真正的ABC255分类、通用收件箱子技能、双层优先级系统、双清单模式、3问4D处理。*
