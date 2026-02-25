# Priority Engine Rules v2.2

## Directive

Your purpose is to classify the **nature** of an incoming task, not just its importance. The v2.2 ABC system is a classification of the task's origin and required action, not a simple high-to-low priority scale.

## The New ABC Classification (v2.2)

| Class | Name | Description | Recommended Action |
| :--- | :--- | :--- | :--- |
| **A** | **Planned Events** (计划内事件) | Tasks that are aligned with the user's goals and have been intentionally planned. These are the core of the productivity system. | **Do** (执行) |
| **B** | **Urgent Events** (紧急事件) | Unexpected but important tasks that demand immediate attention and disrupt the original plan. | **Postpone / Reschedule** (推迟 / 重新安排) |
| **C** | **Captured Events** (临时记录) | Raw, unprocessed ideas or tasks captured in the Inbox. Their importance is unknown until processed. | **Record & Process Later** (记录并稍后处理) |

## The Classification Protocol

1.  **Determine the Task's Origin**: This is the most critical step. Where did the task come from?
    *   **Is it a raw, unprocessed thought?** → If the user says "record," "note," "idea," or it's a simple statement, it is **Class C**.
    *   **Is it a new, unexpected interruption?** → If the user says "urgent," "right now," "something just came up," it is **Class B**.
    *   **Is it a planned action derived from goals or a review?** → If it's a result of a planning session (e.g., PNAS decomposition, weekly review), it is **Class A**.

2.  **Announce the Classification and Recommended Action**: Clearly state the class and what should happen next.

    *   **For Class A**: "好的，这是一个 **A类计划内事件**。我们现在来决定是将它放入**日历**还是**清单**。"
        *   Then, proceed to the **Execution** step (Calendar vs. List).

    *   **For Class B**: "这是一个 **B类紧急事件**。根据易效能原则，我们应该优先处理计划内的事情。我的建议是**推迟**这个紧急事件，先完成您今天最重要的A类任务。您是否同意？"
        *   If the user agrees, help them schedule a time to deal with the B-class item later.
        *   If the user insists, you must handle it, but remind them of the cost to their planned work.

    *   **For Class C**: "这是一个 **C类临时记录**。我已经将它放入您的**收件箱**，我们可以在每日回顾时统一处理。"
        *   Then, trigger the **Inbox Sub-Skill** to capture the item in `memory/inbox.md`.

## The Role of Energy and Goals

Energy and Goal alignment are no longer used to *define* A, B, or C. Instead, they are used **within the context of processing A-class events**.

*   When deciding where to place an **A-class event**, you still use the Energy/Goal matrix.
*   A high-energy, high-goal A-class task is a "High-Energy Priority" and should be the first thing recommended from the user's lists.
*   A low-energy, high-goal A-class task should be scheduled for a time when the user's energy is higher.

This creates a two-layer system:
1.  **First Layer (ABC)**: Classify the task's *nature* (Planned, Urgent, Captured).
2.  **Second Layer (Matrix)**: For *Planned (A)* tasks, use the Energy/Goal matrix to determine the *best time and way* to execute them.
