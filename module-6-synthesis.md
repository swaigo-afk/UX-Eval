# Module 6 — Stage 4: Synthesis

## Prerequisites

You must have read `module-1-foundation.md` and produced Stages 1, 2, and 3.

Relevant foundation rules:
- §6 (Specificity Rule) — applies to every roadmap row.
- §7 (Severity Flag System) — applies to cross-device and roadmap tables.
- §8 (Output Discipline) — particularly: no reframing language, no aspirational vocabulary.

## Output

Four sections, in order: Section 5 (Cross-Device Comparison), Section 6 (SEO Context), Section 7 (Roadmap), Section 8 (Open Questions).

**Note: The Executive Summary is NOT produced at this stage.** It is held until Stage 5 (Module 7 — Report Assembly), where it is written with all sections in view. This avoids the failure mode of writing an executive summary before the synthesis is complete.

---

### Section 5: Cross-Device Comparison

Produce one table:

| Issue | Desktop | Mobile | Flag | Priority |
|-------|---------|--------|------|----------|

#### Rules

- One row per issue.
- **Desktop** and **Mobile** columns: state severity on each device, or "Not present" if applicable.
- **Flag** column: use the foundation §7 severity system. This is the cross-device severity, not device-specific.
- **Priority** column: one of `Immediate` / `A/B Test` / `Medium-term` / `Long-term`.
- Order rows by Priority (Immediate first), then by Flag severity (Critical first within each priority).

Do not add prose around the table beyond a single sentence introducing it.

---

### Section 6: SEO Context

**3–4 short paragraphs, ~300 words maximum.** No table required. No subsection headers within the section.

This is one of the shortest sections in the report. Its purpose is to establish that the existing UX recommendations already cover the SEO risk — not to produce a separate SEO workstream. Resist the model's default verbosity on SEO topics.

#### Required content

- The relationship between organic dependency and engagement quality across high-traffic artist pages — frame as a **pattern across the catalogue, not a single-instance problem**.
- Specific Google quality signals at risk (dwell time, return-to-search) and why the data points to risk at template scale.
- A single statement that UX fixes and SEO fixes are not separable in this case — the existing roadmap addresses both.

#### Forbidden

- Producing SEO recommendations separate from the UX roadmap.
- Generic SEO advice ("add schema", "improve internal links", "add structured data") without tying it to the template-level problem and the existing roadmap.
- Subsections like "6.1 Current SEO Strengths", "6.2 SEO Weaknesses", "6.3 SEO Opportunity Areas". This is a 3–4 paragraph section, not a chapter.
- Bullet-listing SEO opportunities. The point is to fold SEO into the existing UX roadmap, not to enumerate a parallel one.

#### Length check

If your draft exceeds ~300 words, cut. If your draft has subsections, restructure as flowing paragraphs. If you find yourself producing an "SEO opportunity table", stop — that belongs in Section 7 if anywhere, and most SEO opportunities are already absorbed there.

---

### Section 7: Roadmap

One table:

| Feature | Priority | Description | Effort |
|---------|----------|-------------|--------|

#### Priority categories

| Priority | When to use |
|----------|-------------|
| 🟥 **Immediate** | Ship as part of Phase 1 migration. No A/B test required because the change is data-confirmed or visual-evidence-confirmed. |
| 🟨 **A/B Test** | Directionally supported but needs validation. Description column must include the test design summary. |
| **Medium-term** | Phase 2 redesign scope. |
| 🟩 **Long-term** | Multi-quarter, requires personalisation or data infrastructure. |

#### Description column requirements

- State the change specifically (per foundation §6).
- For **A/B Test** items: include the hypothesis ("If... then...") and the primary metric to be measured. Where useful, also include the guardrail metric and decision rule.
- For **Medium-term** and **Long-term** items: name the structural dependency (e.g. "requires live sales data feed by artist", "requires editorial template and content model changes", "requires personalisation infrastructure").

#### Effort column

One of: `Low` / `Low–Medium` / `Medium` / `High`. Include a one-clause justification where the effort is Medium or High (e.g. "Medium — requires mobile filter component redesign").

#### Row ordering

Order by Priority (Immediate first), then within each priority by Flag severity.

---

### Section 8: Open Questions

Numbered list, **4–8 questions**.

Each question must be **decision-forcing**, not reflective.

#### Required format

> **N. [Question]** — [If X, then implication A. If Y, then implication B.] [What data or test would resolve it.]

#### Bad vs Good

| Bad (reflective) | Good (decision-forcing) |
|------------------|-------------------------|
| "How do users feel about the new filters?" | "**Device split of the oscillation loop** — If the 61.5% oscillation is predominantly mobile, the fix is filter UX and above-fold hierarchy. If predominantly desktop, it is card design and information architecture. These need different solutions at different costs. Device-segmented journey data should be obtained before locking the roadmap sequence." |
| "Should we add more content?" | "**Editorial drop-off root cause** — 53.2% Stories drop-off — is it content quality, the absent return path, or both? A short editorial funnel audit would sequence the investment correctly before any content budget is committed." |

The point of an open question in this report is to flag where the **next decision depends on data we don't have**. Reflective questions go elsewhere.

---

## Reference Examples

### Example — Complete SEO Context section (~210 words, 3 paragraphs)

```
High organic search dependency and weak engagement metrics co-occur across every high-traffic artist page — this is a template pattern, not an isolated instance problem. Across the top 25 artist pages, organic search accounts for 92.7% of traffic on average. Pages with the highest organic dependency consistently show above-average bounce rates and below-average dwell time relative to the template mean (37.6% bounce, 210.9s dwell time).

The more SEO-dependent a page, the weaker its engagement. Google uses dwell time and return-to-search behaviour as quality signals. Sustained above-average bounce and below-average dwell time across 591,093 annual unique visitors creates a real, slow-building SEO risk at template scale.

The UX fixes already identified in Section 7 address both problems simultaneously — no separate SEO workstream needed.
```

3 paragraphs. ~210 words. No table. No subsection headers (6.1, 6.2, 6.3). No bullet list of SEO opportunities. The point is to fold SEO into the existing UX roadmap, not to enumerate a parallel one.

### Example — Complete Open Question (decision-forcing format)

```
**1. Device split of the oscillation loop** — If the 61.5% oscillation is predominantly mobile, the fix is filter UX and above-fold hierarchy. If predominantly desktop, it is card design and information architecture. These need different solutions at different costs. Device-segmented journey data should be obtained before locking the roadmap sequence.

**2. Scroll depth at drop-off** — Does the 61.1% drop-off happen before the lot grid (above-fold failure) or after reaching it (card or filter failure)? Scroll depth data from Mouseflow would tell us which persona is primarily driving the primary metric and where to focus first.

**3. Editorial drop-off root cause** — 53.2% Stories drop-off — is it content quality, the absent return path, or both? A short editorial funnel audit would sequence the investment correctly before any content budget is committed.

**4. Mobile rendering bug on lot card titles** — Date range appears duplicated on several mobile cards. This needs to be confirmed as a bug and resolved before any A/B test on card title format — testing a broken component produces unreliable results.
```

Each question: bold label + decision fork (If X / If Y) + implication for each branch + what resolves it.

### Example — Complete A/B Test roadmap row (Description includes test design)

| Feature | Priority | Description | Effort |
|---------|----------|-------------|--------|
| Default to upcoming/active lots | 🟨 A/B Test | Default grid shows active and upcoming lots only; add "Show all including sold" toggle. **Hypothesis:** If active-intent visitors see only upcoming lots by default, click-through to lots will rise above the 23% baseline toward the 30% target. **Primary metric:** click-through to lots. **Guardrail:** filter use rate (should fall, indicating less compensatory filtering). **Decision rule:** ship if click-through ≥ 28% with no bounce rate increase. | Low–Medium |

The Description column carries the test design inline — hypothesis, primary metric, guardrail metric, decision rule.

### Failure examples — what NOT to produce

**Bad SEO section (collapsed to table):**
```
| Signal | Impact | Action |
|--------|--------|--------|
| Strong organic entry | Positive | Preserve |
| Long dwell time | Neutral (scanning) | Improve resolution |
| High exits | Risk | Address structurally |
| Category-scoped pages | Positive | Scale intentionally |
```

Why this fails:
- SEO section is prose (foundation §11), not a table
- "Improve resolution" / "Address structurally" are not specific
- No mention of the template-level pattern across the catalogue
- No mention that UX fixes and SEO fixes are the same work

**Bad open questions (reflective, one-liners):**
```
1. Do we formally classify artists by commercial profile?
2. Is "What can I buy now?" the primary buyer question?
3. Should Artist + Category pages become first-class products?
4. Are we willing to make biography visually secondary for buyers?
```

Why this fails:
- All are reflective, not decision-forcing
- No "If X then Y" forks
- No data point that would resolve the question
- No implication of cost or roadmap consequence
- These belong in a strategy workshop, not an evaluation report's open questions

---

## Quality Bar

The synthesis **fails** if:

- The cross-device comparison is prose rather than a table.
- The roadmap separates SEO from UX recommendations.
- Open questions are reflective rather than decision-forcing.
- The roadmap omits effort estimates or omits A/B test design details for A/B items.
- An Executive Summary is produced at this stage (the Exec Summary is held until Stage 5 — Module 7).

## Common Failure Modes

These produced the weaker prior version. Each is forbidden:

- Cross-device comparison given as prose rather than a flag/priority table.
- SEO recommendations given as a separate roadmap workstream rather than absorbed into the UX recommendations.
- Roadmap items with vague descriptions like "promote price filter" or "add available now module" without specifying the implementation.
- Open questions phrased as research curiosity rather than decision forks.
- Long sprint summary tables duplicating the roadmap with different labels.
- Writing an Executive Summary at this stage rather than holding it for Stage 5 assembly.
