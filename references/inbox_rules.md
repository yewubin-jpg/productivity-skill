# Inbox Sub-Skill Rules v2.2

## Directive

The Inbox is the system's universal entry point. Its sole purpose is to **capture everything, instantly, without friction**. It is a temporary holding area for any thought, idea, task, or piece of information the user wants to get out of their head. You must make this process as fast and seamless as possible.

## Core Principle: Capture Now, Process Later

Do not attempt to classify, prioritize, or assign context to items entering the Inbox. The goal is speed. The user should be able to say "record this," and you simply write it down. Processing happens later, during a dedicated review session.

## The Inbox File

All captured items are appended to a single, simple text file: `/home/ubuntu/productivity-skill/memory/inbox.md`.

## The Protocol

1.  **Trigger**: The user uses a trigger phrase like "record," "note," "idea," "capture," or simply states a thought they want to save.
    *   *Example*: "Record: need to buy milk."
    *   *Example*: "Idea: what if we used a new marketing slogan?"

2.  **Capture**: Immediately append the user's raw text to `inbox.md`. Add a timestamp.

    ```markdown
    - [ ] YYYY-MM-DD HH:MM - [User's raw text]
    ```
    *   **Example**: `- [ ] 2026-02-27 15:30 - need to buy milk`
    *   **Example**: `- [ ] 2026-02-27 15:31 - Idea: what if we used a new marketing slogan?`

3.  **Confirm**: Provide a brief, non-intrusive confirmation.
    *   *Instruction*: "好的，已记录到收件箱。"

4.  **Do Nothing Else**: Do not ask for context, priority, or dates. The interaction ends here. The sub-skill's job is done.

## The Processing Protocol (During a Review)

The Inbox is processed during a `DAILY_REVIEW` or `WEEKLY_REVIEW`.

1.  **Read the Inbox**: Read all items from `inbox.md`.
2.  **Process One by One**: For each item, ask the user the **3 Core Questions**:
    *   **1. Is it actionable?** (需要我做什么吗？)
        *   If No → Archive it or move to `someday.md`.
        *   If Yes → Proceed to question 2.
    *   **2. What is the desired outcome?** (我想要的结果是什么？)
        *   This helps clarify the task.
    *   **3. What is the next action?** (下一步行动是什么？)
        *   This defines the actual task to be done.
3.  **Classify & Route**: Once the "next action" is defined, route it through the main skill workflow: **PRIORITY ENGINE (ABC) → EXECUTION (Calendar/List)**.
4.  **Clear the Inbox**: Once an item is processed, mark it as done in `inbox.md` by changing `[ ]` to `[x]`.
