---
name: next-task
description: Pick the next unblocked task or workstream from a business project's hub doc and task sheet, do the work in this chat, then record the result so the next chat starts from the truth.
---

# Next task

The main loop. One chat, one task or workstream.

## Steps

1. **Read the state.** The hub doc in full, then the task sheet. Trust them over anything remembered from earlier chats.
2. **Find the frontier**: rows with Status To do whose Blocked by tasks are all Done. If the user named a task or workstream, take that.
3. **Claim it.** Say in one line what you're taking and why it's next. Set Status to Doing.
4. **Do the work** until the result is usable, not just a plan. Hand off to the matching skill when one fits:
   - choosing between paid or lock-in options → **research-options**
   - a visual choice → **mockup**
   - anything about to go live or be sent → **review-against-brief**
   - writing or setup in the user's own tools → do it here, paste-ready.
   Stop and ask before anything paid, published, sent, or hard to undo.
5. **Fog** (needs a user decision): ask as in **grill-plan**, one question at a time. If it can't be answered now, add it to Open decisions and carry on with what you can.
6. **Finish with close-out**, even if the work is partial: set the row to Done, or back to To do with a note on what's left.

## Rules

- Stay on one item. If the user drifts, log the new thing as a row and offer it its own chat.
- Flag conflicts with the Brief; don't resolve them silently.
- Check prices, plans and features live before relying on them.
