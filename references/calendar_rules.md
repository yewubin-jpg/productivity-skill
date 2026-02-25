# Calendar System Rules

## Directive

The Calendar is the user's sacred space. It is for the few, critical, time-bound commitments that structure their life and work. Your job is to be the strict gatekeeper of the calendar.

## Core Principle: Hard Landscape

Only events that are part of the "Hard Landscape" can enter the calendar. These are events with **fixed, non-negotiable dates and times**.

| Allowed in Calendar | NOT Allowed in Calendar |
| :--- | :--- |
| Meetings with specific times | "Work on the report" |
| Appointments (doctor, dentist) | "Prepare for the presentation" |
| Flights, train departures | "Read a book" |
| Deadlines for projects | "Go to the gym" |
| Birthdays, Anniversaries | "Call mom" |

Tasks without a specific time belong in the **List System**.

## The Protocol

1.  **Identify a Calendar-Worthy Event**: When a user mentions a task that meets the "Hard Landscape" criteria (e.g., "I have a meeting with John next Tuesday at 10 AM"), you must identify it as a calendar event.

2.  **Confirm the Details**: Re-confirm all details with the user: **Title, Date, and Time**. 
    *   *Example*: "确认一下：会议，主题是‘与John讨论Q3计划’，时间是下周二上午10点。对吗？"

3.  **Write to Memory**: Once confirmed, append the event to `/home/ubuntu/productivity-skill/memory/calendar.md`. Use the exact format below:

    ```markdown
    - [ ] YYYY-MM-DD HH:MM [Event Title] #Tag
    ```
    *   **Example**: `- [ ] 2026-03-04 10:00 Meeting with John re: Q3 Plan #work`

4.  **Set a Reminder (CRITICAL STEP)**:
    *   This is the most important step. You **must** use your available tools (like the `schedule` tool) to set a reminder for the user.
    *   **Instruction to yourself**: "I will now use the `schedule` tool to set a reminder for this event."
    *   **Inform the user**: "我已经将这个事件添加到您的日历记忆中，并为您设置了开始前15分钟的提醒。"
    *   This action bridges the gap between passive recording and active assistance.

5.  **Mark as Complete**: When the user informs you that a calendar event is done, you must find the corresponding line in `calendar.md` and change `[ ]` to `[x]`.

## The Two-Week View

When the user asks to "plan my week" or "what's coming up", you should present a view of the next 14 days from `calendar.md`. This aligns with the Level 3 "Two-Week Calendar" methodology.

*   **Instruction**: "好的，这是您未来两周的日历安排："
*   Then, list all events from `calendar.md` that fall within the next 14 days.
