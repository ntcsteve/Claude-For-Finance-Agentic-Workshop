# Rescue copies — known-good workshop files

If a file you build during the workshop won't work, copy the matching known-good copy from
here into your project. It's a safety net — you'll learn more by building the files yourself,
but if you're stuck, this keeps you moving.

## How to use

Copy a **skill** file — it takes effect immediately, no restart:
```bash
cp rescue/skills/equity-research/SKILL.md .claude/skills/equity-research/SKILL.md
```

Copy an **agent** file, then restart so Claude Code loads it:
```bash
cp rescue/agents/equity-researcher.md .claude/agents/equity-researcher.md
```
After copying an agent file you must restart before it registers: `/exit`, then
`claude --continue` (or a fresh `claude .`), then `/agents` to confirm it loaded. This can
occasionally take a second restart cycle. See the guide's Concepts section, "Why you
sometimes need to restart" — for an agent, copying the file alone is never enough.

**Lab 6 note:** `rescue/agents/equity-researcher.md` and `equity-validator.md` are the Lab 5
versions — no `Write` tool. If you're rescuing a file mid-Lab 6, copy it, then add `- Write`
to its `tools:` list per Lab 6's instructions (and restart again). The rescue copy alone
won't fix a Lab 6 problem.

## Contents

```
rescue/
├── agents/
│   ├── equity-researcher.md
│   ├── equity-validator.md
│   └── brief-writer.md
└── skills/
    ├── coach/SKILL.md              — the /coach warm-up helper (you build this yourself in the Warm-up)
    ├── equity-research/SKILL.md
    ├── equity-validate/SKILL.md
    ├── brief-writer/SKILL.md
    ├── run-research/SKILL.md
    └── run-research-async/SKILL.md
```

`skills/coach/SKILL.md` is the `/coach` helper you build in the guide's **Warm-up** — it
isn't pre-installed. The copy here is a reference if your coach file breaks.

---

**Facilitator note:** the Lab 2 answer key is deliberately **not** in this repo — it's
gitignored (`rescue/lab2-answer-key.md`) so it stays on the facilitator's machine and never
publishes. The rest of `rescue/` is public on purpose, as the self-rescue safety net above.
