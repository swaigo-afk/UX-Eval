# Module 3: Analytics & Friction Hypotheses
**Produces: Executive Summary, Section 1 (Analytics Signals), Section 2 (Friction Hypotheses)**

---

## Prerequisites
- Module 1 (Foundation) loaded via URL field
- Module 2 (Data) pasted into the prompt

---

## Instructions

### Step 0 — DATA INTEGRITY CHECK (internal, not shown in output)

Before writing any section, run all six verification checks on every figure in the dataset. Use a think block:

For each figure you plan to use:
- What column did it come from?
- Is it inbound or outbound?
- What is the denominator population?
- Does the ratio make sense?
- Are time periods aligned?
- Is there a survivorship bias risk?

List figures that fail any check. List corrected figures. List any figures excluded as UNVERIFIED.

Do not proceed to Step 1 until all figures are verified or excluded.

---

### Step 1 — ANALYTICS SIGNALS

Write the Executive Summary (5–8 sentences: key metrics, two-sentence diagnosis, three top changes).

Then write Section 1 of the report. Include three sub-tables:

**1a. Journey Data table** — key flow metrics: total sessions, drop-off rate (with count), external entry % (with count), inbound from specific sources (with % of total), outbound to lots (with %), oscillation rate (with numerator/denominator), Step+2 return-to-lots %, key exits with drop-off rates. Label clearly: inbound vs outbound, time period, data source. Note that session counts are from Mouseflow (behavioural sample) and traffic volume is from Adobe Analytics.

**1b. Engagement Data table** — template-level metrics: unique visitors, new visitors %, organic %, bounce rate, avg time, follow rate, click-through to lots. Label column as "Artist Pages Avg" not "Site Average". Source: Adobe Analytics.

**1c. Filter Behaviour table** — Visits column (not Filter Applied). Columns: Filter name | Visits using filter | Filter events | Events per visit. Add note explaining why Visits is the correct measure and what high events-per-visit indicates.

After the tables, write a "New Findings" note for any figures that represent a change from prior periods or a genuinely new signal in the data.

---

### Step 2 — FRICTION HYPOTHESES

Write Section 2. Generate 6–10 hypotheses grounded in the data. For each hypothesis:

- **Hypothesis number and title** with traffic light flag (🟥/🟨/🟩)
- **Persona(s) affected** (use persona names exactly)
- **Status:** CONFIRMED (data directly supports) | INFERRED (mechanistically plausible, data consistent but not direct proof) | UNKNOWN (qualitative signal only, no supporting data)
- **Body:** 3–5 sentences. Lead with the data. Explain the mechanism. End with the scale of impact.

Order by severity descending.

---

## Output for this module

Start with the title block:

```
# Artist Overview Page — UX Evaluation Report
**Desktop + Mobile | [Artist Name] Reference Page**
Date: [date]
Data period: [journey data period] | [engagement data period]
```

Then output: Executive Summary, Section 1, Section 2.

Stop after Section 2. Do not proceed to the desktop critique — that is Module 4.
