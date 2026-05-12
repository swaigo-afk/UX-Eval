# Module 5 — Stage 3: Mobile Critique

## Prerequisites

You must have read `module-1-foundation.md` and produced Stages 1 and 2. The desktop critique informs but does not duplicate this section.

Relevant foundation rules:
- §4 (Persona Tagging) — applies to every row.
- §5 (Preserve Rule) — **mandatory**. Minimum 1 Preserve entry per persona.
- §6 (Specificity Rule) — applies to every recommendation.
- §7 (Severity Flag System) — calibration note: anything blocking imagery on mobile is **Critical**, not Major.

## Inputs

- Mobile screenshot(s) of the reference artist page (specify device and viewport)
- Stage 1 and Stage 2 output

## Output

### Section 4: Mobile Critique

#### Template Design — Mobile

Open with a short paragraph describing the mobile layout structurally, including:

- Single-column or other layout structure
- Above-fold composition (what's visible without scrolling)
- What is visible vs hidden by default (filters, controls, secondary navigation)
- Any persistent overlays (chat widgets, sticky elements)
- Card anatomy on mobile and any differences from desktop

**State the device and viewport tested** (e.g. "iPhone 14 Pro Max, 430px width").

#### Critical Immediate Fix (conditional)

If there is a **single critical immediate fix** that must ship before anything else on mobile — typically an element physically blocking core content — name it in a call-out block **before the table**:

> **Critical immediate fix:** [Specific statement of what must be moved/changed and where]

This is the Lane 2 move — explicit prioritisation. Do not bury this in a table row.

If no such single fix exists, skip the call-out. Do not invent one to fill the slot.

#### Mobile Issues and Strengths

Produce one table with this exact column structure:

| Persona | Flag | Finding | Recommendation |
|---------|------|---------|----------------|

#### Table rules

All rules from Stage 2 apply. In addition:

1. **Where a desktop issue becomes more severe on mobile, name the escalation explicitly.** Example:
   > "Desktop problem becomes mobile crisis — hidden filters require finding and opening a drawer; on desktop they are at least visible, if misordered."

2. **Flag any element that competes with or blocks lot imagery as Critical, not Major.** Mobile imagery is the strongest engagement hook the template has — anything obstructing it is a primary metric driver.

3. **Where mobile has no surface at all for a function that exists on desktop** (e.g. Calendar exit, secondary navigation), name it as a structural gap, not a minor finding.

4. **Recommendations must specify the mobile-specific implementation.** "Full-width CTA in the hero" is acceptable; "CTA in the hero" is not — mobile-specific dimensions and placement matter.

#### Row ordering

Same as Stage 2: by persona, Preserve entries first within each persona block, then issues by severity.

#### Journey Data Implications

After the table, produce a short paragraph specific to mobile — particularly about how high-organic, new-visitor, mobile traffic interacts with the template's defaults. Cover:

- Whether mobile is likely amplifying the primary metric problems
- Which best-retention exits (Calendar, Homepage) have no mobile surface
- Any mobile-specific journey signal worth flagging

---

## Quality Bar

The section **fails** if:

- The Critical immediate fix is buried in a table row rather than called out (assuming one exists).
- Mobile findings duplicate desktop findings without naming the mobile-specific escalation.
- The Preserve rule isn't satisfied per persona.
- Recommendations don't specify the mobile-specific implementation (e.g. "full-width CTA" vs just "CTA").
- An imagery-blocking element is flagged Major instead of Critical.

## Common Failure Modes

These produced the weaker prior version. Each is forbidden:

- Treating the chat widget as a stylistic issue rather than a Critical immediate fix when it physically blocks the first lot image.
- Producing long prose paragraphs about mobile experience instead of a structured table.
- Recommending "context-aware chat" or other conditional behaviour when the simple fix is "move to bottom-right".
- Failing to escalate desktop findings to higher severity on mobile where the desktop problem becomes a mobile crisis (e.g. filter access).
