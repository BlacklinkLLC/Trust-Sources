# Trust Source Data

> **Verified educational resources and research materials from the Trust ecosystem**

[![Trust Standard](https://img.shields.io/badge/Trust%20Standard-V2-5533cc?style=flat-square)](https://blacklink.net/trust)
[![License](https://img.shields.io/badge/License-BL--RSL%201.0-b98eff?labelColor=1b1233&style=flat-square)](https://trust.blacklink.net/licenses/bl-rsl)
[![Version](https://img.shields.io/badge/Version-1.3-8658ff?style=flat-square)](https://blacklink.net)

---

## 📚 What is This?

This repository contains **source data, research materials, and educational resources** evaluated and scored by **Blacklink Trust** — a credibility platform for academic and educational content.

All materials here have been:

- ✅ Evaluated using **Trust Standards V2**
- ✅ Scored using **Aero AI** (Only some sources)
- ✅ Verified for academic integrity
- ✅ Licensed for open educational and research use

---

## 🎯 Repository Contents

```
trust-source-data/
├── data.json        # Source registry with Trust Scores and metadata
├── LICENSE.md       # Blacklink Research Source License (BL-RSL)
├── STANDARD.pdf     # Trust Standards (V2)
└── README.md        # You are here
```

All source entries live in **`data.json`**.

---

## 🔍 Trust Scores

Each source includes a **Trust Score (0–100)** derived from five weighted signal groups:

### Signal Categories
- **Identity** — Authorship, ownership, accountability
- **Evidence** — Citations, data, methodology
- **Recency** — Timeliness relative to subject
- **Transparency** — Disclosure, funding, limitations
- **Safety** — Educational suitability

### Score Bands

| Score | Label | Description |
|------:|------|-------------|
| 90–100 | **Highly Trusted** | Strong signals across all dimensions |
| 75–89 | **Trusted** | Reliable with minor limitations |
| 60–74 | **Caution** | Mixed or incomplete signals |
| 40–59 | **Low Confidence** | Significant gaps |
| 0–39 | **Not Trusted** | High risk or misleading |

📘 Full methodology: https://trust.blacklink.net/standard.html

---

## 🚀 Getting Started

### Clone & Inspect

```bash
git clone https://github.com/BlacklinkLLC/Trust-Sources.git
cd Trust-Sources
jq '.sources[] | {title, trust_score}' data.json
```

### Filter High-Trust Sources

```bash
jq '.sources[] | select(.trust_score >= 90)' data.json
```

---

## 📖 Citation

All use requires attribution under **BL-RSL 1.0**.

```
Author(s). (Year). Title.
Blacklink Trust Source Data.
Trust Score: [Score] (Evaluated: [Date])
URL or DOI
Licensed under BL-RSL 1.0
```

---

## ⚖️ License

This dataset is licensed under the **Blacklink Research Source License (BL-RSL) v1.0**.

### You may:
- Use for education and research
- Modify and redistribute
- Create derivatives (share-alike)
- Analyze with AI systems

### You may not:
- Alter or remove Trust Scores†
- Misrepresent evaluations
- Remove attribution
- Apply more restrictive terms

📄 Full license: `LICENSE.md`


† Sources MAY be added by creating an ext#.jsonc file in the Extensions folder, then submitting a PR.
---

## 🤖 Aero AI

Some sources are analyzed by **Aero AI (NOVA 1.0)** for:

- Evidence strength
- Bias signals
- Transparency markers
- Context extraction

More info: https://aero.blacklink.net

---

## 🔐 Data Integrity

- Cryptographically signed Trust Scores
- Metadata hashes preserved
- Evaluation audit trails retained

---

## 🔄 Versioning

- **Data Version:** 1.3.0
- **Trust Standards:** V2
- **Aero Model:** NOVA 1.0
- **Last Updated:** 2026-01-14

---

**Trust 1.3 — The Living Layer**

© 2026 Blacklink, Inc. · *Empowering open scholarship*
