# Module 3 — Stage 1: Analytics Signals & Friction Hypotheses

## Prerequisites

You must have read `module-1-foundation.md`. The rules there are binding for this stage. In particular:
- §2 (Visits vs Events) — applies directly to filter behaviour.
- §3 (Structural Framing Rule) — applies to every hypothesis.
- §4 (Persona Tagging) — applies to every hypothesis.
- §7 (Severity Flag System) — applies to every hypothesis.

## Inputs

You will be provided with:
- Adobe Analytics export (traffic, engagement, filter behaviour)
- Mouseflow journey data (flows, oscillation, drop-off, entry/exit)
- Date ranges for both
- The artist page reference instance being used as the template proxy

## Output

Two sections, formatted exactly as below.

---

### Section 1: Analytics Signals

Open with **one sentence** stating that two data sources are used in this report — Adobe Analytics for traffic and engagement, Mouseflow for journey behaviour — and a second sentence noting that Mouseflow is a behavioural sample, not total traffic.

Then produce three tables, in this order:

#### 1.1 Adobe Analytics — Traffic & Engagement

Headline format: `Adobe Analytics — Traffic & Engagement ([date range])`

| Metric | Value |
|--------|-------|
| Unique visitors | [value] |
| % New visitors | [value] |
| Organic search traffic | [value] |
| Bounce rate | [value] |
| Avg time on page | [value] |
| Follow rate | [value] |
| Click-through to lots | [value] |

#### 1.2 Mouseflow Journey Data — Flow & Behaviour

Headline format: `Mouseflow Journey Data — Flow & Behaviour ([date range])`

Prefix the table with: *"Mouseflow captures a behavioural sample. Session counts below reflect tracked sessions only, not total traffic."*

| Metric | Value |
|--------|-------|

Include at minimum: tracked sessions, drop-off at artist page, external entries, top inbound internal sources, sessions navigating to live lot pages, of those returning without acting, of returning visits going back to lots, top exit destinations with drop-off percentages.

Format each row as: absolute number + percentage where relevant. Example: `Drop-off at artist page | 61.1% — 202,400 sessions`

#### 1.3 Filter Behaviour

Prefix the table with this exact definition (per foundation §2):

> *Visits = distinct sessions using that filter. Events = total interactions (a range slider fires once per drag position). Intent is measured by Visits only.*

| Filter | Visits | Events | Events / Visit |
|--------|--------|--------|----------------|

**Rank rows by Visits descending.** Not by Events.

After the table, produce a one-paragraph interpretation that:
- Names the intent order by Visits
- Flags any filter with a >3× Events/Visit ratio as **interaction-heavy, not intent-heavy**
- States whether the current sidebar order matches the intent ranking
- If the sidebar order is inverted relative to the intent ranking, state that explicitly

---

### Section 2: Friction Hypotheses

Produce **6–10 hypotheses**, numbered H1, H2, H3, etc.

Each hypothesis must follow this exact format:

```
### H[N] [Flag] — [Decisive structural statement]

**Personas:** [list] | **[STATUS]**

[2–4 sentences: data evidence + structural mechanism + measurable cost]
```

#### Structural statement requirements

- Must follow the structural framing rule from foundation §3.
- Must be a complete decisive sentence, not a topic label.
- Examples:
  - "Oscillation is structural, not incidental"
  - "Filters are ordered by prominence, not by use"
  - "The lot grid default is wrong for most active-intent visitors"
  - "Follow rate is low because the follow action is in the wrong place"
  - "Editorial drives traffic in but the template loses it"
  - "Dwell time gap reflects a template built for transactions, not discovery"

#### Evidence requirements

- Quote the specific metric. Don't generalise.
- Where possible, project the cost at 12-month scale.
- Tie the structural cause to a specific template element (card design, filter order, default grid state, hero composition, etc.).
- If the hypothesis is supported by both data and visual evidence (e.g. a screenshot), note both: "CONFIRMED — visual evidence from mobile screenshot".

#### Status requirements

- Use CONFIRMED only where backed by a quantitative data point or visual evidence.
- Use UNCONFIRMED for plausible inferences without data.
- Use NEEDS DATA for hypotheses requiring a data point that hasn't been gathered. Specify what data is needed.

#### Flag requirements

Apply foundation §7. Every hypothesis gets a flag. A hypothesis with a Critical flag should appear early in the H-numbering.

---

## Quality Bar

A hypothesis **fails** the quality bar if:

- It's descriptive rather than structural ("Filters could be more prominent" rather than "Filters are ordered by prominence, not by use").
- It lacks a persona tag.
- It lacks a status.
- It lacks a specific metric.
- It restates an observation already covered by another hypothesis.
- It includes hedging language on confirmed findings.

**If you produce fewer than 6 hypotheses that meet the bar, that is acceptable. Soft hypotheses padded to hit a count are not.**

## Common Failure Modes

These produced the weaker prior version. Each is forbidden:

- Treating Price as a dominant filter because of high Event count. See foundation §2.
- Producing numbered observations ("1. The page is too long. 2. Users get tired.") instead of structurally-framed hypotheses.
- Using prose paragraphs in place of the hypothesis block format.
- Mixing Mouseflow session counts with Adobe traffic figures.
