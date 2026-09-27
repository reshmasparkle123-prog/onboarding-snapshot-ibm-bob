# Onboarding Snapshot — IBM Bob 2.0 Hackathon

**Built with IBM Bob IDE** | Category: Developer Onboarding

## The Problem

New developers joining a team routinely lose hours (sometimes days) just
reading through an unfamiliar codebase before they can make their first
meaningful contribution. Existing docs are often outdated, missing, or too
high-level to be actionable.

## What We Built

An onboarding assistant, powered by IBM Bob, that takes a raw repository and
turns it into:

1. **A plain-language architecture explanation** — what the codebase does,
   how a request/data flows through it, and what each major file/module is
   responsible for.
2. **Two concrete, beginner-friendly starter tasks** — real, scoped tasks a
   new developer can complete on day one to build confidence and familiarity
   with the codebase, instead of just reading docs passively.

## How Bob Was Used

We used **Bob IDE's agent mode** to analyze a real, production codebase
(Express.js — a well-known Node.js web framework) end-to-end:

- Bob explored the repo structure (`list_files`, `read_file`, `GetSymbolsOverview`)
  across `lib/`, `test/`, and root config files
- It synthesized this into a structured architecture breakdown, including a
  request-flow diagram
- It then reasoned about the existing test suite patterns to propose two
  starter tasks scoped appropriately for a beginner, each pointing to exact
  files and line numbers

Session evidence is available in [`bob_sessions/`](./bob_sessions), showing
token and Bobcoin usage for this task (22.3k / 270k tokens, 0.211 Bobcoins).

## Impact

- Cuts the "read the whole codebase before touching anything" phase from
  **hours to minutes**
- Gives new devs a *guided first contribution* instead of an overwhelming
  blank slate
- Scales to any repo — not just Express — since the same prompt pattern
  works on any codebase Bob can index

## What's Next (Stretch Goals)

- Calendar-aware task suggestions (flagging tasks that fit before/after a
  new dev's scheduled meetings)
- Automated dev environment setup as part of the onboarding flow
- Integration with deployment downtime, so idle wait-time during builds
  surfaces onboarding tasks for new team members

## Repo Used for Demo

This demo runs against [expressjs/express](https://github.com/expressjs/express),
a well-known open-source Node.js framework, chosen for its real-world
complexity and recognizability to judges.

## Team

Built by Reshma K for the IBM Bob 2.0 Hackathon 