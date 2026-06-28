# EPCIS Traceability — Cow Ghee · Bhilwara Dairy

GS1 EPCIS 2.0.1 provenance trace for cow ghee lot **GHE-20260501** from
**Bhilwara Jila Dugdh Utpadak Sahkari Sangh Ltd**.

## Live page

👉 **[View the trace](https://peterbijoy.github.io/ghee-trace/)**
*(update this URL to match your GitHub username and repo name)*

## What this shows

A four-step backward trace from finished ghee back to the village milk societies:

| Step | Event type | Date | Product |
|---|---|---|---|
| 1 | TransformationEvent | 01 May 2026 | White butter → Cow ghee (81.3% yield) |
| 2 | TransformationEvent | 01 May 2026 | Cream → White butter (48.5% yield) |
| 3 | TransformationEvent | 01 May 2026 | Raw milk (3 routes) → Cream (10.5% yield) |
| 4 | ObjectEvent × 3    | **24 Apr 2026** | Milk collected from 29 BMCs / 27 societies |

## Standards

- **EPCIS 2.0.1** — GS1 event format
- **GS1 Digital Link 1.2** — `epcClass` as `https://id.gs1.org/01/{GTIN14}/10/{lot}`
- **NI URI event IDs** — SHA-256 content-addressed (`ni:///sha-256;…?ver=CBV2.0`)
- **CBV 2.0** — full URI bizStep and disposition values

## EPCIS files

| File | Description |
|---|---|
| `epcis_milk_route61_20260424_v4.json` | Route 61 milk receiving · 24 Apr 2026 |
| `epcis_milk_route63_20260424_v4.json` | Route 63 milk receiving · 24 Apr 2026 |
| `epcis_milk_route70_20260424_v4.json` | Route 70 milk receiving · 24 Apr 2026 |
| `epcis_cream_production_May2026_v4.json` | Cream production · May 2026 (11 days) |
| `epcis_butter_production_May2026_v4.json` | Butter production · May 2026 (11 days) |
| `epcis_ghee_production_May2026_v4.json` | Ghee production · May 2026 (11 days) |

## Publishing to GitHub Pages

```bash
git clone https://github.com/<your-username>/ghee-trace.git
cd ghee-trace
# copy files here, then:
git add .
git commit -m "Add EPCIS traceability page"
git push origin main
```

Then in the repo **Settings → Pages → Source → main branch / root**.
