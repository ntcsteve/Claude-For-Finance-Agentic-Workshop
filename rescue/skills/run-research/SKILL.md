---
description: Full research pipeline for SGX-listed companies. Runs equity-researcher, equity-validator, and brief-writer in sequence to produce a one-page investment brief.
---

# Research Pipeline

When invoked:
1. Convert the company name to a short lowercase slug with no spaces (e.g. "DBS Bank" → "dbs", "OCBC Bank" → "ocbc", "UOB" → "uob"). Use this slug for all file names below.
2. Use the equity-researcher agent to research the named company. Each agent runs in its own separate session and cannot see this conversation. When the agent finishes, write its output to notes/[company]-research.md so the next agent can read it.
3. Use the equity-validator agent to validate notes/[company]-research.md. When the agent finishes, write its output to notes/[company]-validation.md.
4. Use the brief-writer agent to read notes/[company]-research.md and notes/[company]-validation.md and write a one-page investment brief with: a one-line view, summary, key financials table, themes, and risks. Save the brief to notes/[company]-brief.md.
5. Confirm all three files exist by reading each one: notes/[company]-research.md, notes/[company]-validation.md, notes/[company]-brief.md. Report any that are missing.
