# Vericore — Data Pain Points → Solutions → Stakeholder Decisions

The business case for a Vendor Master Data practice, in four failures and their fixes.

## 1. ERP field drift — Infor SX.e
**Pain:** one supplier enters as `ACME IND`, `Acme Industrial Supply` and
`Acme Ind. Supply Co.` — 14 field-format variants per vendor across branches.
It gets paid three ways.
**Solution:** standardization + survivorship rules in Stibo STEP; golden record per vendor.
**Decision unlocked:** AP can consolidate payment terms and stop duplicate pay.

## 2. Platform duplicates — Stibo STEP
**Pain:** up to 11 duplicate records per vendor. Without hierarchy roll-ups, a parent
with $4.2M in spend reports as eleven small vendors — invisible to negotiation.
**Solution:** deduplication, global parent wiring, hierarchy roll-ups.
**Decision unlocked:** category management sees true concentration and renegotiates
from strength.

## 3. Enrichment ambiguity — D&B
**Pain:** 27% of match candidates land below the auto-merge threshold; each needs
human, rule-based judgment.
**Solution:** thresholded auto-merge (≥90 confidence) + steward review queue with
documented decision criteria.
**Decision unlocked:** procurement gets compliance it can audit; analysts spend time
only on the ambiguous 27%.

## 4. Site-level variance — e-Crib network
**Pain:** 160+ customer storerooms and point-of-use locations transacting daily with
site-level records that never reconcile to the vendor master.
**Solution:** governed site feeds into STEP; nightly reconciliation to golden records.
**Decision unlocked:** site × field heatmap directs cleansing effort where it pays back
fastest; operations trust one vendor number everywhere.

## Value chain

| Pain point | Solution | Stakeholder | Decision made possible |
|---|---|---|---|
| Field drift (SX.e) | Standardize + survivorship | CFO / AP | Recover $1.2M duplicate payments |
| Duplicates (STEP) | Hierarchies + roll-ups | Category mgmt | Consolidate $0.9M tail spend |
| Enrichment ambiguity (D&B) | Thresholds + stewardship | Procurement | Auditable, defensible merges |
| Site variance (e-Crib) | Governed site feeds | Operations | Targeted cleansing, trusted reporting |
| **Net** | **$3.1M annualized** | **All** | Waterfall: +1.2 / +0.9 / +0.6 rebates / +0.4 freight |
