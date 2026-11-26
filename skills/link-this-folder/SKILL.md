---
name: link-this-folder
description: Use when the person asks to link the folder they're working in to a Taskigent project, for example "link this folder to Taskigent", "link this folder to my RevnIQ project" or "this folder is my Kids Games project". Saves the folder so "Do now with AI" opens Claude desktop there and AI runs know where to work.
---

# Linking this folder to a Taskigent project

Taskigent can open Claude desktop straight into a project's folder ("Do now with AI"), and AI runs can work in the right place. It only needs to know which folder belongs to which project. You know the folder you're working in, so you can tell it.

## The steps

1. **Find the folder.** Use the full path of the folder this session is working in (the project's main folder, not a sub-folder, unless the person says otherwise). If you can't tell what it is, ask.
2. **Find the project.** If the person named one, use it. If not, call `get_backlog` to see their projects and pick the one whose name clearly matches the folder. If more than one could fit, or none does, ask which project, in one short question.
   - If the project doesn't exist yet, offer to start it with `add_project`, then link it.
3. **Link it.** Call `link_project_folder` with the project name and the full folder path.
4. **Confirm** in one line, for example: "Linked RevnIQ to this folder. Do now with AI on its tasks will open here." If it replaced an older folder, say so.

## Good to know

- One folder per project. Linking again replaces the old one.
- Only link when the person asks. Don't link folders on your own initiative during other work.
- The person can see and change the folder in Taskigent: click the project's colour dot in Tasks.
- Claude desktop always asks the person to confirm a folder from a link before opening it.
