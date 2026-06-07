# Tag Review Report

**Date:** 2026-03-28 | **Transcripts:** 2 (transcript-01-tags.md, transcript-02-tags.md) | **Coded segments:** 25 unique turns | **Total tag assignments:** 46

---

## Summary

| Severity | Count |
|----------|-------|
| Critical | 0 |
| High | 4 |
| Moderate | 3 |
| Low | 1 |

---

## High Issues

### H1 — Possible misfit: T-04 (P01) tagged Skepticism towards AI

| Field | Value |
|-------|-------|
| Transcript | transcript-01-tags.md |
| Turn | T-04 |
| Participant | P01 (Julia) |
| Quote | "I mean, I trust my opinions, but I don't know if like I would really like... it's hard to know if I'm always like doing the right thing with it." |
| Current tag | Skepticism towards AI |
| Issue | **Definition mismatch.** Skepticism towards AI is defined as "doubt about AI accuracy." This quote expresses uncertainty about the reliability of Julia's *own* manual validation process — not about AI. The rationale itself acknowledges this: "uncertainty is not just about AI but about whether human checks are sufficient." The concern is about solo review methodology, not the AI system. |
| Suggested action | **Remove Skepticism towards AI; retain Validation.** If researcher wants to preserve this signal, consider a new code ("Validation Uncertainty" or similar) — but a single quote does not yet meet the quality bar. Tier 2 — requires adjudication. |

---

### H2 — Codebook overlap: Hypothesis Confirmation 100% co-occurrence with Survey Goals

| Field | Value |
|-------|-------|
| Transcripts | transcript-01-tags.md, transcript-02-tags.md |
| Turns | T-10, T-14, T-15 (P01); T-J08 (P02) |
| Issue | **All 4 Hypothesis Confirmation quotes are also tagged Survey Goals (100% overlap).** The codebook rule flags emergent codes with >60% quote overlap with a predefined code for merger review. The codes are conceptually distinguishable — Survey Goals captures objective alignment in general; Hypothesis Confirmation captures the specific value of AI converting pre-existing team beliefs into data-backed advocacy material. But in practice every Hypothesis Confirmation quote is doing Survey Goals work simultaneously. |
| Suggested action | **Researcher decision required:** (A) Retain Hypothesis Confirmation as a standalone emergent code with a sharper definition that excludes generic objective alignment, or (B) absorb it as a sub-theme of Survey Goals (e.g., "Survey Goals — advocacy sub-type"). If retaining, tighten the definition: Hypothesis Confirmation should require explicit mention of internal advocacy, leadership communication, or pre-existing belief. |

---

### H3 — Codebook overlap: Report Context Gap 62.5% co-occurrence with Validation

| Field | Value |
|-------|-------|
| Transcripts | transcript-01-tags.md, transcript-02-tags.md |
| Turns | T-16 (P01); T-J09, T-J10, T-J11, T-J16 (P02) — all also tagged Validation |
| Issue | **5 of 8 Report Context Gap quotes (62.5%) are also tagged Validation**, just above the 60% merger flag threshold. The codes are mechanistically distinct — Validation describes the *behavior* of verifying AI outputs; Report Context Gap describes *why* that verification is needed (AI's blindness to survey design). This is a cause-vs.-effect relationship, not true conceptual overlap. However, the boundary is difficult to maintain for future coders without explicit guidance. |
| Suggested action | **Clarify, not merge.** Add a decision rule to the Report Context Gap definition: "Apply when the quote identifies a *specific* gap in AI's survey design knowledge (routing logic, question framing, sample composition, researcher methodology standards). Do not apply when the verification behavior is the salient theme with no explicit survey-design failure named." The codes can co-occur but each requires its own warrant. |

---

### H4 — Stale source note in transcript-01 memo

| Field | Value |
|-------|-------|
| Transcript | transcript-01-tags.md |
| Location | Transcript Memo, final paragraph (⚠ Note on source files) |
| Issue | The memo states: *"Both interview-01.vtt and interview-02.vtt appear to be recordings of the same interview session with the same participant (Julia)."* This is incorrect. Interview-02.vtt contains a Julia overlap segment (lines 1–~139, already coded in transcript-01) followed by a fully distinct interview with a second participant, Jacklyn (P02, lines ~140–end). Transcript-02 was coded separately and is reflected in transcript-02-tags.md. |
| Suggested action | **Update the memo note.** Replace with: *"Interview-02.vtt contains a Julia overlap segment (lines 1–~139, coded here) and a separate interview with P02 (Jacklyn, coded in transcript-02-tags.md). The overlap runs ~01:15–08:54; Jacklyn's interview begins at ~09:00."* |

---

## Moderate Issues

### M1 — Interactive Analytics: single-interviewee threshold not met

| Field | Value |
|-------|-------|
| Transcript | transcript-02-tags.md |
| Turns | T-J14, T-J15 (P02 only) |
| Issue | The predefined code quality bar requires ≥2 unique interviewees unless the code is "highly distinctive." Interactive Analytics currently has 2 quotes from 1 interviewee (P02). The code was already flagged for researcher approval in transcript-02-tags.md. |
| Suggested action | **Researcher decision required.** Does the specificity and distinctiveness of the interactive querying paradigm (wanting conversational AI vs. static report) meet the "highly distinctive" exception? If yes, confirm. If no, hold as provisional until a second interviewee corroborates. The signal is strong within P02 — both quotes are strong-confidence and describe a specific unmet interaction model — but the quality bar requires human judgment here. |

---

### M2 — T-J16 (P02) Report Context Gap fit is a stretch

| Field | Value |
|-------|-------|
| Transcript | transcript-02-tags.md |
| Turn | T-J16 |
| Quote | "I like to have a sample size of at least 50. Otherwise it's just directional feedback... 80% of those 24 people means nothing to me from a data standpoint." |
| Issue | Report Context Gap is defined around *survey design* awareness — routing logic and question framing. This quote is about Jacklyn's professional statistical threshold (n≥50 for actionable findings). That is a *researcher methodology* standard, not a survey design feature. Applying Report Context Gap here subtly broadens the code's scope from "AI doesn't know the survey's structure" to "AI doesn't know the researcher's analytical standards." These are related but distinct. |
| Suggested action | **Tier 3 — stylistic.** If the researcher wants to expand Report Context Gap to include researcher methodology standards (e.g., sample size thresholds, weighting conventions), update the definition explicitly. Otherwise, consider coding T-J16 as Validation only, and note the analytical standards theme as a potential future emergent code if it recurs. |

---

### M3 — T-J08 (P02): unexpected discovery signal within Hypothesis Confirmation

| Field | Value |
|-------|-------|
| Transcript | transcript-02-tags.md |
| Turn | T-J08 |
| Quote | "...the things that pop the most as we kind of expected as we heard from the client, were reducing fine lines and wrinkles, improving skin elasticity and also reducing stress and anxiety. **In that one was exciting.**" |
| Issue | The quote contains two signals: (1) AI confirmed expected findings → Hypothesis Confirmation, and (2) AI surfaced a genuinely unexpected finding (stress/anxiety benefit) that added value beyond what the team hypothesized. The transcript memo already flags this as a potential counter-pattern. The Hypothesis Confirmation code does not capture the discovery dimension, and current tagging obscures it. |
| Suggested action | **Note for researcher; no action required now.** Single data point — insufficient to generate a new code. Flag for monitoring in subsequent transcripts. If an "Unexpected Discovery" or "Beyond Confirmation" pattern recurs, it would meet the quality bar and warrant a new code. |

---

## Low Issues

### L1 — T-13 (P01) Validation tag — weak fit

| Field | Value |
|-------|-------|
| Transcript | transcript-01-tags.md |
| Turn | T-13 |
| Quote | "I like to see these tables especially like that you have the sample size there. So we can see. Like, this isn't just based on a few responses." |
| Issue | The Validation tag is applied because "sample size visibility helps confirm findings are representative." However, the participant is expressing appreciation for a display feature — she is not describing an active verification behavior. The stronger read is Survey Goals: she values a report format that communicates credibility to the stakeholders she shares it with. Validation is plausible but downstream from the quote's primary signal. |
| Suggested action | **Tier 3 — stylistic.** Acceptable to retain as a weak Validation instance (passive verification-enabling feature). Alternatively, drop Validation and keep Survey Goals only. Either is defensible; researcher preference. |

---

## Per-Code Summary

| Code | Type | Frequency (total tags) | % of All Tags | Flags |
|------|------|------------------------|---------------|-------|
| Survey Goals | Predefined | 16 | 34.8% | None |
| Validation | Predefined | 11 | 23.9% | None |
| Report Context Gap | Emergent | 8 | 17.4% | H3 (overlap with Validation); M2 (scope creep at T-J16) |
| Skepticism towards AI | Emergent | 5 | 10.9% | H1 (possible misfit at T-04) |
| Hypothesis Confirmation | Emergent | 4 | 8.7% | H2 (100% overlap with Survey Goals) |
| Interactive Analytics | Emergent | 2 | 4.3% | M1 (single interviewee) |

---

## Emergent Codes Assessment

| Code | # Quotes | # Unique Interviewees | % Overlap with Predefined | Recommendation |
|------|----------|-----------------------|---------------------------|----------------|
| Report Context Gap | 8 | 2 (P01, P02) | 62.5% with Validation | **Promote to confirmed** — strong signal across both participants; clarify boundary with Validation (see H3) |
| Skepticism towards AI | 5 | 2 (P01, P02) | 0% direct overlap | **Promote to confirmed** — after adjudicating T-04 misfit (see H1); if T-04 removed, count drops to 4 quotes / 2 interviewees — still qualifies |
| Hypothesis Confirmation | 4 | 2 (P01, P02) | 100% with Survey Goals | **Hold pending H2 adjudication** — resolve merger question before confirming |
| Interactive Analytics | 2 | 1 (P02 only) | 0% direct overlap | **Hold pending M1 adjudication** — confirm or keep provisional based on researcher's quality bar exception ruling |

---

## Predefined Codes Not Applied

Both **Survey Goals** and **Validation** are applied across both transcripts. No predefined codes missing.

---

## Reviewer Memo

The coding is methodologically sound across both transcripts — no critical misfits, consistent rationale depth, and appropriate multi-coding of genuine co-occurrences. The dominant finding from this review is a codebook management question rather than a tagging error: **Hypothesis Confirmation** is at 100% overlap with Survey Goals and needs a sharper boundary or a merger decision. The **Report Context Gap / Validation** boundary is also worth codifying before the next transcript, since the cause-effect relationship between the two codes makes it predictable that they will continue to co-occur.

The most analytically significant open question is **Interactive Analytics** — the weakest code by coverage (1 interviewee) but potentially the most distinctive new signal in the dataset. Jacklyn's description of wanting to query the AI conversationally is a specific, coherent mental model that doesn't appear anywhere in P01's data. A third interviewee mentioning any form of interactive or queryable AI behavior would confirm it.

Two housekeeping items: (1) The stale source note in transcript-01's memo should be corrected (H4). (2) Interview-02.vtt is truncated at 30:33 mid-sentence — researcher should verify whether more content from Jacklyn's interview exists.

**Priority actions for researcher:**
1. Adjudicate H1 (T-04 Skepticism misfit)
2. Adjudicate H2 (Hypothesis Confirmation merger vs. retain)
3. Adjudicate M1 (Interactive Analytics — confirm or hold)
4. Confirm H3 boundary clarification language for Report Context Gap
5. Correct transcript-01 memo source note (H4)
