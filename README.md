# Productivity Skill v2.0 — Intelligent Execution Engine

**[English](./README.md) | [中文](./README_zh.md)**

---

[![GitHub stars](https://img.shields.io/github/stars/yewubin-jpg/productivity-skill.svg?style=social&label=Star)](https://github.com/yewubin-jpg/productivity-skill/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/yewubin-jpg/productivity-skill.svg?style=social&label=Fork)](https://github.com/yewubin-jpg/productivity-skill/network/members)
[![MIT License](https://img.shields.io/badge/license-MIT-green.svg)](https://github.com/yewubin-jpg/productivity-skill/blob/main/LICENSE)
[![ClawHub](https://img.shields.io/badge/ClawHub-productivity--skill-orange.svg)](https://clawhub.ai/)
[![Version](https://img.shields.io/badge/version-2.0-blue.svg)](https://github.com/yewubin-jpg/productivity-skill/releases)

> **Not just knowledge — an AI-powered execution system.** Based on Ye Wubin's (叶武滨) patented time management methodology with 150M+ plays on Ximalaya.

This skill transforms your AI assistant into a **proactive productivity executive** that actively manages your tasks, goals, and schedule using the YiXiaoNeng (易效能) system. It assesses your energy, aligns tasks with your goals, and routes them through a dual Calendar/List execution system — all with persistent memory and automatic reminders.

## What's New in v2.0

Version 2.0 is a complete architectural rewrite, evolving from a passive knowledge base into an active, stateful execution engine.

| Feature | v1.x (Knowledge) | v2.0 (Execution) |
| :--- | :--- | :--- |
| **Energy Assessment** | Mentioned in theory | AI actively assesses your L1-L4 state before every decision |
| **Goal Management** | Described the Waterdrop 520 method | AI guides you through the full 520 process and stores goals in persistent memory |
| **Task Classification** | Explained ABC categories | AI uses a decision matrix (Energy × Goals) to automatically classify every task |
| **Calendar** | Described the Two-Week Calendar concept | AI writes events to a persistent calendar file and **sets automatic reminders** |
| **Lists** | Described flexible lists | AI manages 5+ sub-lists (A/B/C/Waiting/Someday) with context tags and PNAS decomposition |
| **Memory** | None | Full persistent memory system: user profile, goals, calendar, and task lists |

## How It Works

The skill follows a strict workflow for every interaction:

```
INPUT → ENERGY ASSESSMENT → GOAL ALIGNMENT → PRIORITY CLASSIFICATION → DUAL-TRACK EXECUTION
```

The **Priority Engine** uses a decision matrix that combines your energy level with goal alignment to classify every task:

| | **High Goal Alignment** | **Low Goal Alignment** |
| :--- | :--- | :--- |
| **High Energy (L3/L4)** | **Class A: High-Energy Priority** → Calendar or A-List | **Class C: Distraction** → C-List or Delete |
| **Low Energy (L1/L2)** | **Class B: Mismatched** → Defer until energy recovers | **Class D: Trivial** → Delete or Delegate |

The **Dual-Track Execution** then routes tasks to the appropriate system:

| Track | Purpose | Characteristics |
| :--- | :--- | :--- |
| **Calendar** | Hard-landscape events | Few, rigid, time-bound. With automatic reminders and long-term memory. |
| **Lists** | Soft-landscape tasks | Many, flexible, actionable. Sorted into A/B/C/Waiting/Someday sub-lists. |

## Quick Start

After installation, simply say one of the following to your AI assistant:

| Trigger Phrase | What Happens |
| :--- | :--- |
| "Help me plan my day" | Daily Review: energy check → calendar overview → top A-tasks |
| "I have a new task" | Full workflow: energy → goals → priority → execution |
| "Plan my week" | Weekly Review: 14-day calendar view + all list reviews |
| "I feel exhausted" | AI detects L1 energy, recommends rest, defers important tasks |
| "Set up my goals" | Waterdrop 520 goal-setting protocol |
| "I have a meeting Tuesday at 3 PM" | Calendar Track: stores event + sets automatic reminder |

## File Structure

```
productivity-skill/
├── skill.md                         # Core execution logic (the brain)
├── references/
│   ├── energy_engine.md             # Energy assessment rules (L1-L4)
│   ├── goal_engine.md               # Goal management (Waterdrop 520 + Eight Areas)
│   ├── priority_engine.md           # High-Energy Priority decision matrix
│   ├── calendar_rules.md            # Calendar system rules (Hard Landscape)
│   ├── list_rules.md                # List system rules (Soft Landscape)
│   ├── core-theory.md               # Nine-Level Performance System theory
│   └── core-methodology.md          # ABC255, PNAS, and more
├── memory/                          # (Created at runtime by the AI)
│   ├── profile.md                   # User energy patterns and preferences
│   ├── goals.md                     # Annual goals (Waterdrop 520) + Eight Life Areas
│   ├── calendar.md                  # Time-bound events with reminders
│   └── lists/
│       ├── a_tasks.md               # High-Energy Priority tasks
│       ├── b_tasks.md               # Deferred important tasks
│       ├── c_tasks.md               # Low-priority tasks
│       ├── someday.md               # Someday/Maybe ideas
│       └── waiting.md               # Delegated tasks
├── README.md
├── README_zh.md
└── LICENSE
```

## Installation

**Via ClawHub CLI (Recommended):**

```shell
npx clawhub@latest install productivity-skill
```

**Via GitHub URL (Paste into your AI assistant's chat):**

```
https://github.com/yewubin-jpg/productivity-skill
```

**Manual Installation:**

```shell
git clone https://github.com/yewubin-jpg/productivity-skill.git
cp -r productivity-skill ~/.openclaw/skills/
```

## The Origin

This skill is built on the work of **Ye Wubin (叶武滨)**, founder of YiXiaoNeng (易效能), China's leading productivity institution.

The methodology is protected by **Chinese national invention patents** and is based on 15 years of research, 1000+ live workshops across 10 countries, and millions of practitioners. The core book "High-Energy Priorities" (《高能要事》) and the Ximalaya course "Time Management 100 Lectures" (《时间管理100讲》) with 150M+ plays form the theoretical foundation.

Learn more: [www.yixiaoneng.com](https://www.yixiaoneng.com) | Ximalaya: Search "时间管理100讲"

## Support This Skill

If this skill has helped you, please consider:

*   **Star** this repository on [GitHub](https://github.com/yewubin-jpg/productivity-skill) to show your support
*   **Like** and **Comment** on [ClawHub](https://clawhub.ai) to help others discover it
*   **Share** it with friends who need better time management
*   **Fork** and contribute improvements

> "Every star, share, and review helps more people escape the productivity trap. Your support means the world to us."

## Contributing

We welcome contributions! Please feel free to submit a pull request or open an issue to discuss your ideas.

## License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.

---

*v2.0 — Complete rewrite: from knowledge base to intelligent execution engine with persistent memory, automatic reminders, and dual Calendar/List system.*
