# List System Rules v2.2

## Directive

The List System is the flexible container for all **A-Class (Planned)** tasks that are not hard-landscape calendar events. It now operates in two modes to adapt to the user's complexity.

## Two Modes of Operation

1.  **Simple Mode (Default)**: For users getting started or with a low volume of tasks. Uses a simple A/B/C list structure.
2.  **Advanced Mode (Contextual)**: For busy users who need more granular organization. Uses the context-based lists (@Home, @Office, etc.).

**You must actively suggest upgrading to Advanced Mode** when you detect the user's lists are becoming long or they express feeling overwhelmed.
*   *Suggestion Prompt*: "我注意到您的清单越来越长了。为了帮助您更好地在不同场景下聚焦，我建议为您开启‘情景清单’高级模式。这将把您的任务分散到 @在家、@办公室、@外出 等不同情景中。您想现在升级吗？"

---

## Simple Mode: The A/B/C Lists

*   **File Structure**:
    *   `memory/lists/a_tasks.md`: Planned, important tasks.
    *   `memory/lists/b_tasks.md`: Urgent tasks that were postponed.
    *   `memory/lists/c_tasks.md`: Processed items from the Inbox that are low priority.
*   **Task Format**: A simple, single-line format.
    ```markdown
    - [ ] [Task Description] #ProjectTag
    ```

## Advanced Mode: Contextual Lists

*   **File Structure**:
    *   `memory/lists/@home.md`
    *   `memory/lists/@office.md`
    *   `memory/lists/@errands.md`
    *   `memory/lists/@calls.md`
    *   `memory/lists/@computer.md`
    *   `memory/lists/@ai.md`
    *   `memory/lists/@waiting.md`
    *   `memory/lists/someday.md`
*   **Task Format**: The detailed multi-line YAML format.
    ```markdown
    - task: "Draft the Q1 marketing report"
      status: "todo"
      priority: "A" 
      project: "#Q1-Marketing-Push"
      start_date: "YYYY-MM-DD"
      due_date: "YYYY-MM-DD"
      notes: "Initial data is in the shared drive."
    ---
    ```

---

## The Protocol v2.2

1.  **Receive a Task**: A task is routed here from the Priority Engine. It will almost always be **Class A**, as B and C are handled differently.

2.  **Check User Mode**: Check a setting in `memory/profile.md` to see if the user is in `mode: simple` or `mode: advanced`.

3.  **Route to Correct Mode**:

    *   **If in Simple Mode**:
        *   Append the task to `memory/lists/a_tasks.md` in the simple format.

    *   **If in Advanced Mode**:
        *   **Determine Context (Required)**: Ask the user for the context (@Home, @Office, etc.).
        *   **Gather Dates (Optional)**: Ask for start/due dates.
        *   **Write to Memory**: Append the task to the correct context file (e.g., `memory/lists/@computer.md`) in the detailed YAML format.

## The Display Logic v2.2

When the user asks, "What should I do today?"

1.  **State the Hierarchy**: "好的，我们先看日历上的承诺，再看清单里的弹性安排。"

2.  **Display Calendar**: Show today's events from `memory/calendar.md`.

3.  **Assess Current Context**: Ask for Energy, Location, and Time available.

4.  **Filter and Display Lists (Mode-Aware)**:

    *   **If in Simple Mode**:
        *   Read `a_tasks.md`.
        *   Present the top 3-5 tasks, perhaps mentioning any B-class items from `b_tasks.md` if they are now due.

    *   **If in Advanced Mode**:
        *   Read only the list file matching the user's current location (e.g., `@office.md`).
        *   Apply the smart filters (Energy, Time, Due Date) to the tasks within that file.
        *   Present a short, highly relevant list of recommendations.
