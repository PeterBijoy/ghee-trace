# Bhilwara Dairy — GS1 EPCIS Traceability Demo

**Bhilwara Jila Dugdh Utpadak Sahkari Sangh Ltd**  
GS1 EPCIS 2.0.1 end-to-end traceability from village milk collection societies to finished cow ghee.

---

## 🔗 Live Pages

| Page | URL |
|---|---|
| 🧈 Trace page | [peterbijoy.github.io/ghee-trace](https://peterbijoy.github.io/ghee-trace/) |
| 📱 QR code generator | [peterbijoy.github.io/ghee-trace/qr.html](https://peterbijoy.github.io/ghee-trace/qr.html) |
| 🔗 GS1 Digital Link URI | [peterbijoy.github.io/ghee-trace/01/08908016987457/10/GHE-20260501](https://peterbijoy.github.io/ghee-trace/01/08908016987457/10/GHE-20260501/) |

---

## 📦 Product

| Field | Value |
|---|---|
| Product | SARAS Cow Ghee |
| GTIN-13 | 8908016987457 |
| GTIN-14 | 08908016987457 |
| Lot number | GHE-20260501 |
| GCP | 8908016987 |
| Production date | 01 May 2026 |
| Licensee | BHILWARA ZILA DUGDH UTPADAK SAHAKARI SANGH LTD |
| Address | 5 KM Stone, Bhilwara, Rajasthan — 311001 |
| MO | GS1 India |

---

## 🗺️ Traceability Chain

```
Cow Ghee (GHE-20260501)
    ↑  TransformationEvent · 01 May 2026 · 14:00 IST · yield 81.33%
White Butter (BTR-20260501) · 1,500 kg
    ↑  TransformationEvent · 01 May 2026 · 12:00 IST · yield 48.48%
Cream (CRM-20260501) · 3,093.75 kg
    ↑  TransformationEvent · 01 May 2026 · 10:00 IST · yield 10.5%
Raw Cow Milk · 29,464.3 kg
    ↑  ObjectEvent × 3 routes · 24 April 2026
    ├── Route 61 · 9,380 kg · Fat 4.64% · SNF 8.55 · 11 BMCs · 14 societies
    ├── Route 63 · 8,570 kg · Fat 5.52% · SNF 8.54 · 7 BMCs  · 9 societies (cow milk)
    └── Route 70 · 9,670 kg · Fat 4.18% · SNF 8.42 · 11 BMCs · 17 societies
```

**Total:** 27,620 kg cow milk · 29 BMC stops · 27 village milk collection societies

---

## 🏷️ GS1 Identifiers (GCP: 8908016987)

### GTIN-14s

| Product | GTIN-14 | GS1 Digital Link URI |
|---|---|---|
| Cow Ghee | 08908016987457 | id.gs1.org/01/08908016987457/10/GHE-20260501 |
| White Butter | 08908016987037 | id.gs1.org/01/08908016987037/10/BTR-20260501 |
| Cream | 08908016987020 | id.gs1.org/01/08908016987020/10/CRM-20260501 |
| Raw Milk | 08908016987013 | id.gs1.org/01/08908016987013/10/R61-20260424 |

### GLN-13s

| Location | Ref | GLN-13 |
|---|---|---|
| Bhilwara Dairy Plant | 00 | 8908016987006 |
| Route 61 | 61 | 8908016987617 |
| Route 63 | 63 | 8908016987631 |
| Route 70 | 70 | 8908016987709 |
| 11 BMCs Route 61 | 11–21 | 8908016987112 … 8908016987211 |
| 7 BMCs Route 63 | 31–37 | 8908016987310 … 8908016987372 |
| 11 BMCs Route 70 | 41–51 | 8908016987415 … 8908016987518 |
| 27 Village societies | 71–97 | 8908016987716 … 8908016987971 |

---

## 📂 Repository Structure

```
ghee-trace/
├── index.html                                      ← Full trace page (DataKart + EPCIS chain)
├── qr.html                                         ← QR code generator
├── README.md                                       ← This file
│
├── 01/
│   └── 08908016987457/
│       └── 10/
│           └── GHE-20260501/
│               └── index.html                      ← GS1 Digital Link redirect page
│
├── epcis_ghee_production_May2026_v5.json           ← TransformationEvent (11 days)
├── epcis_butter_production_May2026_v5.json         ← TransformationEvent (11 days)
├── epcis_cream_production_May2026_v5.json          ← TransformationEvent (11 days)
├── epcis_milk_route61_20260424_v5.json             ← ObjectEvent · Route 61 · 24 Apr 2026
├── epcis_milk_route63_20260424_v5.json             ← ObjectEvent · Route 63 · 24 Apr 2026
└── epcis_milk_route70_20260424_v5.json             ← ObjectEvent · Route 70 · 24 Apr 2026
```

---

## 📋 EPCIS Files

| File | Event type | Date | Events |
|---|---|---|---|
| epcis_milk_route61_20260424_v5.json | ObjectEvent | 24 Apr 2026 | 1 |
| epcis_milk_route63_20260424_v5.json | ObjectEvent | 24 Apr 2026 | 1 |
| epcis_milk_route70_20260424_v5.json | ObjectEvent | 24 Apr 2026 | 1 |
| epcis_cream_production_May2026_v5.json | TransformationEvent | 01–11 May 2026 | 11 |
| epcis_butter_production_May2026_v5.json | TransformationEvent | 01–11 May 2026 | 11 |
| epcis_ghee_production_May2026_v5.json | TransformationEvent | 01–11 May 2026 | 11 |

---

## 🔍 Demo Flow

```
1. Open qr.html → generate and print QR code
2. Scan QR with smartphone camera
3. Browser opens: peterbijoy.github.io/ghee-trace/01/08908016987457/10/GHE-20260501/
4. Spinner shows GTIN + lot → instant redirect to trace page
5. Trace page loads:
   ├── Product card (live from GS1 DataKart API)
   ├── GS1 Digital Link identifier bar
   ├── Date banner (milk 24 Apr → ghee May 2026)
   └── EPCIS event chain (ghee → butter → cream → milk → 27 societies)
6. Expand route cards to drill into BMCs and village societies
```

---

## 🛠️ Standards & Conformance

| Standard | Version | Usage |
|---|---|---|
| GS1 EPCIS | 2.0.1 | Event format for all 6 files |
| GS1 CBV | 2.0 | Full URI bizStep and disposition values |
| GS1 Digital Link | 1.2 | DL URI as primary epcClass identifier |
| GS1 General Specifications | 24.0 | GTIN-14 and GLN-13 check digit calculation |
| NI URI (RFC 6920) | — | SHA-256 content-addressed eventIDs |

**Key conformance features:**
- `epcClass` uses GS1 Digital Link URI (not LGTIN URN) in all quantity elements
- `eventID` is a content-addressed NI SHA-256 URI — tamper-evident
- `bizStep` and `disposition` use full CBV URI form
- `readPoint` and `bizLocation` use GS1 Digital Link GLN URI
- `sensorMetadata` (correct capitalisation per EPCIS 2.0.1 JSON-LD schema)
- No `additionalProperties` in `quantityElement` (validated against GS1 JSON schema)
- `dairy:milkCollectionDate` links all transformation events back to 24 Apr 2026 collection

---

## 🌐 GS1 Digital Link Resolution

For production deployment, register GTIN `08908016987457` with GS1 India's resolver so that:

```
https://id.gs1.org/01/08908016987457/10/GHE-20260501
    ↓  (GS1 India resolver)
https://peterbijoy.github.io/ghee-trace/
```

For this demo the GitHub Pages path mirrors the DL URI structure directly — only the domain changes when connected to the GS1 resolver.

---

## 📞 Contact

**GS1 India**  
[www.gs1india.org](https://www.gs1india.org)

*Implemented by GS1 India using GS1 EPCIS 2.0.1 and GS1 Digital Link standards.*
