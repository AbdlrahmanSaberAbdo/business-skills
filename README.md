# business-skills

Agent skills for running a small business project (a SaaS product, an online store, a service or local business, a side venture) across many short AI chats instead of one endless one.

Adapted from [Matt Pocock's skills for coding agents](https://aihero.dev/skills-wayfinder) (`grill-me`, `to-spec`, `to-tickets`, `wayfinder` and friends) for non-code work. Where his skills use a repo and an issue tracker, these use a **hub doc** and a **task sheet**.

Not sure where to start? Type **`/ask-guide`** and describe where you are.

## Mental model

- **The hub doc is the memory.** Standing decisions (Brief), facts that are true now (Done so far), and questions not yet answered (Open decisions). If it isn't in the doc, the next chat doesn't know it.
- **The task sheet is the queue.** One row per action, with blockers. The next thing to do is the first To do row whose blockers are all Done.
- **A chat is a disposable worker.** It reads the doc and sheet, does one item, writes back, and ends. Long chats drift; fresh chats start from the truth.
- **Decide, then record.** Skills that think (`grill-plan`, `research-options`, `mockup`) never write a choice the user hasn't made. Skills that record (`to-brief`, `to-tasks`, `close-out`) never invent one.
- **The human holds the gates.** Anything paid, published, sent, or hard to undo waits for a yes.

## Skills

| Coding flow | Business flow | Use it when |
|---|---|---|
| `setup-…` | `setup-hub` | starting a project (or deciding it's too small for one) |
| `grill-me` | `grill-plan` | a decision is fuzzy |
| `to-spec` | `to-brief` | something was decided and needs recording |
| `to-tickets` | `to-tasks` | work needs breaking into rows |
| `wayfinder` + `implement` | `next-task` | "what now?": picks, does, writes back |
| `research` | `research-options` | choosing between things that cost money or lock you in |
| `prototype` | `mockup` | the choice is visual |
| `code-review` | `review-against-brief` | something is about to go live |
| (session handoff) | `close-out` | a chat is ending |
| `ask-matt` | `ask-guide` | you don't know which of the above |

## The loop

```
setup-hub  →  grill-plan  →  to-brief  →  to-tasks
                                              ↓
         ┌──────────── next-task (one per chat) ────────────┐
         │   research-options / mockup / writing / setup    │
         │   review-against-brief before anything goes live │
         └──────────────────── close-out ───────────────────┘
```

## Blank hub doc

Copy this into any doc tool, or let `setup-hub` build it for you.

````markdown
# [Project name] hub

## How to use this doc
Run each workstream in a fresh chat and paste this doc's link with it.
Before the chat ends, update Done so far and Open decisions (`/close-out`).

## Brief
| Area | Decision |
|---|---|
| Type | [physical / digital / service] · [online / in person / both] |
| Offer | [TBD] |
| Customer | [TBD] |
| Problem it solves | [TBD] |
| Main promise | [TBD] |
| Price and model | [TBD] |
| Market | [TBD] |
| How customers find you | [TBD] |
| Name | [TBD] |
| Feel and voice | [TBD] |
| Budget | [TBD] |
| "Launched" means | [TBD] |
| *(type rows, see below)* | |

## Done so far
| Item | Status |
|---|---|
| | |

## Open decisions
- [ ] 

## Workstreams

### [Workstream name]
```
/next-task [hub doc link]
Workstream: [name]. Outcome: [what "done" looks like].
```
````

Add the rows for your business type:

- **Physical product:** sourcing, stock, sales channel, payment, delivery, returns
- **Digital product (SaaS, app, course):** platform or stack, MVP scope, billing, onboarding, support, data and privacy
- **Service:** who delivers and capacity, packages, booking, contracts, payment
- **In person:** location or area, hours, permits

**Task sheet** columns: `Task | Subtask | Status | Workstream | Blocked by | Notes`. Status is To do, Doing, Blocked or Done.

## Install

One command, for Claude Code, Codex, Cursor, OpenCode and other agents that read skills (needs Node.js 22+):

```bash
npx skills@latest add AbdlrahmanSaberAbdo/business-skills
```

It asks which agents to install for, then copies the skills in. Useful flags:

```bash
npx skills@latest add AbdlrahmanSaberAbdo/business-skills -g               # all your projects, not just this one
npx skills@latest add AbdlrahmanSaberAbdo/business-skills -a claude-code   # one agent only
npx skills@latest add AbdlrahmanSaberAbdo/business-skills --list           # see what's inside first
```

Then type `/ask-guide` in your agent.

**Claude (claude.ai / desktop):** zip each `skills/<name>` folder and upload it as a skill in Settings.

**Manual:** copy the `skills/*` folders into `~/.claude/skills/` (or your agent's skills directory).

Install the whole pack: the skills hand off to each other by name. `grill-plan`, `research-options` and `mockup` also work alone for one-off questions. The agent needs access to a doc it can edit, a spreadsheet it can edit, and, for setup work, a browser.

## Example

Built while launching an Egyptian jewelry brand: the store platform comparison, the logo and palette choice, the policies and the task list all ran through this flow.

## License

MIT
