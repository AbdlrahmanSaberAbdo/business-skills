---
name: ask-guide
description: Not sure which business-skills skill to run next? Describe where you are with your idea or business and get the next skill (or short sequence) to type. Routes only, never runs the skill.
disable-model-invocation: true
---

# Ask guide

A router over this pack. The user says where they are; you answer with **the next thing to type**. Don't grill, don't do the work, don't open their doc.

## How to answer

1. Place the user on a flow below by situation, not keywords.
2. Name the skill, or a sequence of up to 3, with one line on why each fits now.
3. Mark where a human decision sits ("you decide here").
4. Say whether to continue in this chat or start fresh (see Chat boundaries).
5. End with the exact line to type, with the hub doc link if they have one.

About 8 lines. If it's ambiguous, ask one question with 2–3 options.

## The skills

- **setup-hub**: no hub doc or task sheet yet.
- **grill-plan**: a decision is fuzzy or a plan has holes.
- **to-brief**: something was decided and needs recording.
- **to-tasks**: things to do need turning into rows.
- **next-task**: "what do I work on now?"
- **research-options**: choosing between things that cost money or lock you in.
- **mockup**: the choice is visual.
- **review-against-brief**: something is about to go live or be sent.
- **close-out**: a chat is ending.

## Flows

**Main:** setup-hub → grill-plan (fuzzy parts of the brief) → to-tasks → next-task, one per chat, each ending in close-out → review-against-brief before each launch item.

**On-ramps**
- *Just an idea:* grill-plan first; if it survives, setup-hub (which sends tiny projects back to a plain to-do list).
- *Already running but messy:* setup-hub, telling it what exists, then to-tasks.
- *One big choice blocks everything:* research-options → you decide → to-brief.
- *Something is ready to publish:* review-against-brief → you decide → publish.
- *Changed your mind on a past decision:* to-brief (it sweeps stale text).

**Standalones:** grill-plan, research-options and mockup work without a hub doc.

## Close calls

- **to-brief vs close-out:** one decision mid-chat vs everything at the end.
- **grill-plan vs research-options:** depends on what *you* want vs on facts in the world.
- **to-tasks vs next-task:** plans the work vs does it.
- **mockup vs review-against-brief:** makes options vs checks a finished thing.

## Chat boundaries

1. **Continue here** when the next step is small and uses what this chat knows.
2. **close-out, then fresh chat** when switching workstream or the chat is long. The default.
3. **Fresh chat, no close-out** only when nothing here changed the hub doc or sheet.

## Rules

- Route only to these skills. If nothing fits, say so and suggest doing the work directly.
- For details of a skill, read its SKILL.md; it wins over this summary.
