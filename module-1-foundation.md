# Module 1 — Foundation Rules

These rules apply to every stage of the artist page UX evaluation. Read in full before running any stage module. If any rule conflicts with a stage module instruction, the foundation rule wins.

---

## §1. Personas

Four personas. Tag every finding, hypothesis, and recommendation with the affected persona(s).

| Persona | Description | Primary intent |
|---------|-------------|----------------|
| **Seeker** | Largest-volume persona. Arrives from organic search with general interest in the artist. Mostly new visitors, mostly cold. | Discover available works, get oriented to the artist, decide whether to act |
| **Regular Bidder** | Returning users tracking specific artists or lots. Higher commitment baseline. | Monitor upcoming sales, follow lots, register, set alerts |
| **Casual Browser** | Exploratory traffic, often from editorial or lateral artist browsing. | Discover related artists, read context, follow narrative threads |
| **Curious Owner** | Sell-side persona. Researching whether to consign a work. | Find selling guidance, evaluate Christie's as a consignment partner |

Primary persona by volume: **Seeker**. Secondary: **Curious Owner**. Optimise for these two by default; Regular Bidder and Casual Browser findings are still in scope.

---

## §2. Data Interpretation Rules

### Visits vs Events

- **Visits** = distinct sessions using a filter. This is the **intent signal**.
- **Events** = total interactions on a filter. Can be inflated by repeat-fire controls (e.g. range sliders fire one event per drag position).
- **Always rank intent by Visits, never by Events.**
- Flag any filter with an Events-per-Visit ratio above 3× as **interaction-heavy, not intent-heavy** — its high event count is a control artifact, not a usage signal.

**Worked example:** a price range slider with 52,506 Events but 5,303 Visits has a ~9.9× ratio. This is fewer users than Category (19,719 Visits), Sale Type (9,296), or Availability (8,811). Treat Price as the **least-used** filter by intent, not the most-used. Any recommendation that promotes Price based on Events count is wrong.

### Data sources

- **Adobe Analytics** is the authority for traffic volume, bounce rate, dwell time, follow rate, click-through, and filter usage.
- **Mouseflow** is the authority for journey sequences, oscillation, drop-off, and flow behaviour. Mouseflow captures a behavioural sample, not total traffic — its session counts are lower than Adobe's and **must not be presented as traffic figures**.

State the source on every data point. Do not blend the two without flagging which provides which.

### Calibration baselines

Use these as reference points when calling severity:

- Bounce rate template average: 37.6%
- Avg time on page template average: 210.9s
- Follow rate template average: 0.095%
- Click-through to lots baseline: 23.0% (target: 30.0%)
- Organic share: 92.7% (high)
- New visitor share: 81.6% (high)

A page metric below the template average on engagement (or above on bounce) is a **confirmed underperformance signal**, not an observation.

---

## §3. Structural Framing Rule

Every confirmed hypothesis must be named as a **structural template failure**, not an incidental observation.

Required pattern:
- "[Issue] is structural, not incidental"
- "[Issue] reflects a template built for [X], not [Y]"
- Equivalent decisive framing

| Bad | Good |
|-----|------|
| "Price filter could be more prominent." | "Filters are ordered by prominence, not by use." |
| "Users sometimes loop between lot and artist pages." | "Oscillation is structural, not incidental — the template provides no information at artist level to resolve a lot evaluation." |
| "The follow rate is low." | "Follow rate is low because the follow action is in the wrong place." |
| "Mobile filters are hard to find." | "On mobile, filters are hidden entirely — the desktop problem becomes a mobile crisis." |

This framing matters because the report justifies template-level changes. Descriptive observations justify nothing.

---

## §4. Persona Tagging Rule

Every finding, hypothesis, and recommendation must carry:

1. **Persona(s)**: which of the four are affected. Multiple allowed.
2. **Status**: one of CONFIRMED, UNCONFIRMED, or NEEDS DATA.
   - `CONFIRMED` = backed by quantitative data or visual evidence.
   - `UNCONFIRMED` = plausible but not yet evidenced.
   - `NEEDS DATA` = requires a specific data point that hasn't been gathered. State what's needed.

In tables, use the persona name in a column. In hypothesis blocks, use the format:

> **Personas:** [list] | **[STATUS]**

---

## §5. Preserve Rule

Every device critique table (Sections 3 and 4) must include explicit **✓ Preserve** entries alongside the issues.

- **Minimum: 1 Preserve entry per persona per device.**
- A Preserve entry names what the current template does well for that persona and instructs the team not to regress it.
- Preserve entries are not filler — they are the guard rail against accidental regression in the redesign.

Format:
> ✓ | [Persona] | [What works for this persona] | Preserve

Without Preserve entries, the report only describes what's broken and gives the redesign no protection on what's already working. This is a hard requirement, not a stylistic preference.

---

## §6. Specificity Rule for Recommendations

Recommendations must be **shippable as written**. They must specify the change in enough detail that a designer or engineer can act without a follow-up question.

| Bad | Good |
|-----|------|
| "Promote price filter" | "Reorder sidebar: Category → Sale Type → Availability → Price" |
| "Improve filter visibility" | "Persistent filter chip bar with Sale Type and Availability above the lot grid; secondary filters in a 'More' drawer" |
| "Make CTAs clearer" | "Add artist-level Follow/Alert CTA below artist name on both desktop and mobile (full-width on mobile)" |
| "Add available lots module" | "Default the lot grid to upcoming/active lots; add 'Show all including sold' toggle" |
| "Improve card hierarchy" | "Replace 'ARTIST NAME (DATES)' with artwork title as the dominant heading on artist-specific page instances" |

Where a measurement target applies, include it (e.g. "Measure: follow rate uplift against template baseline of 0.095%").

---

## §7. Severity Flag System

Apply to every hypothesis, every finding row, and every roadmap item. **Do not leave blank.**

| Flag | Meaning | When to apply |
|------|---------|---------------|
| 🟥 Critical | Blocks core task or has direct measurable cost at scale | Mobile-first failures, primary-metric drivers, broken core flows, elements physically obstructing content |
| 🟧 Major | Significantly degrades experience for a primary persona | Misordered filters, weak conversion architecture, missing decision support |
| 🟨 Moderate | Reduces effectiveness but not blocking | Polish issues, secondary persona gaps |
| 🟩 Low | Minor or strategic-only | Future-state opportunities, nice-to-haves |

Calibration note: anything blocking imagery on mobile is Critical, not Major — mobile imagery is the strongest engagement hook the template has.

---

## §8. Output Discipline

- **Tables where specified, prose elsewhere.** Do not turn a critique table into a paragraph or vice versa.
- **No filler.** If a section has nothing of substance, write one sentence stating that and move on.
- **No hedging on confirmed findings.** "May", "could", "might" are reserved for UNCONFIRMED items.
- **Decisive recommendations.** State the call. Do not list options without picking one.
- **Length earns its place.** Every paragraph must add something a stakeholder couldn't get from the table.
- **No reframing or aspirational vocabulary.** "Reposition", "transform into", "elevate to", "build an authority hub" — all forbidden in the executive summary and discouraged elsewhere. State what changes, where, and why.

---

## §9. Executive Summary Constraint (synthesis stage only)

The executive summary must:

1. Open with a one-line statement of the structural problem the template has.
2. Name the **single most critical immediate fix** in its own paragraph or call-out — the one thing that must ship before anything else.
3. List the three highest-leverage changes that cover the majority of the measurable gap.
4. Be short. If it exceeds ~250 words, cut.

No reframing language. No strategy-deck phrasing. State the fix, name the priority, move on.

---

## §10. Formatting and Length Conventions

The report is a stakeholder deliverable. Formatting consistency matters as much as content discipline. These conventions apply to every stage.

**Note on the prompt itself:** the markdown styling used throughout these module files (bold, italics, headers, bullets) is for the human reading the prompt. Your output should follow the conventions below, which are deliberately more restrained.

### Typography conventions

| Element | Use for | Do not use for |
|---------|---------|----------------|
| **Bold** | Severity flag labels, hypothesis names, column headers, the Preserve marker, the single critical immediate fix callout | General emphasis within prose, every key term, every other sentence |
| *Italic* | Definitions, source notes, table prefix notes (e.g. *"Visits = distinct sessions..."*), quoted UI strings | Emphasis within prose |
| Headers (`##`, `###`) | Section and subsection boundaries only | Mini-headers within a paragraph block, breaking up prose |
| Bullet lists | Genuinely enumerable content (the three highest-leverage changes, the four personas) | Splitting a paragraph into fragments, every list of related ideas, prose dressed as a list |
| Numbered lists | Sequenced steps, numbered hypotheses (H1–HN), numbered open questions | Default for any list |
| Tables | Where specified by the stage module | Anywhere a sentence would carry the same content |
| Inline code | Literal UI strings being quoted (e.g. `"ARTIST NAME (DATES)"`) | Variable names, generic emphasis |

### Prose density

- **Default paragraph length: 3–5 sentences.** Single-sentence paragraphs are reserved for callouts and the executive summary opener.
- **No wall-of-text paragraphs.** A paragraph exceeding ~80 words should usually become two.
- **No fragmented prose.** A paragraph broken into one-sentence bullets isn't a list — it's prose pretending to be a list. Restructure as prose.
- **Blank line between paragraphs.** No exceptions.

### Length calibration

These are target lengths, not minimums. **Cut to fit. Padding to hit a length is a failure mode. Brevity where the content is brief is the goal.**

| Section | Target |
|---------|--------|
| Executive Summary | ~250 words max (hard cap) |
| Section 1.1–1.3 (Analytics) | Tables + ~150 words total of prose interpretation |
| Section 2 (Friction Hypotheses) | 6–10 hypotheses, each 2–4 sentences of evidence |
| Section 3 — Template Design para | 4–6 sentences, descriptive only |
| Section 3 — Issues table | One row per finding, no row count target |
| Section 3 — Journey Data Implications | 3–5 sentences |
| Section 4 — Template Design para | 4–6 sentences |
| Section 4 — Critical immediate fix callout | 1 sentence |
| Section 4 — Issues table | One row per finding |
| Section 4 — Journey Data Implications | 3–5 sentences |
| Section 5 (Cross-Device) | Table + one introductory sentence |
| Section 6 (SEO Context) | **3–4 short paragraphs, ~300 words max** |
| Section 7 (Roadmap) | Table only, no intro prose |
| Section 8 (Open Questions) | 4–8 questions, each 2–4 sentences |

### Length pattern to avoid

The prior version produced a Section 6 (SEO) of ~700 words and a Section 5 (Cross-Device) of ~600 words of prose, while compressing critical findings into one-sentence bullets elsewhere.

**Length must be proportional to the importance and density of the content, not to the prompt model's default verbosity for the topic.** SEO context is one of the shortest sections in this report, not one of the longest. The hypotheses and roadmap carry the weight — they get the words.

### Section transitions

- One blank line between paragraphs within a section.
- Two blank lines or a horizontal rule (`---`) between major sections.
- Section headers (`###`) on their own line with blank lines above and below.

### Markdown discipline in output

- Do not use `>` blockquotes except for the critical immediate fix callout in Section 4 and the executive summary callout in §9.
- Do not use horizontal rules within a section.
- Do not bold entire sentences.
- Do not nest lists.
- Do not produce a numbered list of one item.

---

## §11. Prose vs Table Reference

A persistent failure mode is converting prose sections into tables. The structural rule:

- **Tables** = structured data with consistent attributes per row (analytics metrics, persona-tagged findings, cross-device comparison, roadmap items).
- **Prose** = synthesis, interpretation, narrative, executive framing, single-flow analysis.

**Sections that are PROSE only:**
- Executive Summary
- Template Design paragraph (opening of Sections 3 and 4)
- Journey Data Implications (closing of Sections 3 and 4)
- Section 6 (SEO Context)

**Sections that are TABLE only:**
- Section 1.1, 1.2, 1.3 (Analytics)
- Section 5 (Cross-Device Comparison)
- Section 7 (Roadmap)

**Sections with BOTH (prose + table):**
- Section 3 (Desktop Critique): prose Template Design + table + prose Journey Implications
- Section 4 (Mobile Critique): prose Template Design + optional callout + table + prose Journey Implications

**Sections with structured blocks (NOT tables, NOT prose paragraphs):**
- Section 2 (Friction Hypotheses): each hypothesis is a heading + meta line + 2–4 sentence prose body
- Section 8 (Open Questions): each question is a heading + 2–4 sentence prose explanation

If a section is specified as prose, do not collapse it into a table or bullet list. If a section is specified as structured blocks, do not collapse it into a table.

---

## §12. Verbiage Reference

Concrete language patterns for the high-failure-mode sections.

### Structural framing patterns (Section 2 hypothesis titles)

Use one of these patterns for every confirmed hypothesis title:

- `[X] is structural, not incidental`
- `[Filters/Cards/Layout] [are/is] ordered by [X], not by [Y]`
- `[X] is low because [Y] is in the wrong place`
- `The [X] default is wrong for most [Y] visitors`
- `[X] drives [Y] in but the template loses it`
- `[X] is undesigned but significant`
- `[Metric] gap reflects a template built for [X], not [Y]`

**Worked examples:**
- "Oscillation is structural, not incidental"
- "Filters are ordered by prominence, not by use"
- "Follow rate is low because the follow action is in the wrong place"
- "The lot grid default is wrong for most active-intent visitors"
- "Editorial drives traffic in but the template loses it"
- "Lateral browsing is undesigned but significant"
- "Dwell time gap reflects a template built for transactions, not discovery"

### Persona + status line patterns

- `**Personas:** [Persona1], [Persona2] | **CONFIRMED**`
- `**Persona:** [Persona] | **CONFIRMED** — visual evidence from mobile screenshot`
- `**Personas:** [Persona] | **INFERRED**`
- `**Persona:** [Persona] | **NEEDS DATA** — device-segmented journey data required`

### Recommendation phrasing patterns

Each recommendation must be specific enough to ship. Use these patterns:

| Pattern | Example |
|---------|---------|
| `Reorder X: A → B → C → D` | "Reorder sidebar: Category → Sale Type → Availability → Price" |
| `Replace X with Y as the [position] [element]` | "Replace 'ARTIST NAME (DATES)' with artwork title as the dominant card heading" |
| `Add X [position] on [device] (full-width on mobile)` | "Add artist-level Follow/Alert CTA below artist name on both desktop and mobile (full-width on mobile)" |
| `Default X to Y; add Z toggle` | "Default grid to upcoming/active lots; add 'Show all including sold' toggle" |
| `Move X to [position]` | "Move chat widget to bottom-right corner" |
| `Promote X to [position]; remove Y from [position]` | "Promote artwork title to primary heading; remove artist name from lot cards on artist-specific page instances" |

### Critical immediate fix callout pattern

Single-sentence callout, starts with the action verb:

> **Critical immediate fix:** Move the floating chat widget off the first artwork image — fixed in upper-right viewport, physically overlapping the first lot card's image.

### Open question pattern (decision-forcing)

Each question follows this structure: **bold question label** — sentence stating the fork. Then a sentence per branch with implication. Then a sentence on what data resolves it.

> **1. Device split of the oscillation loop** — If the 61.5% oscillation is predominantly mobile, the fix is filter UX and above-fold hierarchy. If predominantly desktop, it is card design and information architecture. These need different solutions at different costs. Device-segmented journey data should be obtained before locking the roadmap sequence.

### Preserve entry phrasing

Each Preserve row: state what works for the persona in one or two phrases, then write `Preserve` in the recommendation column.

| Persona | Flag | Finding | Recommendation |
|---------|------|---------|----------------|
| Seeker | ✓ | Filter sidebar structurally correct — Category, Sale Type, and Availability exist and serve this persona when found. Two-column grid gives reasonable scanning density. | Preserve |

### Forbidden phrasings

| Don't | Do |
|-------|-----|
| "Promote price filter" | "Reorder sidebar: Category → Sale Type → Availability → Price" |
| "It appears users may struggle..." | "Users return without acting in 61.5% of sessions" |
| "Reposition the page as an authority hub" | "Replace artist name + dates with the artwork title as the primary card heading" |
| "How do users feel about filters?" | "If oscillation is predominantly mobile, the fix is filter UX. If desktop, card design. Device-segmented data resolves." |
| "Improve hierarchy" | "Replace 'ARTIST NAME (DATES)' with artwork title as the dominant heading" |

---

## §13. Anti-Compression Rule (BINDING — HIGHEST PRIORITY)

The most common output failure is compression — producing structurally correct but thin output. This rule overrides any inclination to "be concise" or "cover the key points."

### Reference examples are MINIMUMS, not targets

Every reference example in this foundation file and in each stage module shows the **minimum required depth**. Production output should match or exceed the example. Below the example is a failure.

If a module shows a 10-row example table, 10+ rows is the target. 5 rows is a failure. If a module shows a 230-word example paragraph, 200+ words is required. 80 words is a failure.

### Format conversion is forbidden

If a stage module specifies a **table**, produce a table. Do not convert to bullets. Do not convert to prose. Do not produce a mini-table with 2 rows.

If a stage module specifies **prose paragraphs**, produce prose paragraphs. Do not convert to bullets. Do not convert to a table. Do not produce a 2-sentence summary.

If a stage module specifies a **structured block format** (e.g. hypotheses, open questions), produce that exact format. Do not convert to a bulleted list.

### Hard minimums per section

These are **floors**, not targets. Output below these is a failure that must be expanded before shipping.

| Output | Hard minimum |
|--------|--------------|
| Section 1.1 Adobe Analytics table | 7 metric rows |
| Section 1.2 Mouseflow Journey table | 8 metric rows |
| Section 1.3 Filter Behaviour table | 6 filter rows |
| Section 2 Friction Hypotheses | 6 hypotheses, each with 3+ sentences of evidence prose |
| Section 3 Template Design paragraph | 4 sentences of descriptive prose |
| Section 3 Desktop Critique table | 10 rows total; minimum 2 rows per persona (1 Preserve + 1 issue) |
| Section 3 Journey Data Implications | 3 sentences of prose |
| Section 4 Template Design — Mobile paragraph | 4 sentences |
| Section 4 Critical Immediate Fix callout | 1 sentence in `>` blockquote format (if applicable) |
| Section 4 Mobile Critique table | 8 rows total; minimum 2 rows per persona |
| Section 4 Journey Data Implications | 3 sentences |
| Section 5 Cross-Device table | 6 rows; all 5 columns populated (Issue, Desktop, Mobile, Flag, Priority) |
| Section 6 SEO Context | 3 paragraphs, 200 words minimum, 300 max. **Bullets, tables, and subsection headers are forbidden in Section 6.** |
| Section 7 Roadmap table | 8 rows; all 4 columns populated (Feature, Priority, Description, Effort) |
| Section 7 A/B Test rows | Description column must include hypothesis + primary metric + decision rule |
| Section 8 Open Questions | 4 questions, each 3+ sentences in decision-fork format |
| Executive Summary | 180 words minimum, 250 max |
| Title Block | All 5 fields populated (Template scope, Reference instance, Date, Adobe Analytics period, Mouseflow period, Mobile device) |

### Compression check (apply at each stage before outputting)

Before producing the final output of any stage, ask:

1. Does each section meet its hard minimum from the table above?
2. Have I converted any table to bullets or prose? Revert.
3. Have I converted any prose section to bullets or a table? Revert.
4. Have I produced "key points" instead of full evidence? Expand.
5. Does this section feel terse? It probably is. Expand.

If any answer indicates compression, expand before shipping the stage output.

### Self-talk that signals compression

If you find yourself thinking any of the following, stop and expand:

- "I've covered the key points concisely"
- "Bullets are clearer here"
- "This is the most important content"
- "A short summary captures it"
- "The reader will get the idea"

This report's purpose is structural detail at stakeholder-decision depth. Concision is a failure mode, not a virtue.
