---
name: data-tagging
description: Applies predefined codes and generates emergent codes. Run when asked to tag interview transcripts.
---

## Constraints

- Save all outputs to `outputs/` as `transcript-N-tags.md`
- Exclude transcript segments that are intro/closing small talk or off-topic


## Workflow Phases

### Phase 0: Clarify Before Starting

Before loading any files, check for `outputs/progress.json`:

**If `outputs/progress.json` exists:**
- Load it and display the resume state to the researcher:
  - Completed transcripts
  - In-progress transcript and last coded turn
  - Emergent codes accumulated so far
- Ask only: "Ready to resume, or do you want to start over?"
- Do not ask questions 1–3 below — skip directly to Phase 1.

**If `outputs/progress.json` does not exist:**
Ask the researcher:
1. Which transcript(s) to analyze? ("all" is a valid answer — the skill will sequence through remaining transcripts automatically.)
2. Are there emergent codes from prior transcripts to carry forward? *(Skip if `memory/emergent_codes.md` already contains carry-forward codes — load those automatically.)*
3. Any specific research questions or themes to prioritize?

**Do not proceed to Phase 1 until the researcher has responded.**

---

### Phase 1: Setup and Data Loading

**Fresh start (no `progress.json`):**
1. Read `.claude/rules/predefined-codes` — the codebook
2. Read `context/interview-guide.txt`
3. Read `.claude/rules/outputs` — output formatting conventions
4. Load emergent codes for coding — **labels and definitions only; do not load anchor examples, quote counts, or participant references** — these are not needed during coding and will be loaded in full only at Phase 2.5

**Resuming (`progress.json` exists):**
1. Read `.claude/rules/predefined-codes` — reload in case codebook was updated between sessions
2. Load emergent codes for coding — **labels and definitions only** (same constraint as above)
3. Skip `context/interview-guide.txt` and `.claude/rules/outputs` — these are static and do not change between sessions

**Both paths:**
5. For each transcript, check its line count first, then select chunk size:

   | File length | Chunk size | ~Interview time per chunk |
   |---|---|---|
   | Under 400 lines | Load in full | — |
   | 400–1,500 lines | 300 lines | ~15–20 min |
   | 1,500–4,000 lines | 600 lines | ~30–40 min |
   | 4,000+ lines | 1,000 lines | ~45–60 min |

   **Read and code one chunk at a time — do not load the full transcript before starting to code.**

   Seek to `in_progress.last_coded_turn` if resuming mid-transcript. Do not re-code already completed turns.

---

### Phase 2: Coding

**Segmentation:** Use speaker turns as the primary unit. Code participant turns only; skip interviewer speech. For turns covering multiple themes, mark sub-spans and assign different codes to each.

#### First Deductive Pass
1. For each participant turn, check against predefined codes
2. Assign the code + 1-2 sentence rationale if it fits
3. Mark unmatched turns — do NOT force a fit

Apply conservatively: a quote must clearly exemplify the code's definition. When in doubt, leave it unmatched.

#### Second Deductive Pass
1. Review all unmatched units
2. Generate a provisional code for each; prefer in-vivo language
3. Consolidate near-duplicates under one label
4. Each emergent code needs: short label (2-5 words), definition (1-2 sentences), anchor example

Emergent codes are provisional — flag them for researcher approval. Once approved, record in `memory/emergent_codes.md` using this format:

```
### [Code Label]
- **Status:** Provisional — awaiting approval
- **Created:** [transcript filename] | [date]
- **Definition:** [1-2 sentences]
- **Anchor example:** "[exact quote]" ([participant ID], [turn timestamp])
- **Quotes:** [N] | **Unique interviewees:** [N]
```

The `Created` field and anchor example are fixed at approval — never update them even if the code accumulates more quotes later. They are the permanent baseline for drift detection.

#### Multi-Tag Rules
- Assign multiple tags only for genuine co-occurrence or hierarchical overlap
- When uncertain between two codes, pick the best fit and note ambiguity — don't assign both
- Normal range: 1-3 tags per unit; flag 4+ for review (unit likely needs splitting)
- Each tag requires a confidence indicator: **strong**, **moderate**, or **tentative**
- Multi-tagged units must appear under each assigned code in the output

#### Progress tracking (after every chunk)
After coding each chunk, update `outputs/progress.json`:

```json
{
  "completed": ["transcript-01.vtt"],
  "in_progress": {
    "file": "transcript-03.vtt",
    "last_coded_turn": "00:47:22"
  },
  "emergent_codes": ["Workaround Behavior", "Trust Calibration"],
  "pending_registry_review": {
    "near_duplicate_candidates": [["Code A", "Code B"]],
    "retirement_candidates": ["Interactive Analytics"]
  }
}
```

When a transcript is fully coded, move it from `in_progress` to `completed` and clear `in_progress`.

**Accumulating registry candidates (do not interrupt — just log):**
- If a new emergent code's definition or anchor example overlaps substantially with an existing one, add the pair to `pending_registry_review.near_duplicate_candidates`
- After each completed transcript, check if any emergent code has appeared in only one transcript and not recurred — add its label to `pending_registry_review.retirement_candidates`
- Do not surface these to the researcher mid-session. Log only.

---

### Phase 2.5: Emergent Code Registry Review

**Trigger:** Run this phase once at end of session — either when all transcripts are complete, or when the researcher signals they are stopping. Do not run after every transcript.

Load `pending_registry_review` from `outputs/progress.json` and check for two conditions:

#### 1. Near-duplicates
Identify any two emergent codes whose definitions or anchor examples overlap substantially. Present each pair to the researcher:

```
These two emergent codes may overlap:
- [Code A]: [definition]
- [Code B]: [definition]

Options:
  1. Merge into [Code A] — retire [Code B], re-tag its quotes under [Code A]
  2. Merge into [Code B] — retire [Code A], re-tag its quotes under [Code B]
  3. Keep both separate
  4. Rename one — provide new label
```

Do not merge or rename anything until the researcher responds. Apply only the approved action.

#### 2. Retirement candidates
Flag any emergent code that meets both conditions:
- Appeared in only one transcript
- Has not recurred in any transcript coded since

Present each candidate to the researcher:

```
Retirement candidate: [Code Label]
Appeared in: transcript-N only
Quote count: N
Has not recurred across [N] subsequent transcripts.

Approve removal? (yes / no — if no, it remains active in the registry)
```

Do not remove any code until the researcher approves. If approved, remove the code from `memory/emergent_codes.md` and note its removal in `outputs/handoff.md`.

#### Registry rules
- Never promote an emergent code to predefined — keep all emergent labels as-is regardless of frequency
- Never auto-merge, auto-rename, or auto-retire — researcher decision required for every change
- After applying any approved changes, update `memory/emergent_codes.md`
- After Phase 2.5 completes, clear `pending_registry_review` from `outputs/progress.json`

---

### Phase 3: Save Output

Write the full output directly to `outputs/analysis/transcript-N-tags.md` — do not print it to the conversation. Once saved, display only a brief completion summary:

```
Saved outputs/analysis/transcript-N-tags.md
[N] quotes coded | [N] emergent codes flagged | [N] unassigned turns
```

**File structure:**

---

```
## Code Table

| Code | Definition | # of quotes |
---

[One <details> block per code with all quotes, confidence, and rationale]

---

## Unassigned Turns

Participant turns that were reviewed but not assigned any code (neither predefined nor emergent). Excluded segments (small talk, rapport building, interviewer turns) are NOT listed here — only turns that were substantively considered and left untagged.

| Timestamp | Text | Reason not coded |
|------|-------------|-----------|

```

After saving the output file, write `outputs/handoff.md`:

```
## Handoff — [date]
Completed: [list of transcript filenames]
In progress: [filename], stopped at [timestamp] — or "none" if all done
Emergent codes: [list of active emergent code labels]
Next: [resume instruction or "corpus complete"]
```

Overwrite `outputs/handoff.md` on every save — it always reflects current state.

**Session break suggestion:** After every 5 transcripts completed within a single session, before loading the next transcript, display:

```
[N] transcripts completed this session.
This is a good stopping point — progress.json is current and resuming
in a fresh session ensures full context fidelity for the remaining transcripts.

Continue to [next transcript], or stop here?
```

Wait for the researcher to respond before proceeding. Either answer is valid — this is an informed choice, not a required stop.

---

## Rules

- Never modify the raw transcript
- Flag predefined codes that were never applied
- Every quote must include: confidence, rationale
- Emergent codes must include a definition and anchor example
- Always include the Unassigned Turns table even if empty (write "None" as a single row)
