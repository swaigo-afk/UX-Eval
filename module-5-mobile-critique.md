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

## Reference Examples

### Example — Template Design — Mobile paragraph (prose, descriptive)

```
Single-column layout on iPhone 14 Pro Max (visual review via screenshot). Above fold: nav bar, breadcrumb, artist name, truncated biography with "See more", a horizontal scrollable related artists strip, results count. A fixed chat button overlays the upper-right viewport, physically blocking the first lot card image. Below fold: full-width lot card images, artist name + dates as primary heading (date range duplicated on several cards — likely a rendering bug), artwork title in smaller text, price data, FOLLOW button. No filter controls visible anywhere without a deliberate tap to open a hidden drawer.
```

Note: descriptive prose only. Device and viewport stated. No evaluation here — the critique comes in the table.

### Example — Critical Immediate Fix callout

```
> **Critical immediate fix:** Move the floating chat widget off the first artwork image — fixed in upper-right viewport, physically overlapping the first lot card's image. Move to bottom-right corner. No design cost.
```

This is one sentence (plus a fragment). Bolded label. Action-oriented. Specific. Above the table.

### Example — Full mobile table rows with escalation language

| Persona | Flag | Finding | Recommendation |
|---------|------|---------|----------------|
| Seeker | ✓ | Full-width artwork images at single-column width make individual works identifiable | Preserve |
| Seeker | 🟥 | Filters hidden entirely — on desktop filters are always visible (if mis-ordered); on mobile there are no visible filter controls; Sale Type and Availability require finding and opening a hidden drawer. The desktop problem becomes a mobile crisis. | Persistent filter chip bar: Sale Type and Availability as always-visible tappable chips above the lot grid; secondary filters in a "More" drawer |
| Seeker | 🟥 | Chat widget blocks the first artwork image — fixed in upper-right viewport, physically overlapping the first lot card's image; visually confirmed in the screenshot | Move to bottom-right corner |
| Seeker | 🟥 | Card title more damaging at mobile width — "ARTIST NAME (DATES)", potentially duplicated, occupies the first 2–3 lines of a 430px viewport; artwork title requires active effort to find | Promote artwork title to primary heading; investigate date duplication as a rendering bug before A/B testing |
| Regular Bidder | ✓ | Breadcrumb navigation gives fast orientation | Preserve |
| Regular Bidder | 🟧 | No artist-level follow in the hero — higher impact on mobile than desktop; this persona's mobile use is monitoring-oriented; an artist-level alert is exactly what they would set during a check-in session | Full-width "Follow this artist" CTA in the hero area |
| Casual Browser | ✓ | Related artists horizontal strip — serves the 6.5% lateral exit pattern (29,874 annual exits); concept is right | Preserve and invest in |
| Casual Browser | 🟥 | Chat widget blocks the first artwork image — the primary engagement hook for this persona; blocking it at first impression is the most damaging single issue for the Casual Browser on mobile | Move to bottom-right immediately — no design cost |
| Curious Owner | 🟩 | No selling entry point on mobile — same gap as desktop | Contextual selling link — same as desktop |

Notes:
- "The desktop problem becomes a mobile crisis" — explicit escalation language per the mobile-specific framing requirement
- Chat widget appears twice with different persona framing — same fix, different persona impact, both Critical
- All Critical flags justified by primary-metric driver, imagery blocking, or core flow obstruction

### Example — Journey Data Implications — Mobile (prose)

```
The drop-off rate and oscillation loop are disproportionately likely to be mobile-driven given the high organic search and new visitor share. A Seeker arriving on mobile from a lot page faces hidden filters, a blocked first image, and harder card scanning. The template provides no mobile-specific mechanism to compensate. Calendar and Homepage — the two best-retention exits — are unreachable from mobile without deliberate off-page navigation. Neither has a surface in the mobile template.
```

5 sentences, flowing prose. Names the persona pattern, the structural gaps, the exit-surface gap. Connects mobile findings to journey data.

### Failure example — what NOT to produce

```
4.1 Above-the-Fold (Mobile)
| Element | Impact | Persona | Severity |
| Bio compression | Inventory fully below fold | Buyer | 🔴 High |

4.2 Inventory Scanning (Mobile)
| Element | Impact | Persona | Severity |
| Card height | Very low items per screen | Buyer | 🔴 High |

4.3 Filters (Mobile)
| Issue | Impact | Persona | Severity |
| Modal-only filters | Activation cost | Buyer | 🔴 High |
```

Why this fails:
- No Template Design paragraph (descriptive prose required)
- No Critical Immediate Fix callout (chat widget blocking imagery is absent entirely)
- Section split into mini-tables by element type rather than one persona-organised table
- "Buyer" is not a defined persona
- No Preserve entries
- No Journey Data Implications closing paragraph
- Recommendations missing entirely
- Findings carry no data points or visual confirmation

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
