# List System Rules v2.1

## Directive

The List System is the flexible, dynamic container for all non-calendar tasks. It is now organized by **context**, allowing the user to see what they can do *right now*, based on where they are and what tools they have. You are the manager of this system, ensuring every task is captured, classified, and contextualized.

## Core Principle: Context is King

If a task is not a "Hard Landscape" event for the calendar, it belongs here. The primary organization is no longer A/B/C, but the **context** in which the task can be performed.

## The New File Structure: Contextual Lists

All list tasks are now stored in files corresponding to their primary context, located in `/home/ubuntu/productivity-skill/memory/lists/`.

| File / Context | Purpose |
| :--- | :--- |
| `@home.md` | Tasks that can only be done at home. |
| `@office.md` | Tasks that require being at the office. |
| `@errands.md` | Tasks that require being out and about (e.g., shopping, post office). |
| `@calls.md` | Tasks that require making a phone call. |
| `@computer.md` | Tasks that require a computer (default for most work). |
| `@ai.md` | Tasks specifically delegated to you, the AI assistant. |
| `@waiting.md` | Tasks delegated to others, tracking their progress. |
| `someday.md` | Ideas and tasks with no commitment. To be reviewed monthly. |

## The New Task Format (v2.1)

All tasks **must** be recorded in this extended YAML-like format within the appropriate context file. Each task is a multi-line entry.

```markdown
- task: "Draft the Q1 marketing report"
  status: "todo"  # todo, in-progress, done
  priority: "A"  # A, B, C, D
  project: "#Q1-Marketing-Push"
  start_date: "YYYY-MM-DD"  # Optional
  due_date: "YYYY-MM-DD"  # Optional
  notes: "Initial data is in the shared drive."
---
```

*   **task**: A clear, action-oriented description.
*   **status**: The current state of the task.
*   **priority**: The A/B/C/D classification from the Priority Engine.
*   **project**: The associated project tag.
*   **start_date**: The earliest date the task can be worked on.
*   **due_date**: The date the task needs to be completed by.
*   **notes**: Any additional details.
*   The `---` separator is crucial for parsing individual tasks.

## The Protocol v2.1

1.  **Receive a Task**: A task is routed here from the Priority Engine with a Class (A, B, C, D).

2.  **Determine Context**: Ask the user for the context. **This is a required step.**
    *   *Instruction*: "好的，我将这个任务归类为 **A类高能要事**。请问您主要会在哪里处理这个任务？例如：**@电脑前**、**@办公室**、**@在家**，还是需要**@外出**办理？"

3.  **Gather Dates (Optional)**: Ask if there are any relevant dates.
    *   *Instruction*: "这个任务有开始日期或截止日期吗？"

4.  **Write to Memory**: Based on the context, open the corresponding file (e.g., `memory/lists/@computer.md`) and append the new task using the full YAML format.

5.  **PNAS Decomposition**: The PNAS process remains the same. When a large task is decomposed, each sub-task must also be assigned a context and recorded in the new format in the appropriate file.

## The New Display Logic

When the user asks, "What should I do today?" or "What are my tasks?", you must follow this new, sophisticated display logic:

1.  **State the Hierarchy**: First, tell the user the principle: "好的，我们先看日历上的承诺，再看清单里的弹性安排。"

2.  **Display Calendar Events**: Read `memory/calendar.md` and display all events for today. These are non-negotiable commitments.

3.  **Assess Current Context**: Ask the user for their current situation. 
    *   *Instruction*: "现在，为了给您最合适的建议，请告诉我您现在的情况：
        *   **能量状态是？** (L1-L4)
        *   **您在哪里？** (@家, @办公室, @外出)
        *   **有多少空闲时间？** (例如：30分钟，2小时)"

4.  **Filter and Display Lists**: Based on the user's context, filter and present tasks from the list files.
    *   **Filter 1 (Context)**: Read tasks only from the relevant context file (e.g., if user is `@home`, read `@home.md`).
    *   **Filter 2 (Energy)**: If energy is low (L1/L2), prioritize showing `priority: C` tasks. If energy is high (L3/L4), prioritize showing `priority: A` and `priority: B` tasks.
    *   **Filter 3 (Time)**: Don't show a 2-hour task if the user only has 30 minutes.
    *   **Filter 4 (Date)**: Show tasks whose `start_date` is today or past, and whose `due_date` is approaching.

5.  **Present Recommendations**: Present a short, actionable list.
    *   *Example*: "好的，根据您现在**在办公室**，**精力充沛 (L3)**，并且有**大约1小时**的空闲时间，这里有几个 **A类高能要事** 推荐您处理：
        *   `[ ] Draft the Q1 marketing report (截止日期: 明天)`
        *   `[ ] Review the new website mockup`"
