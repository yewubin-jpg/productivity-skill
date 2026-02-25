# Calendar System Rules v2.1

## Directive

The Calendar is the user's sacred space, representing **unbreakable commitments**. It is the absolute source of truth for their schedule. Your job is to be the strict gatekeeper of the calendar and ensure it is always respected as the top priority.

## Core Principle: Calendar First, Always

In any review or planning session, **Calendar events are always presented first**. They are promises the user has made. Lists are flexible tasks to be done *around* these commitments.

| Allowed in Calendar | NOT Allowed in Calendar |
| :--- | :--- |
| Meetings with specific times | "Work on the report" |
| Appointments (doctor, dentist) | "Prepare for the presentation" |
| Flights, train departures | "Read a book" |
| Deadlines for projects | "Go to the gym" |
| Birthdays, Anniversaries | "Call mom" |

Tasks without a specific time belong in the **List System**.

## The Protocol

1.  **Identify a Calendar-Worthy Event**: When a user mentions a task with a specific, non-negotiable date and time, identify it as a calendar event.

2.  **Confirm the Details**: Re-confirm all details: **Title, Date, and Time**.

3.  **Write to Internal Memory**: Append the event to `/home/ubuntu/productivity-skill/memory/calendar.md`. This file is the skill's internal, permanent long-term memory.

    ```markdown
    - [ ] YYYY-MM-DD HH:MM [Event Title] #Tag
    ```
    *   **Example**: `- [ ] 2026-03-04 10:00 Meeting with John re: Q3 Plan #work`

4.  **Set a Reminder (CRITICAL STEP)**:
    *   Use the `schedule` tool to set a reminder for the user. This is non-negotiable.
    *   **Inform the user**: "我已经将这个事件添加到您的日历记忆中，并为您设置了开始前15分钟的提醒。"

5.  **External System Integration (Aspirational)**:
    *   **Check for Tools**: Before writing to the internal memory, check if any external calendar tools (e.g., a Google Calendar MCP server) are available.
    *   **Prioritize External Tools**: If an external tool exists, use it to create the event directly in the user's real calendar. This is the preferred method.
    *   **Inform the User**: "我已经将这个事件直接同步到了您的 Google 日历，并为您设置了提醒。"
    *   **Fallback**: If no external tools are available, fall back to using the internal `calendar.md` memory and the `schedule` tool.

## Long-Term Memory & Display

*   All events in `calendar.md` are **permanent** unless the user explicitly deletes them. You must read this file whenever the user asks about their schedule.
*   When asked to plan a day or week, you will always read from this file first and present its contents before moving on to the flexible list items.
