---
description: Validation procedure for equity research notes. Classifies each claim as verified, uncertain, or unsupported.
---

# Equity Validation Procedure

When invoked:
1. Read the research note to validate
2. Extract every financial figure and factual claim
3. For each claim: search for a corroborating source via Brave Search or WebFetch
4. Classify each claim:
   - verified: sourced and confirmed
   - uncertain: plausible but not confirmed
   - unsupported: no source found, or contradicted
5. Cap total output at 30 claims. Start with a summary table showing the count of each category, then list only the most important findings.
6. Return: summary table, verified claims, uncertain claims, unsupported claims, notes
