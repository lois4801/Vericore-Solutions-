# VERICORE — Every Vendor. One Truth.

**Vericore** is a (concept) vendor-master-data intelligence company. It sells one thing: a
**governed golden record for every vendor**, built on **Stibo STEP** master data management,
**D&B** third-party enrichment, and **Infor SX.e** ERP integration — so every stakeholder
spend decision stands on data that can be trusted.

![Hero](assets/hero.png)

---

## Live site

**The full interactive command center — every visualization, animation and 3D layer — is the repo itself:**

| Where | Link |
|---|---|
| Open the site (this repo, `docs/`) | [`docs/index.html`](docs/index.html) |
| GitHub Pages (once enabled: Settings → Pages → `/docs`) | `https://<you>.github.io/vericore/` |

The site is a single self-contained HTML file (Tailwind / ECharts / GSAP / Three.js via CDN,
imagery embedded). Every chart is interactive: tooltips, hover states, live-updating feeds,
WebGL 3D with mouse parallax.

---

## Company at a glance

| | |
|---|---|
| **Tagline** | Every vendor. One truth. |
| **HQ** | Edmonton, AB, Canada — 53.55°N 113.49°W |
| **Stack** | Stibo STEP (MDM) · D&B enrichment · Infor SX.e / AS/400 · proprietary e-Crib network |
| **Core metric** | 42,318 raw vendor records → 31,240 golden records · 92/100 master-data health · $3.1M annualized recovery |
| **Method** | Ingest → Profile → Match → Merge → Govern |

---

## Services & products

- **[Services](docs/services.md)** — Integrated Supply, Vendor-Managed Inventory (VMI),
  Customer-Managed Inventory (CMI), storeroom management, point-of-use vending, digital
  procurement, safety services, e-Crib SaaS platform.
- **[Products](docs/products.md)** — MRO & safety supplies (millions of SKUs), own-manufactured
  safety equipment (Encon), vending hardware (CabLock, AccuCab), women's PPE line.
- **[Data pain points → solutions](docs/pain-points.md)** — the four fragmentation failures
  (SX.e field drift, STEP duplicates, D&B sub-threshold matches, e-Crib site variance) and the
  succeeding solution for each, mapped to stakeholder decisions.

---

## Visualization gallery

Each visualization in the command center answers a stakeholder question. Full write-up:
**[docs/visualizations.md](docs/visualizations.md)**

| Visualization | What it's for | What it solves |
|---|---|---|
| Duplicate-cluster network graph | See which records are the same vendor | Finds the 11× duplicate records per vendor before they split invoices |
| Live merge-resolution terminal | Watch governance happen | Auditability — every merge, enrichment and hierarchy change is logged |
| D&B match-confidence histogram | Know where automation stops | Separates auto-merge (≥90) from the 27% needing steward judgment |
| Vendor hierarchy sunburst | Roll sites up to parents | Makes $4.2M parent spend visible instead of eleven small vendors |
| Master-data health gauge | One number for trust | 92/100 — the confidence level every downstream report inherits |
| Spend Pareto | 80/20 concentration | Shows which vendors justify negotiated contracts |
| Record-lifecycle Sankey | Raw → golden flow | Quantifies the pipeline: 42,318 in, 31,240 governed out |
| Match-throughput area (24 wks) | Prove momentum | Auto-merge vs review vs reject trend over a governance program |
| Site × field heatmap | Target cleansing effort | Pinpoints which of 12 sites and 8 fields are dirty first |
| Supplier constellation (3D/WebGL) | Global relationship context | Rotating 3D view of the supplier network and its relationships |
| Quality-dimensions radar | Benchmark maturity | Today vs post-governance across 6 data-quality dimensions |
| Spend × confidence bubble matrix | Prioritize by value × risk | Amber priority zone = high-spend, low-confidence vendors fixed first |
| Deduplication waterfall | Dollars recovered | $3.1M annualized: duplicate-pay recovery, tail-spend consolidation, rebates, freight |
| Method timeline | The operating model | The 5-step lifecycle: Ingest → Profile → Match → Merge → Govern |

### Preview

| Core dashboard | 3D + radar + matrix | Impact |
|---|---|---|
| ![core](assets/signal-core.png) | ![3d](assets/signal-3d.png) | ![impact](assets/impact.png) |

---

## Repo structure

```
vericore/
├── index.html                  # redirect → docs/
├── docs/
│   ├── index.html              # THE SITE (self-contained, Pages-ready)
│   ├── services.md             # company services
│   ├── products.md             # company products
│   ├── pain-points.md          # data pain points → solutions → decisions
│   └── visualizations.md       # what every visualization is for & solves
└── assets/                     # rendered screenshots used in this README
```

## Run locally

Open `docs/index.html` in any modern browser. No build step, no server required.
