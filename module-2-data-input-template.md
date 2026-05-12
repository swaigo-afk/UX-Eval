# Module 2: Data Input Template

**Paste this filled-in when CoPilot asks for Stage 1 inputs. Changes every run.**

---

## Instructions

Replace each placeholder below with the actual data. All three datasets plus screenshots are required for a complete evaluation. The prompt will not produce accurate output with partial data.

---

## Data Inputs

### Journey Data CSV

Paste the Mouseflow or equivalent page-flow export. Required columns: `stepOfSource`, `sourcePage`, `targetPage`, `linkCount`, `sourceDrops`, `sourceEntries`.

Note: Mouseflow is a behavioural sample, not total traffic — per foundation §2, session counts here will be lower than Adobe Analytics traffic figures and must be labelled as a sample throughout the report.

```
[[ Paste journey data CSV here ]]
```

### Engagement Data (Adobe Analytics)

Artist-level metrics: unique visitors, new visitors %, organic %, bounce rate, avg time on page, follow rate, click-through to lots. Include artist comparison table if available.

```
[[ Paste engagement data here ]]
```

### Filter Behaviour Data

Two columns required:

- **Visits** — distinct sessions using the filter. This is the intent signal.
- **Events** — total interactions on the filter. Can be inflated by range slider drag behaviour or repeat-fire controls.

Per foundation §2, intent is measured by Visits only. Any filter with an Events-per-Visit ratio above 3× is interaction-heavy, not intent-heavy.

```
[[ Paste filter behaviour data here. Columns: Filter | Visits | Events ]]
```

### Visual Inputs

Visual evidence enables the desktop and mobile critique stages to produce CONFIRMED findings rather than INFERRED ones. Without screenshots, layout-specific issues (e.g. chat widget placement, card hierarchy, filter visibility) drop to INFERRED status — which weakens the recommendations.

**Desktop screenshot:** `[paste image or attach file; describe layout briefly if no image available]`

**Mobile screenshot:** `[paste image; specify device and viewport, e.g. iPhone 14 Pro Max, 430px]`

### Context Variables

```
Artist page being evaluated: [Artist Name]
Reference URL: [Christie's URL of the artist page being evaluated]
Device for mobile review: [Device model + viewport width, e.g. iPhone 14 Pro Max, 430px]
Data period — journey data: [start date – end date]
Data period — engagement data: [start date – end date]
```
