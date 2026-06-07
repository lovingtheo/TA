---
name: data-reviewing
description: Reviews tagged transcript outputs for errors, inconsistencies, and codebook drift. Run after data-tagging.
---

## Setup

1. **If reviewing 3 or more transcripts:** launch an Explore agent first with this exact task:

   > For each file in `outputs/analysis/`, return a per-transcript table in this exact format — no prose, no rationale, no definitions, nothing else:
   >
   > ### [transcript filename]
   > | Code | # Quotes | Strong | Moderate | Tentative | 4+ tag turns |
   > |------|----------|--------|----------|-----------|--------------|
   > | ... | ... | ... | ... | ... | ... |
   >
   > After all per-transcript tables, return one corpus summary table:
   >
   > ### Corpus Summary
   > | Code | Total Quotes | Transcripts Used In | Avg per Transcript |
   > |------|-------------|---------------------|--------------------|
   > | ... | ... | ... | ... |
   >
   > Do not return any quote text, rationale, or prose. Tables only.

   Use the Explore agent's output as input to all review checks — do not load full transcript files into context.
2. **If reviewing 1–2 transcripts:** read `outputs/analysis/` files directly.
3. Read `.claude/rules/predefined-codes` — load the codebook

---

## Checks

### Structural
- Missing fields: quote, tag, transcript ID, or speaker label
- Unknown tags: not in codebook and not flagged as emergent
- Duplicate quote-tag pairs
- Empty segments (< 5 words)

### Distribution
- Tag applied to > 40% of all quotes → possible over-application
- Tag applied only once with no rationale → orphan code
- Transcript with unusually low coded/total-turns ratio → possible under-tagging
- Segments with 4+ tags → flag for review

### Consistency
- Semantically similar quotes tagged differently → inconsistency
- Quotes semantically distant from their tag's other quotes → possible misfit
- **Codebook drift:** For each emergent code, load its anchor example from `memory/emergent_codes.md`. Compare the anchor against quotes applied to the same code in the 3 most recent transcripts. If recent quotes feel semantically distant from the anchor — different context, different participant behaviour, broader or narrower scope — flag as drift. Report the anchor, the diverging quote, and the transcript gap between them.

### Codebook Integrity
- Emergent code with > 60% quote overlap with an existing predefined code → flag for merger
- Predefined code never applied → flag as unused

---

## Issue Types and Severity

| Issue | Severity |
|---|---|
| Misfit — quote contradicts tag definition | Critical |
| Inconsistency — similar quotes tagged differently | High |
| Under-tag — clear theme left untagged | High |
| Codebook drift — tag applied with evolved meaning | High |
| Ambiguous boundary — segment too long or too short | Moderate |
| Orphan code — emergent code on one quote, no rationale | Moderate |
| Over-tag — 3+ tags where 1-2 would suffice | Low |

**Tiers:**
- **Tier 1 (Critical):** Quote contradicts the tag definition — auto-flag with high confidence
- **Tier 2 (Debatable):** Plausible but an alternative fits equally well — requires human adjudication
- **Tier 3 (Stylistic):** Defensible but reflects a coding preference — note only

---

## Output

Save to `outputs/reviews/transcript-N-review.md` as a markdown report using this structure:

```
# Tag Review Report
Date: [date] | Transcripts: [N] | Coded segments: [N]

## Summary
- Critical: [N] | High: [N] | Moderate: [N] | Low: [N]
- Systemic issues: [N] | Must-fix: [N] | Optional: [N]

---

## Systemic Issues — fix these first
Patterns where one root cause is responsible for flags across multiple transcripts.
Resolving each may clear multiple individual flags below.

| # | Root Cause | Flags Affected | Transcripts | Recommended Action |
|---|-----------|----------------|-------------|-------------------|
| 1 | ... | N quotes | N transcripts | ... |

If no systemic issues: write "None identified."

---

## Must-Fix
*Analysis is not defensible until all items in this section are resolved.*
Includes: all Critical issues + High issues affecting more than one transcript.

### Critical
| # | Transcript | Quote | Current Tag | Issue | Suggested Action |

### High (multi-transcript)
| # | Transcripts | Quote | Current Tag | Issue | Suggested Action |

---

## Optional Refinements
*Addressable if time allows — skipping does not invalidate the analysis.*
Includes: single-instance High issues, all Moderate and Low issues.

### High (single transcript)
...

### Moderate
...

### Low
...

---

## Per-Code Summary
| Code | Frequency | Flags |

## Emergent Codes
| Code | # Quotes | Overlap with Existing | Recommendation |
```

---

## Post-Approval Phase

After the researcher has reviewed and approved changes from the review report:

1. For each original file in `outputs/analysis/`, apply only the approved changes
2. Save the modified files to `outputs/modified/` using the same filename (e.g. `transcript-N-tags.md`)
3. Do not alter any segment not covered by an approved change — copy everything else as-is

---

## Interactive Visualization

Follow `.claude/rules/visualization`.

---

## Apply Tag Edits Phase

Follow `.claude/rules/tag-edits`.

---

## Rules

- Never modify tags automatically — recommend only
- Every flag must include a human-readable explanation
- Present Critical and High issues to the researcher before tagging is considered complete
- Human decisions required for: emergent code approval, ambiguous quote adjudication, drift resolution, boundary disputes
- Never overwrite files in `outputs/analysis/` — modified versions go to `outputs/modified/` only
