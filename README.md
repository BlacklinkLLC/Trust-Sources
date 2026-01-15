# Trust Source Data

> **Verified educational resources and research materials from the Trust ecosystem**

[![Trust Score](https://img.shields.io/badge/Trust%20Standard-V2-5533cc)](https://blacklink.net/trust)
![License: BL-RSL 1.0](https://img.shields.io/badge/License-BL-RSL%201.0-b98eff?style=flat)
[![Version](https://img.shields.io/badge/Version-1.3-8658ff)](https://blacklink.net)

---

## 📚 What is This?

This repository contains **source data, research materials, and educational resources** evaluated and scored by [Blacklink Trust](https://blacklink.net) - a Trustpilot-like platform for academic and educational content.

All materials here have been:
- ✅ Evaluated using Trust Standards V2
- ✅ Scored by Aero AI analysis
- ✅ Verified for academic integrity
- ✅ Licensed for open educational use

---

## 🎯 What's Inside

```
trust-source-data/
├── data.json          # All sources with Trust Scores and metadata
├── LICENSE.md         # The BL-RSL license v1.
├── STANDARD.pdf         # The Trust Source Standard in PDF format.
└── README.md          # This file
```

### Data Structure

Everything is in **`data.json`** - a single file containing all evaluated sources with their Trust Scores, metadata, and Aero analysis.

---

## 🔍 Trust Scores Explained

Every source in this collection includes a **Trust Score** (0-100) based on **Trust Standards V2**:

### Signal Categories

- **Identity** - Authorship clarity, organizational ownership, accountability
- **Evidence** - Citations, data sources, methodologies, factual support  
- **Recency** - Timeliness relative to subject matter requirements
- **Transparency** - Disclosure of intent, funding, affiliations, limitations
- **Safety** - Suitability for educational contexts, avoidance of harmful framing

### Score Bands

| Score | Label | Meaning |
|-------|-------|---------|
| 90-100 | **Highly Trusted** | Strong signals across all dimensions |
| 75-89 | **Trusted** | Reliable with minor limitations |
| 60-74 | **Caution** | Mixed or incomplete signals |
| 40-59 | **Low Confidence** | Significant gaps or ambiguity |
| 0-39 | **Not Trusted** | High risk or misleading indicators |

*Full scoring methodology: [Trust Standards V2](https://trust.blacklink.net/standard.html)*

---

## 🚀 Getting Started

### Browse Sources

```bash
# Clone the repository
git clone https://github.com/blacklink/trust-source-data.git
cd trust-source-data

# View all sources
cat data.json | jq '.'

# Check Trust Scores
cat data.json | jq '.sources[] | {title, trust_score, type}'
```

### Search by Category

```bash
# Find research papers
cat data.json | jq '.sources[] | select(.type == "research_paper")'

# Find datasets
cat data.json | jq '.sources[] | select(.type == "dataset")'

# Find high-trust sources (score ≥ 90)
cat data.json | jq '.sources[] | select(.trust_score >= 90)'
```

### Using in Your Research

1. **Find relevant sources** in the category folders
2. **Check the Trust Score** in `metadata/`
3. **Review the Aero analysis** for evidence summary
4. **Cite properly** using the attribution format below

---

## 📖 Citation & Attribution

All sources must be attributed according to **BTRL 1.0** requirements:

### Standard Citation Format

```
[Author(s)]. ([Year]). [Title]. Blacklink Trust Source Data.
Trust Score: [Score] (Evaluated: [Date])
Available at: [URL or DOI]
Licensed under BTRL 1.0.
```

### Example

```
Smith, J., & Doe, A. (2025). Machine Learning in Climate Models.
Blacklink Trust Source Data.
Trust Score: 92 (Evaluated: 2026-01-10)
Available at: https://github.com/blacklink/trust-source-data
Licensed under BTRL 1.0.
```

---

## ⚖️ License

This collection is licensed under the **Blacklink Trust Open Research License (BTRL) 1.0**.

### ✅ You CAN:
- Use for education and research
- Modify and create derivative works
- Share with proper attribution
- Include in academic papers and projects
- Analyze with AI/ML tools

### ❌ You CANNOT:
- Remove or alter Trust Scores
- Use without attribution
- Claim sources as your own work
- Use for commercial purposes (without permission)
- Misrepresent findings or conclusions

**Full license:** [LICENSE.md](LICENSE.md)

---

## 🤖 Aero AI Integration

All sources have been analyzed by **Aero AI** for:
- Evidence strength assessment
- Signal detection (bias, methodology, transparency)
- Context extraction
- Reasoning traces

Aero analysis is embedded in each source entry in `data.json`.

Run your own Aero evaluation: [trust.blacklink.net/aero](https://trust.blacklink.net/aero.html)

---

## 📊 Data Structure

The `data.json` file contains all sources in this format:

```json
{
  "version": "1.3.0",
  "generated": "2026-01-14T12:00:00Z",
  "total_sources": 1247,
  "sources": [
    {
      "source_id": "src_12345",
      "title": "Example Research Paper",
      "authors": ["Jane Smith", "John Doe"],
      "type": "research_paper",
      "url": "https://example.com/paper",
      "trust_score": 92,
      "evaluation_date": "2026-01-10",
      "signals": {
        "identity": 94,
        "evidence": 95,
        "recency": 88,
        "transparency": 88,
        "safety": 92
      },
      "aero_summary": "Strong methodological foundation with clear reproducibility...",
      "license": "BTRL-1.0",
      "doi": "10.1234/example"
    }
  ]
}
```",
  "title": "Example Research Paper",
  "authors": ["Jane Smith", "John Doe"],
  "type": "research_paper",
  "trust_score": 92,
  "evaluation_date": "2026-01-10",
  "signals": {
    "evidence_quality": 95,
    "transparency": 88,
    "identity_verified": true,
    "peer_reviewed": true
  },
  "aero_summary": "Strong methodological foundation...",
  "license": "BTRL-1.0",
  "doi": "10.1234/example",
  "file_path": "research/ml-climate-2025.pdf"
}
```

---

## 🛠️ Tools & Integration

### Use with Trust Platform

```javascript
// Import source data into Trust
import { TrustClient } from '@blacklink/trust-sdk';

const client = new TrustClient();
const sources = await client.importSources('./data.json');
```

### Python Data Analysis

```python
import json
import pandas as pd

# Load Trust data
with open('data.json') as f:
    data = json.load(f)

df = pd.DataFrame(data['sources'])
high_trust = df[df['trust_score'] >= 90]
print(high_trust[['title', 'trust_score', 'type']])
```

---

## 🤝 Contributing

We welcome contributions of verified educational resources!

### Submission Guidelines

1. **Verify quality** - Ensure content meets academic standards
2. **Include metadata** - Provide all required attribution info
3. **License properly** - Must be compatible with BTRL 1.0
4. **Run Aero** - Get Trust Score before submitting

**Submit sources:** Use a Pull request via Github with updates to the data.json file, if you would like to start a new repo of sources create a file with a name such as *ext1.json*

---

## 📞 Support & Contact

---

## 🔐 Data Integrity

- All Trust Scores are cryptographically signed
- Metadata includes verification hashes
- Aero analysis traces are preserved
- Audit trail available on request

---


## 🌟 Featured Collections

### High-Impact Research
Sources with Trust Score ≥ 95 and extensive citations
→ `collections/high-impact/`

### Reproducible Studies
Complete datasets with open methodology
→ `collections/reproducible/`

### Educational Standards
Curriculum-aligned teaching materials
→ `collections/educational-standards/`

---

## 🔄 Updates & Versioning

- **Source Data Version:** 1.3.0
- **Trust Standards:** V2
- **Aero Model:** NOVA 1.0
- **Last Updated:** 2026-01-14

Subscribe to updates: [trust.blacklink.net](https://trust.blacklink.net)

---

**Built with Trust 1.3 - The Living Layer for reliable sources**

*©2026 Blacklink, Inc. - Empowering open scholarship*
