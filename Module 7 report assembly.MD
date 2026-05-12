# Module 7 — Stage 5: Report Assembly

## Prerequisites

You must have read `module-1-foundation.md` and produced Stages 1, 2, 3, and 4.

This stage is the final assembly. It produces the consolidated report that gets distributed to stakeholders.

## Purpose

By Stage 5, all analytical work is complete. The work remaining is:

1. Write the Executive Summary — held until now so it can draw from every section.
2. Assemble all sections in the correct stakeholder-facing order.
3. Run a final consistency audit across sections.
4. Output a single consolidated document.

Do not introduce new findings at this stage. Do not re-analyse data. Do not summarise sections — reproduce them in full.

---

## Process

### Step 1 — Write the Executive Summary

Per foundation §9. Constraints:

1. Open with one line stating the structural problem the template has.
2. Name the **single most critical immediate fix** in a dedicated paragraph or callout — the one thing that must ship before anything else.
3. List the three highest-leverage changes that cover the majority of the measurable gap.
4. Cap at ~250 words. If you exceed, cut.

Forbidden patterns:
- Reframing language ("reposition the page as", "transform from X to Y", "build an authority hub")
- Aspirational vocabulary without a measurable target
- Strategy-deck phrasing
- Bullet lists where prose would carry the same content more decisively

Required patterns:
- Specific metrics from Section 1 (e.g. "61.5% of those return without acting")
- Specific structural calls from Sections 2, 3, and 4
- A named priority (the single immediate fix)

See foundation §10 for length and the example in Module 6's Reference Examples for the target prose pattern.

### Step 2 — Write the Title Block

Use this exact format:

```
# Artist Overview Page — UX Evaluation Report

**Template scope:** [Artist Page Template] | **Reference instance:** [Artist Name]
**Date:** [Today's date, format YYYY-MM-DD]
**Adobe Analytics period:** [start date – end date] (traffic volume, engagement benchmarks)
**Mouseflow journey period:** [start date – end date] (flow sequences, oscillation, drop-off)
**Mobile device tested:** [Device + viewport, e.g. iPhone 14 Pro Max, 430px width]
```

### Step 3 — Assemble Sections in Order

The final document has this exact structure:

1. **Title Block** (from Step 2)
2. **Executive Summary** (from Step 1)
3. **Section 1: Analytics Signals** (reproduce from Stage 1 output)
4. **Section 2: Friction Hypotheses** (reproduce from Stage 1 output)
5. **Section 3: Desktop Critique** (reproduce from Stage 2 output)
6. **Section 4: Mobile Critique** (reproduce from Stage 3 output)
7. **Section 5: Cross-Device Comparison** (reproduce from Stage 4 output)
8. **Section 6: SEO Context** (reproduce from Stage 4 output)
9. **Section 7: Roadmap** (reproduce from Stage 4 output)
10. **Section 8: Open Questions** (reproduce from Stage 4 output)

**Reproduce sections verbatim.** Do not summarise. Do not condense. Do not skip findings. Do not reorder rows within tables. The output of each prior stage is the canonical content for that section.

If a prior stage produced content that violates foundation rules (e.g. used a non-defined persona name, missed a Preserve entry), flag it in the consistency audit (Step 4) but do not silently rewrite. The audit produces a list of issues; the user decides whether to re-run a stage.

### Step 4 — Final Consistency Audit

Before outputting the final document, run these checks internally. Do not include the audit in the published report — it exists to catch cross-section drift.

| Check | What to verify |
|-------|----------------|
| Persona names | Same persona names used across all sections. No "Buyer" in one section and "Seeker" in another. |
| Severity flags | The same issue carries the same flag wherever it appears. The chat widget can't be 🟥 Critical in Section 4 and 🟧 Major in Section 5. |
| Filter ordering recommendation | The roadmap, Section 3 (desktop), and Section 4 (mobile) all agree on the filter order. Per foundation §2, the correct order is Category → Sale Type → Availability → Price. |
| Metric consistency | Numbers in the Executive Summary match numbers in Section 1 exactly. No rounding drift. |
| Cross-references | Any reference to "Section 7" or "the roadmap" or "Section 6" in the body of another section actually points to the right place after assembly. |
| Preserve entries | Sections 3 and 4 each have at least one ✓ Preserve entry per persona. If missing, flag for re-run. |
| Critical immediate fix | The fix named in the Executive Summary appears as 🟥 Immediate priority in the Section 7 Roadmap. |
| Hypothesis-to-recommendation chain | Every 🟥 Critical hypothesis in Section 2 has a corresponding row in Sections 3 or 4, and a corresponding line in Section 7 Roadmap. |

If any check fails, append a brief **Audit Findings** note at the end of the document (after Section 8) listing what failed. Example:

```
---

## Audit Findings (internal — remove before stakeholder distribution)

- Section 5 lists filter ordering as a Major flag; Section 3 lists it as Critical. Recommend aligning to Major.
- Section 2 H7 is marked CONFIRMED but underlying data point is not present in Section 1. Recommend re-running Stage 1 with the missing metric or downgrading H7 to INFERRED.
```

If all checks pass, omit the Audit Findings section entirely.

### Step 5 — Output the Final Document

Output the assembled report as a single markdown document. No preamble ("Here is the final report:"). No postamble ("Let me know if you'd like..."). Start with the title block, end with Section 8 (or Audit Findings if any).

---

## Output Format

The final document is markdown. Apply foundation §10 throughout — particularly the typography, prose density, and length conventions.

Per foundation §11, the section types are:

| Section | Type |
|---------|------|
| Executive Summary | Prose |
| Section 1 (Analytics) | Tables |
| Section 2 (Hypotheses) | Structured blocks |
| Section 3 (Desktop) | Prose + Table + Prose |
| Section 4 (Mobile) | Prose + (optional callout) + Table + Prose |
| Section 5 (Cross-Device) | Table |
| Section 6 (SEO) | Prose |
| Section 7 (Roadmap) | Table |
| Section 8 (Open Questions) | Structured blocks |

If any prior stage produced the wrong type (e.g. SEO as a table), the consistency audit flags it but the assembly preserves what was produced. Do not silently restructure.

---

## Quality Bar

The assembly **fails** if:

- The Executive Summary is written before sections are in view (i.e. produced in an earlier stage rather than this one).
- Sections are summarised rather than reproduced verbatim.
- Section order doesn't match the canonical structure (Title → Exec Summary → 1 → 2 → 3 → 4 → 5 → 6 → 7 → 8).
- The consistency audit is included in the published report when checks pass.
- The consistency audit is omitted when checks fail.
- The output includes preamble or postamble outside the report itself.
- The title block is missing the data periods or device tested.

## Common Failure Modes

- Treating assembly as a summarisation step. Sections are reproduced in full, not condensed.
- Writing a fresh Executive Summary that contradicts earlier-stage findings (e.g. summary calls out an issue that no hypothesis flagged).
- Skipping the consistency audit because "everything looks fine" — run all eight checks every time.
- Producing the title block without the data periods. Stakeholders need to know which data window the findings are anchored to.
- Inserting new analysis at assembly time. If something new emerges, it goes back to the relevant stage for re-run, not into the assembly output.
