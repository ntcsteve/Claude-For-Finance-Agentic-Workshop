---
description: Async research pipeline for SGX-listed companies. Uses the Workflow tool to run equity-researcher, equity-validator, and brief-writer in parallel across multiple companies. Saves all outputs to notes/async/.
---

# Async Research Pipeline

When invoked with a list of companies:
1. Parse the company names from the prompt (comma-separated or bulleted). Convert each company name to a short lowercase slug with no spaces (e.g. "DBS Bank" → "dbs", "OCBC Bank" → "ocbc", "UOB" → "uob"). Use this slug for all file names.
2. Use the Workflow tool to run a parallel pipeline across all named companies with three stages:
   - Stage 1 (Research): for each company, use equity-researcher to research the company. Save to notes/async/[company]-research.md
   - Stage 2 (Validate): for each company, use equity-validator to validate the research note. Save to notes/async/[company]-validation.md
   - Stage 3 (Brief): for each company, use brief-writer to synthesise both outputs into a one-page investment brief with: a one-line view, summary, key financials table, themes, and risks. Save to notes/async/[company]-brief.md
3. Companies move through stages independently — no company waits for another to finish
4. Tell the user to run /workflows to watch live progress
5. When the workflow completes, list all files saved in notes/async/
