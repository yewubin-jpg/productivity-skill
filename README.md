# Productivity Skill v2.2 — Intelligent Execution Engine

**[English](./README.md) | [中文](./README_zh.md)**

---

[![GitHub stars](https://img.shields.io/github/stars/yewubin-jpg/productivity-skill.svg?style=social&label=Star)](https://github.com/yewubin-jpg/productivity-skill/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/yewubin-jpg/productivity-skill.svg?style=social&label=Fork)](https://github.com/yewubin-jpg/productivity-skill/network/members)
[![MIT License](https://img.shields.io/badge/license-MIT-green.svg)](https://github.com/yewubin-jpg/productivity-skill/blob/main/LICENSE)
[![ClawHub](https://img.shields.io/badge/ClawHub-productivity--skill-orange.svg)](https://clawhub.ai/)
[![Version](https://img.shields.io/badge/version-2.2-blue.svg)](https://github.com/yewubin-jpg/productivity-skill/releases)

> **Not just knowledge — an AI-powered execution system.** Based on Ye Wubin's (叶武滨) patented time management methodology with 150M+ plays on Ximalaya.

This skill transforms your AI assistant into a **proactive productivity executive** powered by the YiXiaoNeng (易效能) system. It features a universal Inbox for instant capture, the ABC255 classification engine (Do A, Postpone B, Record C), a dual Calendar/List execution system, and persistent long-term memory.

## What's New in v2.2

| Feature | v2.1 | v2.2 |
| :--- | :--- | :--- |
| **ABC Classification** | Energy × Goals matrix | **True ABC255**: A=Planned/Do, B=Urgent/Postpone, C=Captured/Record |
| **Inbox Sub-Skill** | None | **Universal Inbox**: say "record" anytime to instantly capture any thought |
| **List Modes** | Context-only | **Two modes**: Simple (A/B/C lists) for beginners, Advanced (Contextual) for power users |
| **Two-Layer System** | Single classification | **Layer 1**: ABC nature classification. **Layer 2**: Energy/Goals matrix for A-class optimization |
| **3Q4D Processing** | Not integrated | Inbox items processed with **3 Questions + 4D Actions** during reviews |

## The Complete System Architecture

```
                    ┌─────────────┐
                    │   INBOX     │  ← "Record: buy milk" (instant capture)
                    │  (C-Class)  │
                    └──────┬──────┘
                           │ (processed during Review)
                           ▼
┌──────────────────────────────────────────────┐
│            ABC CLASSIFICATION ENGINE          │
│                                              │
│  A = Planned Event → DO                     │
│  B = Urgent Event  → POSTPONE               │
│  C = Captured Event → RECORD (to Inbox)     │
└──────┬───────────────────────┬───────────────┘
       │ A-Class               │ A-Class
       ▼                       ▼
┌──────────────┐     ┌─────────────────┐
│   CALENDAR   │     │     LISTS       │
│  (Commitments│     │  (Flexible)     │
│   Few, Rigid │     │  Many, Adaptive │
│   Auto-Remind│     │                 │
│   FIRST shown│     │  Simple Mode:   │
│              │     │   A/B/C files   │
│              │     │  Advanced Mode: │
│              │     │   @Home @Office │
│              │     │   @Errands etc. │
└──────────────┘     └─────────────────┘
```

## The ABC255 Classification

This is the heart of the system. Every incoming task is classified by its **nature**, not just its importance.

| Class | Name | What It Is | What To Do |
| :--- | :--- | :--- | :--- |
| **A** | Planned Event | A task derived from your goals, plans, or reviews | **Do it** — route to Calendar or List |
| **B** | Urgent Event | An unexpected interruption or someone else's priority | **Postpone it** — protect your A-class plan |
| **C** | Captured Event | A raw thought or idea, importance unknown | **Record it** — goes to Inbox, processed later |

> **Core Principle: Do A, Postpone B, Record C (做A，推B，记C)**

For **A-class tasks**, a second layer of optimization uses the Energy/Goals matrix to determine the best time and method for execution.

## The Inbox: Capture Everything

The Inbox is an always-active sub-skill. Say "record" or "note" at any time, and the AI instantly captures your thought with zero friction — no questions asked, no classification needed. Items are processed later during Daily or Weekly Reviews using the **3 Questions + 4D Actions** framework.

## Calendar vs. Lists

| | **Calendar (Commitments)** | **Lists (Flexible Tasks)** |
| :--- | :--- | :--- |
| **Nature** | Hard landscape — non-negotiable | Soft landscape — do when convenient |
| **Quantity** | Few and precise | Many and adaptive |
| **Time** | Strictly bound to date/time | Optional start/due dates |
| **Display** | **Always shown first** | Shown after calendar, filtered by context |
| **Reminders** | Automatic reminders set | Only when due dates approach |
| **Memory** | Permanent long-term storage | Permanent long-term storage |

## Two List Modes

| Mode | For Whom | How It Works |
| :--- | :--- | :--- |
| **Simple** (Default) | New users, low task volume | Three simple files: `a_tasks.md`, `b_tasks.md`, `c_tasks.md` |
| **Advanced** (Contextual) | Busy users, high task volume | Context-based files: @Home, @Office, @Errands, @Calls, @Computer, @AI, @Waiting, Someday |

The AI will automatically suggest upgrading to Advanced Mode when your lists grow beyond 15 items.

## Quick Start

| Trigger Phrase | What Happens |
| :--- | :--- |
| "Record: buy milk" | **Inbox capture** — instantly saved, no questions asked |
| "Help me plan my day" | **Daily Review**: Calendar first → process Inbox → recommend tasks |
| "I have a new task" | **ABC classification**: determines if it's A (do), B (postpone), or C (record) |
| "Plan my week" | **Weekly Review**: 14-day calendar + full Inbox processing + list review |
| "Meeting Tuesday 3 PM" | **Calendar Track**: stores event + syncs external calendar + sets reminder |
| "I feel exhausted" | Detects low energy, recommends rest, defers A-class tasks |
| "Set up my goals" | Waterdrop 520 goal-setting protocol |

## File Structure

```
productivity-skill/
├── skill.md                         # Core execution logic (the brain)
├── references/
│   ├── inbox_rules.md               # Inbox sub-skill rules (capture & process)
│   ├── priority_engine.md           # ABC255 classification engine
│   ├── energy_engine.md             # Energy assessment rules (L1-L4)
│   ├── goal_engine.md               # Goal management (Waterdrop 520 + Eight Areas)
│   ├── calendar_rules.md            # Calendar system rules (Hard Landscape)
│   ├── list_rules.md                # List system rules (Simple & Advanced modes)
│   ├── core-theory.md               # Nine-Level Performance System theory
│   └── core-methodology.md          # ABC255, PNAS, and more
├── memory/                          # (Created at runtime by the AI)
│   ├── inbox.md                     # Universal capture inbox
│   ├── profile.md                   # User preferences and list mode setting
│   ├── goals.md                     # Annual goals (Waterdrop 520) + Eight Life Areas
│   ├── calendar.md                  # Time-bound events with reminders
│   └── lists/                       # Task lists (Simple or Advanced mode)
├── README.md
├── README_zh.md
└── LICENSE
```

## Installation

**Via ClawHub CLI (Recommended):**
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

## The Origin

This skill is built on the work of **Ye Wubin (叶武滨)**, founder of YiXiaoNeng (易效能). The methodology is protected by **Chinese national invention patents** and is based on 15 years of research, 1000+ live workshops across 10 countries, and millions of practitioners.

Learn more: [www.yixiaoneng.com](https://www.yixiaoneng.com) | Ximalaya: Search "时间管理100讲" (150M+ plays)

## Support This Skill

If this skill has helped you, please consider:

*   **Star** this repository on [GitHub](https://github.com/yewubin-jpg/productivity-skill)
*   **Like** and **Comment** on [ClawHub](https://clawhub.ai)
*   **Share** it with friends who need better time management

> "Every star, share, and review helps more people escape the productivity trap."

## License

MIT License — See [LICENSE](LICENSE) for details.

---

*v2.2 — True ABC255 classification, universal Inbox sub-skill, two-layer priority system, dual list modes, and 3Q4D processing.*
