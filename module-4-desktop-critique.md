# Module 4 — Stage 2: Desktop Critique

## Prerequisites

You must have read `module-1-foundation.md` and produced Stage 1 output (Sections 1 and 2). The hypotheses from Stage 1 inform but do not duplicate this section.

Relevant foundation rules:
- §4 (Persona Tagging) — applies to every row.
- §5 (Preserve Rule) — **mandatory**. Minimum 1 Preserve entry per persona.
- §6 (Specificity Rule) — applies to every recommendation.
- §7 (Severity Flag System) — applies to every row.

## Inputs

- Desktop screenshot(s) or live URL of the reference artist page
- Stage 1 output (Sections 1 and 2)

## Output

### Section 3: Desktop Critique

#### Template Design

Open with a short **Template Design** paragraph (4–6 sentences) describing the layout structurally:

- Column structure
- Persistent elements (sidebar, header)
- Default states (filters applied, grid contents)
- Hero composition
- Card anatomy (what each card shows, in what hierarchy)

**No evaluative language here** — just structure. The critique comes in the table.

#### Desktop Issues and Strengths

Produce one table with this exact column structure:

| Persona | Flag | Finding | Recommendation |
|---------|------|---------|----------------|

#### Table rules

1. **One row per finding.** Do not bundle multiple findings into one row.

2. **Include ✓ Preserve entries per foundation §5.** Minimum 1 per persona. The Flag column for Preserve entries is `✓` (not a severity flag). Preserve rows come first within each persona block.

3. **Findings must be specific to desktop.** Cross-device issues that are equally true on mobile go in the mobile section as well — do not treat as desktop-only.

4. **Recommendations must follow the specificity rule** (foundation §6). "Reorder sidebar: Category → Sale Type → Availability → Price" is acceptable; "Improve filter ordering" is not.

5. **Each finding must reference an underlying hypothesis or data point.** A finding that doesn't trace back to Stage 1 needs its own evidence inline.

#### Row ordering

Order rows by persona (Seeker → Regular Bidder → Casual Browser → Curious Owner), with Preserve entries first within each persona block, then issues by severity (Critical → Major → Moderate → Low).

#### Example rows (for format only, not content)

| Persona | Flag | Finding | Recommendation |
|---------|------|---------|----------------|
| Seeker | ✓ | Filter sidebar structurally correct — Category, Sale Type, and Availability exist and serve this persona when found. Two-column grid gives reasonable scanning density. | Preserve |
| Seeker | 🟥 | Artwork title subordinate on every card — "ARTIST NAME (DATES)" dominates the primary heading; work title appears below in smaller, lighter text. The only differentiating signal across 40+ cards is buried. Primary structural cause of the 61.5% oscillation rate. | Promote artwork title to primary heading; remove artist name from lot cards on artist-specific page instances |
| Seeker | 🟧 | Filter sidebar order inverted — Category (19,719 visits), Sale Type (9,296), Availability (8,811) each outrank Price (5,303), which sits at the top | Reorder sidebar: Category → Sale Type → Availability → Price |

#### Journey Data Implications

After the table, produce a short **Journey Data Implications** paragraph (3–5 sentences) that connects the desktop findings to the journey data — specifically:

- Which audiences the desktop template serves and which it fails
- What the journey data implies about the cost
- Any exit destinations that the desktop template could activate but doesn't (e.g. Calendar, Homepage)

Do not repeat hypothesis text. The point of this paragraph is to translate findings into journey-level consequence.

---

## Quality Bar

The section **fails** if:

- It contains no Preserve entries.
- It contains Preserve entries for some personas but not others.
- Findings repeat each other across personas without distinguishing what's persona-specific.
- Recommendations are vague (see specificity rule).
- The Template Design paragraph editorialises instead of describing.
- The Journey Data Implications paragraph repeats hypothesis text rather than connecting findings to journey data.
- A finding uses hedging language ("might", "could") on a CONFIRMED hypothesis.

## Common Failure Modes

These produced the weaker prior version. Each is forbidden:

- Producing all issues, no Preserve.
- Using long prose paragraphs in place of the table structure (Section 3 is a table, not an essay).
- Recommending the wrong filter ordering because Stage 1 conflated Events with Visits.
- Generic recommendations ("strengthen hierarchy", "promote price") that don't specify the change.
