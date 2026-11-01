---
name: setup-hub
description: Start a business project (brand, store, side venture) by creating its hub doc and task sheet, so every later chat can pick up from one source of truth.
---

# Set up the hub

Run once per project. It creates the two things every later chat reads and writes: the **hub doc** and the **task sheet**. The other skills in this pack assume the structure below.

## Too small for a hub?

If the project is one product, one channel, or a weekend test, don't build a hub. Say so, keep a short to-do list in the chat, and stop. Suggest running this skill again if it grows past what one chat can hold.

## The hub doc

Any editable doc the agent can read and write. Five sections, in this order:

1. **How to use this doc**: one paragraph. Run each workstream in a fresh chat with this doc's link; update Done so far and Open decisions before the chat ends.
2. **Brief**: table (Area | Decision) of standing choices: what is sold, to whom, price range, market, sourcing, main promise, name, feel, logo, palette, voice, payment, delivery, platform, budget. Write [TBD] for anything undecided. Never invent a decision.
3. **Done so far**: table (Item | Status) of facts true now, each dated, with links instead of content.
4. **Open decisions**: checklist of precisely worded questions.
5. **Workstreams**: one heading each, with a starter prompt in a code block naming the doc link and the expected outcome.

## The task sheet

Any spreadsheet the agent can edit. Columns: **Task | Subtask | Status | Workstream | Blocked by | Notes**.

- Status: To do, Doing, Blocked, Done.
- A task with subtasks repeats its name on every subtask row, so the sheet filters cleanly.
- Blocked by lists the tasks that must be Done first.

## Steps

1. Ask what already exists (doc, sheet, store, handles, logo). Extend it rather than duplicating it. If the user mentions a doc or sheet without a link, ask for the link.
2. Interview one question at a time, about 8 at most, until every Brief row is filled or [TBD]. Apply the **too small** check as the answers come in.
3. Create the hub doc.
4. Pick workstreams that fit this business (typically identity, social, store, sourcing, pricing, delivery and policies, launch content) and write a starter prompt for each.
5. Fill the task sheet as in **to-tasks**.
6. Name the first workstream and give the exact line to paste into a fresh chat.

## Rules

- Plain words, readable on a phone.
- Ask before creating accounts, paying, or publishing.
