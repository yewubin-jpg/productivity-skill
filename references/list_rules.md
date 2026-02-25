# List System Rules

## Directive

The List System is the flexible, dynamic counterpart to the rigid Calendar. It is designed to hold all tasks, ideas, and commitments that are not time-bound. You are the manager of this system, ensuring everything is captured, classified, and actionable.

## Core Principle: Soft Landscape

If a task is not a "Hard Landscape" event for the calendar, it belongs here. This is the default destination for most user inputs.

## The File Structure

All lists are stored as separate Markdown files in `/home/ubuntu/productivity-skill/memory/lists/`.

| File | Purpose |
| :--- | :--- |
| `a_tasks.md` | **High-Energy Priority Tasks**. The most important things to do when energy is high. |
| `b_tasks.md` | **Mismatched Tasks**. Important tasks deferred due to low energy. |
| `c_tasks.md` | **Scheduled Distractions**. Low-priority tasks to be done when energy is low. |
| `someday.md` | **Someday/Maybe**. Ideas and tasks with no commitment. To be reviewed monthly. |
| `waiting.md` | **Waiting For**. Tasks delegated to others. Include the person's name and date. |

## The Protocol

1.  **Receive a Task**: A task is routed here from the Priority Engine.

2.  **Classify and Route**: Based on the Class (A, B, C, D) assigned by the Priority Engine, append the task to the correct file.
    *   Class A → `a_tasks.md`
    *   Class B → `b_tasks.md`
    *   Class C → `c_tasks.md`
    *   Class D (if user insists) → `someday.md`

3.  **Use the Standard Format**: All tasks must be recorded in the following format:

    ```markdown
    - [ ] [Task Description] @Context #Tag
    ```
    *   **[Task Description]**: A clear, action-oriented description (e.g., "Draft the Q1 report").
    *   **@Context**: Use T/STEP contexts (`@time`, `@space`, `@tool`, `@energy`, `@people`). This allows for filtering. For example, `@energy(L4)` means this task requires peak energy.
    *   **#Tag**: A project or area tag (e.g., `#marketing`, `#personal`).

4.  **PNAS Decomposition for Large Tasks**:
    *   If a Class A task is large and complex (e.g., "Write a book"), you must ask the user: "这是一个重要项目，我们是否需要使用 PNAS 方法将其分解为更小的行动步骤？"
    *   If they agree, guide them through the PNAS process (Picture → Nouns → Actions → Sequence).
    *   Create a **new project file** for the decomposed steps, e.g., `lists/project_write_book.md`.
    *   Each step in the project file should also follow the standard task format.

5.  **Managing the `waiting.md` List**:
    *   When a user mentions they have delegated a task, ask for details.
    *   **Instruction**: "好的，您已经将 [任务] 委托给了 [谁]。我会将其记录在‘等待清单’中，并标注今天的日期。"
    *   **Format**: `- [ ] Waiting for [Person's Name] to complete [Task] (Delegated on YYYY-MM-DD) #project_tag`

## Review Protocols

*   **Daily Review**: When planning the user's day, present the tasks from `a_tasks.md` as the top priorities. Then, if energy allows, suggest tasks from `b_tasks.md` or `c_tasks.md`.
*   **Weekly Review**: Review all lists. Check for overdue items. Ask the user about items in `waiting.md`. Review the `someday.md` list for any items that have become relevant.
