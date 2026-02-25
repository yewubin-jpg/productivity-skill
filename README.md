# Productivity Skill v2.3 — The Intelligent Coach

**[English](./README.md) | [中文](./README_zh.md)**

---

[![GitHub stars](https://img.shields.io/github/stars/yewubin-jpg/productivity-skill.svg?style=social&label=Star)](https://github.com/yewubin-jpg/productivity-skill/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/yewubin-jpg/productivity-skill.svg?style=social&label=Fork)](https://github.com/yewubin-jpg/productivity-skill/network/members)
[![MIT License](https://img.shields.io/badge/license-MIT-green.svg)](https://github.com/yewubin-jpg/productivity-skill/blob/main/LICENSE)
[![ClawHub](https://img.shields.io/badge/ClawHub-productivity--skill-orange.svg)](https://clawhub.ai/)
[![Version](https://img.shields.io/badge/version-2.3-blue.svg)](https://github.com/yewubin-jpg/productivity-skill/releases)

> **Not just an assistant — an intelligent productivity coach.** Based on Ye Wubin's national invention patent methodology. 150M+ plays on Ximalaya.

v2.3 introduces a **Dynamic Priority Scoring Engine** that calculates a 0-100 score for every task based on your real-time energy, goals, urgency, and context. Your AI assistant is no longer a passive recorder — it's a proactive coach that tells you *exactly* what to do next and *why*.

## What's New in v2.3

| Feature | v2.2 | v2.3 |
| :--- | :--- | :--- |
| **Task Recommendation** | Static Energy/Goal matrix | **Dynamic Priority Score (0-100)** calculated from 4 weighted dimensions |
| **Energy Assessment** | Single L1-L4 level | **Three-dimensional**: Current State + Time Rhythm (Chronotype) + Historical Feedback |
| **Recommendation Style** | "Here are your tasks" | **"Task X scores 95 because..."** — justified, transparent, coach-like |
| **Learning Ability** | None | **Self-improving**: Learns from task completion feedback via `task_history.md` |
| **Alternatives** | None | Always presents **top 3 tasks with scores** for user choice |

## The Priority Scoring Engine

This is the core innovation of v2.3. For every A-class (Planned) task, the engine calculates:

`Priority Score = (Energy * 40%) + (Goals * 40%) + (Urgency * 15%) + (Context * 5%)`

### The Four Scoring Dimensions

| Dimension | Weight | What It Measures | Key Factors |
| :--- | :--- | :--- | :--- |
| **Energy Score** | 40% | Can you do this task well *right now*? | Current L1-L4 level, chronotype match, historical success with similar tasks |
| **Goal Score** | 40% | Does this task move you toward your goals? | Core 5 goal alignment, Eight Life Areas, semantic similarity, "Finisher" bonus |
| **Urgency Score** | 15% | How time-sensitive is this task? | Due date proximity, active time windows |
| **Context Score** | 5% | Can you do this task *here*? | Location/context match (@Home, @Office, etc.) |

### Example Recommendation

> "Based on your current L4 energy state, your morning peak period, and the direct alignment with your core goal 'Complete Q1 Report', I calculate that **'Draft the report outline'** is your highest-scoring task right now (PS: 95). I recommend focusing on it immediately.
>
> Alternatives: 'Prepare Friday presentation' (PS: 82), 'Reply to CEO email' (PS: 75)."

## Complete System Architecture

```
                    ┌─────────────┐
                    │   Inbox     │  ← "Record: buy milk" (instant capture)
                    │  (C-class)  │
                    └──────┬──────┘
                           │ (processed during Review)
                           ▼
┌──────────────────────────────────────────────┐
│         ABC Classification (Layer 1)          │
│  A = Planned → Do    B = Urgent → Postpone    │
│  C = Captured → Record in Inbox               │
└──────┬───────────────────────┬───────────────┘
       │ A-class               │ A-class
       ▼                       ▼
┌──────────────┐     ┌─────────────────────────┐
│   Calendar   │     │  Priority Scoring Engine │
│ (Commitments)│     │      (v2.3 NEW)         │
│ Hard, few    │     │                         │
│ Auto-remind  │     │  Energy Score    (40%)  │
│ Show first   │     │  Goal Score      (40%)  │
│              │     │  Urgency Score   (15%)  │
│              │     │  Context Score    (5%)  │
│              │     │         ↓               │
│              │     │  Sorted Task List       │
│              │     │  "Do THIS next (95pt)"  │
└──────────────┘     └─────────────────────────┘
```

## Three-Dimensional Energy Assessment

v2.3 assesses energy across three dimensions, not just one.

| Dimension | What It Captures | How It's Used |
| :--- | :--- | :--- |
| **Current State (L1-L4)** | How the user feels right now | Base energy score |
| **Time Rhythm (Chronotype)** | User's natural peak/trough periods | +15 bonus for rhythm match, -15 for mismatch |
| **Historical Feedback** | Past success/failure patterns | +10 bonus for historically successful conditions |

## Quick Start

| You Say... | The Coach Does... |
| :--- | :--- |
| "Record: buy milk" | **Inbox capture** — instant, no questions |
| "What should I do now?" | **Full scoring**: Assess energy → Calculate PS for all tasks → Recommend top task with explanation |
| "Plan my day" | **Daily Review**: Calendar first → Process inbox → Score and rank all tasks |
| "I'm exhausted" | Detects L1, recommends rest, defers all high-effort tasks |
| "Set my goals" | Waterdrop 520 goal-setting protocol |

## File Structure

```
productivity-skill/
├── skill.md                         # Core execution logic (the brain)
├── references/
│   ├── priority_engine.md           # Dynamic Priority Scoring Engine (v2.3)
│   ├── energy_engine.md             # Three-dimensional energy assessment (v2.3)
│   ├── inbox_rules.md               # Inbox sub-skill rules
│   ├── goal_engine.md               # Goal management (Waterdrop 520 + Eight Areas)
│   ├── calendar_rules.md            # Calendar system rules
│   ├── list_rules.md                # List system rules (Simple & Advanced)
│   ├── core-theory.md               # Nine-Level Performance System theory
│   └── core-methodology.md          # ABC255, PNAS methodologies
├── memory/                          # (Auto-created at runtime by AI)
│   ├── inbox.md                     # Universal inbox
│   ├── profile.md                   # User preferences + energy rhythm
│   ├── goals.md                     # Annual goals + Eight Life Areas
│   ├── calendar.md                  # Time-bound events with reminders
│   ├── task_history.md              # (New) Task completion feedback for learning
│   └── lists/                       # Task lists (Simple or Advanced mode)
├── README.md
├── README_zh.md
└── LICENSE
```

## Installation

**Via ClawHub CLI:**
```shell
npx clawhub@latest install productivity-skill
```

**Via GitHub URL:**
```
https://github.com/yewubin-jpg/productivity-skill
```

**Manual:**
```shell
git clone https://github.com/yewubin-jpg/productivity-skill.git
cp -r productivity-skill ~/.openclaw/skills/
```

## About the Methodology

This skill is based on the research of **Ye Wubin** (叶武滨), founder of YiXiaoNeng and China's leading time management educator. The methodology is protected by **Chinese National Invention Patent**, built on 15 years of research, 1000+ workshops across 10 countries, and millions of practitioners.

Learn more: [www.yixiaoneng.com](https://www.yixiaoneng.com) | Search "时间管理100讲" on Ximalaya (150M+ plays)

## Support This Skill

If this skill has helped you, please consider:

*   Giving us a **Star** on [GitHub](https://github.com/yewubin-jpg/productivity-skill)
*   **Liking** and **Commenting** on [ClawHub](https://clawhub.ai)
*   **Sharing** with friends who need better time management

> "Every Star, share, and comment helps more people escape the productivity trap. Your support means the world to us."

## License

MIT License — see [LICENSE](LICENSE) file.

---

*v2.3 — Dynamic Priority Scoring Engine, Three-Dimensional Energy Assessment, Self-Improving Task History, Coach-Style Recommendations.*
