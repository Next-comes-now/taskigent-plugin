# Taskigent for Claude

[Taskigent](https://taskigent.com) is a calm weekly task diary. Plan your week, hand the right jobs to AI, and tick off the rest.

This plugin connects your diary to Claude:

- **Plan my week:** plan the week, check in on today, capture tasks, set where you're working, make things repeat, tick off tasks and habits, and add to your notepad, all by asking Claude.
- **Do my AI tasks:** Claude picks up the tasks you've handed to AI in Taskigent, does them, and reports back on each task. If it needs you, it asks.
- **Set up my AI tasks routine:** Claude asks when you want it to run (any time of day) and sets up the scheduled routine for you.
- **Link this folder:** in Claude Code, open a project's folder and say *"link this folder to my Taskigent project RevnIQ"*. Then "Do now with AI" opens Claude desktop right there, and AI runs know where to work.

You need a Taskigent account and a paid Claude plan (Pro or above).

## Add it to Claude

**Claude on the web or the desktop app:** Customize → Plugins → add a marketplace → `Next-comes-now/taskigent-plugin` → install **taskigent**.

**Claude Code:**

```bash
claude plugin marketplace add Next-comes-now/taskigent-plugin
```

```bash
claude plugin install taskigent@taskigent
```

The first time Claude uses Taskigent, you'll be asked to sign in to Taskigent and choose what Claude may see:

- **Full diary + handed-off tasks:** for planning and chatting about your week. Claude can also work on the tasks you hand off.
- **Handed-off tasks only:** Claude sees only the tasks you've handed to AI, and nothing else.

Then say *"Set up my AI tasks routine"*.

## You stay in charge

- Only you can hand a task to AI, write its brief, or answer its questions. You do all of that in Taskigent.
- Claude can't erase anything. Binned tasks can be restored for 90 days.
- Claude prepares drafts rather than sending or posting for you, unless your brief says to.
- Every change is signed with the app that made it, and you can disconnect Claude at any time from your Taskigent Account page.

## Questions

hello@taskigent.com · [Privacy](https://taskigent.com/privacy) · [Terms](https://taskigent.com/terms)
