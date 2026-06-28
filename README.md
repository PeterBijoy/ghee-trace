# EPCIS Traceability Demo — Cow Ghee · Bhilwara Dairy

GS1 EPCIS 2.0.1 provenance trace for cow ghee lot **GHE-20260501**.

## Live pages

| Page | URL |
|---|---|
| 🧈 Trace page | `https://peterbijoy.github.io/ghee-trace/` |
| 📱 QR code | `https://peterbijoy.github.io/ghee-trace/qr.html` |
| 🔗 Digital Link URI | `https://peterbijoy.github.io/ghee-trace/01/08908016987457/10/GHE-20260501/` |

## GS1 Identifiers (GCP: 8908016987)

| Product | GTIN-14 | GS1 Digital Link URI |
|---|---|---|
| Cow Ghee | 08908016987457 | id.gs1.org/01/08908016987457/10/GHE-20260501 |
| White Butter | 08908016987037 | id.gs1.org/01/08908016987037/10/BTR-20260501 |
| Cream | 08908016987020 | id.gs1.org/01/08908016987020/10/CRM-20260501 |
| Raw Milk | 08908016987013 | id.gs1.org/01/08908016987013/10/R61-20260424 |

## GLNs (GCP: 8908016987)

| Location | GLN-13 |
|---|---|
| Bhilwara Dairy Plant | 8908016987006 |
| Route 61 | 8908016987617 |
| Route 63 | 8908016987631 |
| Route 70 | 8908016987709 |
| BMC Rajyas (55) | 8908016987112 |
| BMC Kanechan Khurd (1079) | 8908016987129 |
| *(29 BMCs total — refs 11–51)* | |
| *(27 societies total — refs 71–97)* | |

## Repo structure

```
ghee-trace/
├── index.html                                    ← trace page
├── qr.html                                       ← QR generator
├── 01/
│   └── 08908016987457/
│       └── 10/
│           └── GHE-20260501/
│               └── index.html                    ← DL redirect
├── epcis_ghee_production_May2026_v5.json
├── epcis_butter_production_May2026_v5.json
├── epcis_cream_production_May2026_v5.json
├── epcis_milk_route61_20260424_v5.json
├── epcis_milk_route63_20260424_v5.json
└── epcis_milk_route70_20260424_v5.json
```

## Standards

EPCIS 2.0.1 · GS1 Digital Link 1.2 · CBV 2.0 · NI SHA-256 eventIDs
Milk collected: 24 Apr 2026 · Routes 61/63/70 · 29 BMCs · 27 societies
