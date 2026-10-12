# Vanilla Sky — Tech Support for Running AI

*How to run a crew of AI agents collaborating on one shared GitHub
repository. A straight, no-fluff tutorial. No personal projects — just
the setup.*

## What you need

- One GitHub repository (private recommended for in-progress work).
- One GitHub account per agent (or one GitHub App per agent).
- A project owner — one human with final say on everything.

## Step 1 — Owner: grant access

No agent can grant itself access. The owner does one of these per agent:

1. **Repo → Settings → Collaborators → Add people** — invite the agent's
   GitHub account with **Write** access.
2. **Or** install the agent's GitHub App on the repo (contents: read/write,
   pull requests: read/write).

Until one of these is done, the agent has no write path.

## Step 2 — Agent: verify access

Each agent, in its own environment:

```
git clone https://github.com/<owner>/<repo>.git
```

Then verify with a **read** before any write: list open pull requests, read
the README. Set identity so history shows who did what:

```
git config --global user.name "<agent-name>"
git config --global user.email "<contact-email>"
```

If the agent has never used GitHub, start with `FIRST_TIME_GITHUB.md`.

## Step 3 — The workflow (standing rules)

- **Check first.** Before starting any task, read the current pull requests,
  branches, and main branch. Someone may already own the lane.
- **Branches, never main.** Name them `<agent>/<topic>-YYYYMMDD`
  (e.g. `builder/login-screen-20261012`).
- **Draft pull requests** for review. "Ready for review" is NOT approval
  to merge.
- **Never merge** without the owner's explicit authorization. Not once.
- **One coordinator relays.** Agents don't task each other directly; the
  owner (or a designated coordinator) passes work between them.
- **Label everything:** APPROVED (owner-stated), INFERENCE, PROPOSAL, OPEN.
  Never present a proposition as approved.

## Step 4 — Status words

Use these precisely so everyone knows the state of a thing:

- **REQUESTED** — asked for, not started
- **CREATED** — exists, not yet verified
- **AVAILABLE** — ready to use
- **TRANSFERRED** — handed off
- **READ-VERIFIED** — someone actually opened and confirmed it

## Troubleshooting

- `403` creating repos: expected. The owner creates repos; agents don't.
- Auth failures on clone/push: access was never granted — back to Step 1.
- Another agent's branch: read it, don't rewrite it. Comment on their PR.
- Merge conflicts: rebase your branch, keep history clean.
- An agent can't reach the private material: it must SAY SO and stop —
  never silently substitute public sources and guess.
