# Vericore — Visualization Guide

What every visualization in the command center (`docs/index.html`) is **for**, and what
**problem it solves**. All charts are interactive (tooltips, hover, live updates);
the two 3D scenes are WebGL with continuous animation and mouse parallax.

## 1. Hero — WebGL particle network (Three.js)
**For:** first impression of the vendor graph as a living network.
**Solves:** nothing to click — it sets the mental model: records are nodes, governance
connects them.

## 2. Duplicate-cluster network graph (ECharts force graph)
**For:** seeing which scattered records are actually the same vendor.
**Solves:** makes duplication tangible — each cluster is one vendor wearing many names.
Hover a node to isolate its cluster.

## 3. Live merge-resolution terminal
**For:** watching governance operate in real time.
**Solves:** auditability. Streams MERGED / REVIEW / D&B ENRICH / HIERARCHY events with
timestamps — the operational trail auditors ask for.

## 4. D&B match-confidence histogram
**For:** knowing exactly where automation ends.
**Solves:** staffing. Bars left of the dashed 90 line are steward work; right of it is
auto-merge. The red-to-volt gradient is the risk gradient.

## 5. Vendor hierarchy sunburst
**For:** rolling thousands of sites up to parents.
**Solves:** the "eleven small vendors" problem — one ring in, and $4.2M of concentration
appears that was invisible at vendor level.

## 6. Master-data health gauge (92/100)
**For:** a single trust number for the whole master.
**Solves:** meeting alignment — every downstream dashboard inherits this score's credibility.

## 7. Spend Pareto (bars + cumulative line)
**For:** 80/20 vendor concentration.
**Solves:** negotiation targeting — the amber 80% line shows how few vendors cover most
spend, and where contract consolidation pays.

## 8. Record-lifecycle Sankey
**For:** quantifying the raw → golden pipeline.
**Solves:** program reporting — 42,318 records in; 21,200 auto-merged, 8,900 steward-merged,
3,618 rejected; 31,240 golden out. Nothing disappears silently.

## 9. Match-throughput stacked area (24 weeks)
**For:** governance momentum over time.
**Solves:** program proof — auto-merge volume grows as rules mature; review and reject
shrink. Shows the practice compounding, not one-off cleaning.

## 10. Site × field data-quality heatmap
**For:** targeting cleansing effort.
**Solves:** triage across 12 sites × 8 critical fields. Red cells are where dirty data
costs money first — fix order, not guesswork.

## 11. Supplier constellation — 3D globe (Three.js/WebGL)
**For:** the global vendor relationship space.
**Solves:** context at a glance — volt nodes are suppliers, cyan threads are
relationships; rotation is continuous; back-hemisphere is occluded for depth reading.

## 12. Quality-dimensions radar
**For:** benchmarking record maturity on six dimensions (completeness, uniqueness,
consistency, validity, timeliness, accuracy).
**Solves:** gap honesty — the red "today" polygon vs the volt "post-governance" target
shows exactly which dimension the practice moves.

## 13. Spend × confidence bubble matrix
**For:** prioritizing vendors by value × data risk.
**Solves:** sequencing. Bubble size = duplicate count. The amber **priority zone**
(high spend, below merge threshold) is the fix-first list — biggest dollars riding on
the least trustworthy records.

## 14. Deduplication value waterfall
**For:** the money.
**Solves:** executive buy-in — $3.1M annualized, decomposed into duplicate-pay recovery
(+1.2M), tail-spend consolidation (+0.9M), rebate-tier capture (+0.6M), freight
optimization (+0.4M).

## 15. Method timeline (Ingest → Profile → Match → Merge → Govern)
**For:** the operating model.
**Solves:** repeatability — anyone can see the five steps, their inputs, and why the
order matters.


---

## Linked interactions — charts that respond to each other

The command center is not a dashboard of isolated widgets. From the Signal section onward,
charts share one filter state:

| You click… | …and these respond |
|---|---|
| **Sunburst category** (e.g. *Safety & PPE*) | Scatter matrix dims all non-category bubbles; Pareto highlights that category's vendors; filter chip appears |
| **Histogram bucket** (D&B confidence range) | Scatter dims bubbles outside that confidence band; chip shows the active range |
| **Pareto bar** (a vendor) | That vendor's bar isolates at full opacity; the rest fade; chip shows the vendor |
| **✕ RESET chip** (or re-click the same element) | Full state restored |

The chip at the top of the Signal section (`LINKED FILTER`) always displays the active
combination, e.g. `category: Safety & PPE · confidence 90–95%` — so a stakeholder can
verbally reproduce any view they are looking at.
