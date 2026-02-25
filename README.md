# Productivity Skill v2.1 — Intelligent Execution Engine

**[English](./README.md) | [中文](./README_zh.md)**

---

[![GitHub stars](https://img.shields.io/github/stars/yewubin-jpg/productivity-skill.svg?style=social&label=Star)](https://github.com/yewubin-jpg/productivity-skill/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/yewubin-jpg/productivity-skill.svg?style=social&label=Fork)](https://github.com/yewubin-jpg/productivity-skill/network/members)
[![MIT License](https://img.shields.io/badge/license-MIT-green.svg)](https://github.com/yewubin-jpg/productivity-skill/blob/main/LICENSE)
[![ClawHub](https://img.shields.io/badge/ClawHub-productivity--skill-orange.svg)](https://clawhub.ai/)
[![Version](https://img.shields.io/badge/version-2.1-blue.svg)](https://github.com/yewubin-jpg/productivity-skill/releases)

> **Not just knowledge — an AI-powered execution system.** Based on Ye Wubin's (叶武滨) patented time management methodology with 150M+ plays on Ximalaya.

This skill transforms your AI assistant into a **proactive productivity executive** that actively manages your tasks, goals, and schedule using the YiXiaoNeng (易效能) system. It assesses your energy, aligns tasks with your goals, and routes them through a dual Calendar/List execution system — all with persistent long-term memory, contextual filtering, and automatic reminders.

## What's New in v2.1

Version 2.1 introduces **contextual list management**, **calendar-first display logic**, and **external system integration**.

| Feature | v2.0 | v2.1 |
| :--- | :--- | :--- |
| **List Organization** | A/B/C/Waiting/Someday sub-lists | **Context-based lists**: @Home, @Office, @Errands, @Calls, @Computer, @AI, @Waiting, Someday |
| **Task Dates** | No date support in lists | Each task supports **start_date** and **due_date** |
| **Display Logic** | Simple list display | **Calendar First** → then filtered lists based on energy, context, and time |
| **External Integration** | Internal memory only | **Auto-sync to Google Calendar** and other external tools when available |
| **Smart Filtering** | Manual selection | AI filters tasks by **context + energy + time available + due dates** |

## How It Works

The skill follows a strict workflow for every interaction:

```
INPUT → ENERGY ASSESSMENT → GOAL ALIGNMENT → PRIORITY CLASSIFICATION → DUAL-TRACK EXECUTION
```

### The Priority Engine

The Priority Engine uses a decision matrix combining energy level with goal alignment:

| | **High Goal Alignment** | **Low Goal Alignment** |
| :--- | :--- | :--- |
| **High Energy (L3/L4)** | **Class A: High-Energy Priority** → Calendar or A-List | **Class C: Distraction** → C-List or Delete |
| **Low Energy (L1/L2)** | **Class B: Mismatched** → Defer until energy recovers | **Class D: Trivial** → Delete or Delegate |

### The Dual-Track Execution (v2.1)

| Track | Purpose | Characteristics |
| :--- | :--- | :--- |
| **Calendar** | Hard-landscape events (commitments) | Few, rigid, time-bound. Auto-syncs to external calendars. Sets automatic reminders. Stored in long-term memory. **Always displayed first.** |
| **Lists** | Soft-landscape tasks (flexible) | Many, flexible, actionable. Organized by **context** (@Home, @Office, etc.). Supports start/due dates. Filtered by energy, time, and location. |

### The "What Should I Do?" Logic

When you ask "What should I do today?", the AI follows this precise logic:

1.  **Calendar First**: Shows all committed events for the day. These are non-negotiable.
2.  **Context Check**: Asks where you are (@Home, @Office, etc.), your energy level (L1-L4), and how much time you have.
3.  **Smart Filter**: Reads only the relevant context list, then filters by priority, energy match, time available, and approaching due dates.
4.  **Recommendation**: Presents a short, actionable list of tasks you can do *right now*.

## Context-Based Lists (v2.1)

Tasks are now organized by the **context** where they can be performed:

| Context | File | Example Tasks |
| :--- | :--- | :--- |
| @Home | `@home.md` | Clean the study, organize bookshelf |
| @Office | `@office.md` | Draft Q1 report, review contracts |
| @Errands | `@errands.md` | Buy groceries, pick up dry cleaning |
| @Calls | `@calls.md` | Call dentist, follow up with supplier |
| @Computer | `@computer.md` | Update website, process expense reports |
| @AI | `@ai.md` | Research competitors, summarize meeting notes |
| @Waiting | `@waiting.md` | Waiting for John's feedback, waiting for delivery |
| Someday | `someday.md` | Learn Spanish, write a novel |

Each task includes optional **start_date** and **due_date** fields for time-aware filtering.

## Quick Start

After installation, simply say one of the following:

| Trigger Phrase | What Happens |
| :--- | :--- |
| "Help me plan my day" | Daily Review: Calendar first → context check → smart task recommendations |
| "I have a new task" | Full workflow: energy → goals → priority → context → execution |
| "Plan my week" | Weekly Review: 14-day calendar view + all context list reviews |
| "I feel exhausted" | AI detects L1 energy, recommends rest, defers important tasks |
| "Set up my goals" | Waterdrop 520 goal-setting protocol |
| "Meeting Tuesday 3 PM" | Calendar Track: stores event + syncs to external calendar + sets reminder |
| "What can I do right now?" | Context-aware recommendation based on location, energy, and time |

## File Structure

```
productivity-skill/
├── skill.md                         # Core execution logic (the brain)
├── references/
│   ├── energy_engine.md             # Energy assessment rules (L1-L4)
│   ├── goal_engine.md               # Goal management (Waterdrop 520 + Eight Areas)
│   ├── priority_engine.md           # High-Energy Priority decision matrix
│   ├── calendar_rules.md            # Calendar system rules (Hard Landscape)
│   ├── list_rules.md                # List system rules (Context-based, Soft Landscape)
│   ├── core-theory.md               # Nine-Level Performance System theory
│   └── core-methodology.md          # ABC255, PNAS, and more
├── memory/                          # (Created at runtime by the AI)
│   ├── profile.md                   # User energy patterns and preferences
│   ├── goals.md                     # Annual goals (Waterdrop 520) + Eight Life Areas
│   ├── calendar.md                  # Time-bound events with reminders
│   └── lists/
│       ├── @home.md                 # Tasks for home context
│       ├── @office.md               # Tasks for office context
│       ├── @errands.md              # Tasks requiring going out
│       ├── @calls.md                # Tasks requiring phone calls
│       ├── @computer.md             # Tasks requiring a computer
│       ├── @ai.md                   # Tasks delegated to AI
│       ├── @waiting.md              # Tasks delegated to others
│       └── someday.md               # Someday/Maybe ideas
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

This skill is built on the work of **Ye Wubin (叶武滨)**, founder of YiXiaoNeng (易效能), China's leading productivity institution. The methodology is protected by **Chinese national invention patents** and is based on 15 years of research, 1000+ live workshops across 10 countries, and millions of practitioners. The core book "High-Energy Priorities" (《高能要事》) and the Ximalaya course "Time Management 100 Lectures" (《时间管理100讲》) with 150M+ plays form the theoretical foundation.

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

*v2.1 — Context-based list management, calendar-first display logic, task dates, smart filtering, and external calendar integration.*
