# Claude Code for Finance — Workshop Repo

**Workshop guide:** `docs/participant-guide.md`
**Web version:** `docs/index.html` (a self-contained browser version of the same guide, also servable via GitHub Pages)

Open the guide and follow it from the top. Everything you need is in there.

See `LICENSE.md` before reusing or redistributing anything in this repo.

---

## What is in this repo

| Path | Purpose |
|---|---|
| `docs/participant-guide.md` | Full workshop guide — start here |
| `docs/index.html` | Web version of the guide. Self-contained single page (no dependencies), works offline or via GitHub Pages. Mirrors `participant-guide.md`, so keep the two in sync when either changes. |
| `notes/dbs-excerpt.md` | DBS financial excerpt used in Labs 3–5. **Sample data** — illustrative only, not real-time financials (see the disclaimer at the top of the file) |
| `notes/food-raw.md` | Singapore food notes used in Lab 2. **Contains intentionally incorrect claims** for a hallucination-catching exercise — not accurate food history or trivia |
| `notes/async/` | Empty folder — async pipeline output lands here in Lab 6 |
| `rescue/` | Known-good reference copies of the agent and skill files you build — copy one in if a file you made won't work (see `rescue/README.md`). The Lab 2 answer key is deliberately kept out of this repo. |

## What you will build

A working equity research coordinator that:
- Delegates to three specialist agents (researcher, validator, brief-writer)
- Follows step-by-step research and validation procedures automatically
- Searches live financial news via Brave Search
- Produces a one-page investment brief from a single prompt
- Runs the same pipeline across multiple companies simultaneously

**Final commands:** `/run-research` for one company · `/run-research-async` for multiple at once

---

## Quick start

1. Get the workshop materials from the repo: click **Code → Download ZIP** and unzip it (or `git clone` if you use git) — you'll get a workshop folder
2. Complete the prerequisites in the workshop guide (Claude Code, Node.js, VS Code)
3. Start Claude Code from that folder:
```bash
claude .
```
4. Read the guide's Concepts section first, build your `/coach` helper in the Warm-up, then follow the labs in order starting at Lab 1

If you're comfortable with git, cloning the repo works the same way — see the guide's Prerequisites section for both options.
