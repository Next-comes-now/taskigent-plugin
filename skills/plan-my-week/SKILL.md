---
name: plan-my-week
description: Use whenever the person works with their Taskigent diary in conversation, for example planning the week, asking what's on today, adding or moving tasks, setting where they're working, making something repeat, ticking things off or habits, reviewing last week, or using the notepad. Explains how Taskigent works so changes land in the right place.
---

# Working with a Taskigent diary

Taskigent is a calm weekly task diary. Use the Taskigent connector's actions. Keep replies short and plain, and say what you changed.

## How the diary is shaped

- **Weeks** run Monday to Sunday, in UK time. `get_week` shows today's date, the big three, each day's tasks, where the person is working, their habits and the Done list.
- **Projects** hold tasks, and each has its own colour. "No project" always exists. `get_backlog` lists open tasks by project.
- **A task** can be planned on a day, repeat on set weekdays, have steps, and be flagged as priority or blocked.
- **The big three** are the week's priorities. There are never more than three.
- **Where you're working** (Home, Studio, London…) belongs to the day. It is not a task.
- **Habits** are ticked or skipped under each day. The person sets them up in the app.
- **The notepad** is free text for each week. The person may call it Scratchpad, Notes, Journal or something else.
- **The Bin** keeps binned tasks for 90 days. Nothing is erased.

## Put things in the right place

- **"I'm working from X on Y"** → `set_place` for that day. Never add a location as a task.
- **Something that happens every week** (Gym on Mon, Wed, Thu) → one task with `update_task` repeat_days. Don't add a copy to each day. If copies already exist, offer to keep one as the repeat and bin the rest.
- **One-off things on a day** → `add_task` with a day, or `plan_task` for an existing task.
- **A big piece of work** → a task with steps (`add_task` with parent_task_id). Ticking the last step ticks off the task.
- **"Make X a priority this week"** → usually `pin_big_three`. If three are already set, ask which one to drop.
- **A thought, idea or note** → `add_to_notepad`. You can only add to the end, never rewrite.
- **"Done" or "skipped" a habit** → `tick_habit`. If the habit doesn't exist, say they can add it in the app.

## Before you change things

- Always use ids from `get_week`, `get_backlog` or `get_bin`. Never guess an id.
- Look before adding, so nothing is doubled. Check the week or backlog for a task with the same name.
- Use the person's own project names. Only start a project (`add_project`) when they ask for one.
- Before several changes at once (planning a whole week, binning a few things), say briefly what you'll do and check first.
- Binning is safe to undo (`restore_task`), but still confirm before binning more than one task.

## Common requests

**Plan my week** (often on Monday morning)
1. `weekly_review` for last week: what got done and what slipped.
2. Offer to carry over what slipped (`plan_task` onto a day this week, or back to the backlog).
3. Agree the big three for this week.
4. Set where they're working each day if they mention it.
5. Spread the rest across the days, keeping each day realistic.
6. Finish with a short summary of the week.

**What's on today?** Call `get_week`. Give today's tasks, big three progress and habits in a few lines.

**Quick capture** ("add call the accountant to Admin"). Use `add_task`. If the project isn't clear, put it in No project, or ask if it obviously belongs somewhere.

## What you can't do

- **Hand a task to AI.** Only the person can, in the app: the ✦ on a task, then **Delegate to AI**. They also write the brief and answer AI questions there.
- Change settings, billing or the account, set up habits, or rename, recolour or bin projects. These are all done in the app.
- Erase anything for good.

If an action you need isn't available, the connection may be older than the latest version. Suggest starting a new chat, or disconnecting and reconnecting Taskigent in Claude's connector settings.
